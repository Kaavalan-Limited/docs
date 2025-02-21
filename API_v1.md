# IP_API

## Overview
The **IP Information API** provides detailed insights about a given IP address, including ASN details, location, ISP, carrier information, threat intelligence and user analytics.

## Endpoint

```
GET https://api.cybercheck360.com/v1/ip/{{api_key}}/{ip}/?user_analytics={user_analytics}
```

## Query Parameters

| Parameter         | Type    | Required | Description |
|------------------|---------|----------|-------------|
| `ip`            | string  | Yes      | The IP address to retrieve details for (e.g., `165.166.221.197`). |
| `kaavalan`      | boolean | No       | Set to `True` to include threat intelligence details. Defaults to `False`. |
| `user_analytics`| boolean | No       | Set to `True` to include user analytics data in the response. Defaults to `False`. |

## Sample Request

```http
GET https://api.cybercheck360.com/v1/ip/{{api_key}}/165.166.221.197/?user_analytics=True
```

## Response

The API response includes multiple sections depending on the parameters enabled.

### Full Response (With All Parameters Enabled)

```json
{
  "ip": "165.166.221.197",
  "hostname": "example.com",
  "type": "IPv4",
  "asn": 12345,
  "isp": "Example ISP",
  "carrier": "Example Carrier",
  "location": { ... },
  "threat_intel": { ... },
  "user_analytics": { ... }
}
```

### Individual Responses by Parameter

#### Base Response (Always Included)
```json
{
  "ip": "165.166.221.197",
  "hostname": "example.com",
  "type": "IPv4",
  "asn": 12345,
  "isp": "Example ISP",
  "carrier": "Example Carrier",
  "location": {
    "country_code": "US",
    "country_name": "United States",
    "region_code": "CA",
    "region_name": "California",
    "city": "Los Angeles",
    "zip": "90001",
    "latitude": 34.0522,
    "longitude": -118.2437,
    "is_eu": false
  },
  "threat_intel": {
    "listings": {
      "Malware": 5,
      "Spam": 10,
      "Exploit": 3,
      "Botnet": 2,
      "Anonymizer": 1
    },
    "tags": ["malware", "botnet"],
    "tor": false,
    "proxy": true,
    "crawler": false
  }
}
```

#### Threat Intelligence

CyberCheck360 aggregates intelligence information from multiple threat intelligence feeds and categorizes them into six key categories:

- **Malware**
- **Anonymizer**
- **Spam**
- **Botnet**
- **Phishing**
- **Exploit**

Each domain or IP is analyzed and classified based on the number of threat feeds it appears in. If a domain is listed under a specific category, it means that multiple intelligence sources have flagged it under that classification.

For example, if a response shows `"Malware": 5`, it indicates that the domain/IP appears in 5 independent threat intelligence feeds that categorize it as malware.

```json
{
  "threat_intel": {
    "listings": {
      "Malware": 5,
      "Spam": 10,
      "Exploit": 3,
      "Botnet": 2,
      "Anonymizer": 1
    },
    "tags": ["malware", "botnet"],
    "tor": false,
    "proxy": true,
    "crawler": false
  }
}
```
In the above response:
- The domain/IP is listed in **5 feeds** that classify it as **Malware**.
- It is also present in feeds that categorize it as **Spam (10 feeds), Exploit (3 feeds), Botnet (2 feeds), and Anonymizer (1 feed)**.
- The `tags` field summarizes the primary classifications, in this case, **malware** and **botnet**.
- The `tor`, `proxy`, and `crawler` fields indicate whether the domain is associated with **Tor networks**, **proxy services**, or **web crawlers**.


#### User Analytics (If `user_analytics=True`)
```json
{
  "user_analytics": {
    "search_count": 200,
    "fp_reports_count": 50,
    "malicious_reports_count": 20,
    "user_blacklist_count": 5,
    "user_whitelist_count": 30
  }
}
```

<!-- #### Kaavalan Feeds
```json
{
  "kaavalan_feeds": {
    "confidence": "high",
    "category": "phishing",
    "tags": "malware, botnet",
    "verdict": "malicious"
  }
}
``` -->

## Error Responses

| Status Code | Description |
|------------|-------------|
| `400`      | Bad request. Ensure required parameters are correctly formatted. |
| `401`      | Unauthorized. Invalid or missing API key. |
| `403`      | Forbidden. Access to the requested resource is denied. |
| `404`      | IP not found. The requested IP does not exist. |
| `500`      | Internal Server Error. An unexpected error occurred on the server. |

<!-- ## Rate Limits
- Each API key is subject to rate limits.
- If rate limits are exceeded, a `429 Too Many Requests` response will be returned.

## Contact
For support or questions, please reach out to the API provider.

## License
This project is licensed under the MIT License - see the LICENSE file for details. -->

---


# Domain_API

## Description
The **Domain Information API** provides detailed insights about a given domain, including registration details, SSL certificate information, DNS records, user analytics, threat intelligence, and rankings.

## Endpoint

```
GET https://api.cybercheck360.com/v1/domain/{{api_key}}/?domain={domain}&ssl_details={ssl_details}&user_analytics={user_analytics}&rankings={rankings}
```

## Query Parameters

| Parameter       | Type    | Required | Description |
|----------------|---------|----------|-------------|
| `domain`       | string  | Yes      | The domain name to retrieve details for (e.g., `twitter.com`). |
| `ssl_details`  | boolean | No       | Set to `True` to include SSL certificate details in the response. Defaults to `False`. |
| `user_analytics` | boolean | No      | Set to `True` to include user analytics data in the response. Defaults to `False`. |
| `rankings`     | boolean | No       | Set to `True` to include domain rankings from various sources. Defaults to `False`. |

## Sample Request

```http
GET https://api.cybercheck360.com/v1/domain/{{api_key}}/?domain=twitter.com&ssl_details=True&user_analytics=True&rankings=True
```

## Response

The API response includes multiple sections depending on the parameters enabled.

### Full Response (With All Parameters Enabled)

```json
{
  "domain": "example.com",
  "timestamp": "2022-01-01T00:00:00Z",
  "registration_date": "2020-01-01",
  "last_update_date": "2022-01-01",
  "expiration_date": "2023-01-01",
  "organization": "Example Organization",
  "registrar": "Example Registrar",
  "name_servers": ["ns1.example.com", "ns2.example.com"],
  "abuse_emails": ["abuse@example.com"],
  "ssl_details": {
    "owner_org": "Example Organization",
    "owner_country": "US",
    "issuer_org": "Example Issuer",
    "issuer_country": "US",
    "serial_number": "1234567890",
    "version": "TLSv1.2",
    "valid_from": "2022-01-01",
    "valid_to": "2023-01-01",
    "fingerprint_sha256": "fingerprint123"
  },
  "dns": {
    "A": ["192.0.2.1"],
    "AAAA": ["2001:0db8:85a3:0000:0000:8a2e:0370:7334"],
    "MX": ["mx.example.com"],
    "NS": ["ns1.example.com", "ns2.example.com"],
    "TXT": ["example TXT record"],
    "spf_status": "valid",
    "SOA": "example SOA record"
  },
  "threat_intel": {
    "listings": {},
    "tags": ["malware", "phishing"]
  },
  "user_analytics": {
    "search_count": 100,
    "fp_reports_count": 50,
    "malicious_reports_count": 10,
    "user_blacklist_count": 5,
    "user_whitelist_count": 20
  },
  "domain_rankings": {
    "Cisco": 123,
    "Tranco": 456,
    "Majestic": 789,
    "Open PageRank": 321,
    "Cloudflare": 654
  }
}
```

### Individual Responses by Parameter

#### Base Response (Always Included)
```json
{
  "domain": "example.com",
  "timestamp": "2022-01-01T00:00:00Z",
  "registration_date": "2020-01-01",
  "last_update_date": "2022-01-01",
  "expiration_date": "2023-01-01",
  "organization": "Example Organization",
  "registrar": "Example Registrar",
  "name_servers": ["ns1.example.com", "ns2.example.com"],
  "abuse_emails": ["abuse@example.com"]
}
```

#### SSL Details (If `ssl_details=True`)
```json
{
  "ssl_details": {
    "owner_org": "Example Organization",
    "owner_country": "US",
    "issuer_org": "Example Issuer",
    "issuer_country": "US",
    "serial_number": "1234567890",
    "version": "TLSv1.2",
    "valid_from": "2022-01-01",
    "valid_to": "2023-01-01",
    "fingerprint_sha256": "fingerprint123"
  }
}
```

#### User Analytics (If `user_analytics=True`)
```json
{
  "user_analytics": {
    "search_count": 100,
    "fp_reports_count": 50,
    "malicious_reports_count": 10,
    "user_blacklist_count": 5,
    "user_whitelist_count": 20
  }
}
```

#### Domain Rankings (If `rankings=True`)
```json
{
  "domain_rankings": {
    "Cisco": 123,
    "Tranco": 456,
    "Majestic": 789,
    "Open PageRank": 321,
    "Cloudflare": 654
  }
}
```

## Error Responses

| Status Code | Description |
|------------|-------------|
| `400`      | Bad request. Ensure required parameters are correctly formatted. |
| `401`      | Unauthorized. Invalid or missing API key. |
| `403`      | Forbidden. Access to the requested resource is denied. |
| `404`      | Domain not found. The requested domain does not exist. |
| `500`      | Internal Server Error. An unexpected error occurred on the server. |



# URL_API 

## Description
The **URL Information API** provides detailed insights about a given URL, including registration details, SSL certificate information, DNS records, user analytics, threat intelligence, sandbox analysis, and rankings.

## Endpoint

```
GET https://api.cybercheck360.com/v1/url/{{api_key}}/?url={url}&user_analytics={user_analytics}&sand_box={sand_box}&rankings={rankings}
```

## Query Parameters

| Parameter       | Type    | Required | Description |
|----------------|---------|----------|-------------|
| `url`         | string  | Yes      | The URL to retrieve details for (e.g., `https://www.example.com`). |
| `user_analytics` | boolean | No       | Set to `True` to include user analytics data in the response. Defaults to `False`. |
| `sand_box`    | boolean | No       | Set to `True` to include sandbox analysis results. Defaults to `False`. <br> *__Note__ : this can take longer to respond as it visits the webpage in realtime for analysis*|
| `rankings`     | boolean | No       | Set to `True` to include domain rankings from various sources. Defaults to `False`. |

## Sample Request

```http
GET https://api.cybercheck360.com/v1/url/{{api_key}}/?url=https://www.testsigma.com&user_analytics=True&kaavalan=True&sand_box=True&rankings=True
```

## Response

The API response includes multiple sections depending on the parameters enabled.

### Full Response (With All Parameters Enabled)

```json
{
  "url": "https://www.example.com",
  "domain": "testsigma.com",
  "registration_date": "2020-01-01",
  "last_update_date": "2022-01-01",
  "expiration_date": "2023-01-01",
  "organization": "Example Organization",
  "registrar": "Example Registrar",
  "name_servers": ["ns1.example.com", "ns2.example.com"],
  "abuse_emails": ["abuse@example.com"],
  "dns": { ... },
  "threat_intel": { ... },
  "user_analytics": { ... },
  "sand_box": { ... },
  "domain_rankings": { ... },
  "cybercheck360_feeds": { ... }
}
```

### Individual Responses by Parameter

#### Base Response (Always Included)
```json
{
  "url": "https://www.example.com",
  "domain": "example.com",
  "registration_date": "2020-01-01",
  "last_update_date": "2022-01-01",
  "expiration_date": "2023-01-01",
  "organization": "Example Organization",
  "registrar": "Example Registrar",
  "name_servers": ["ns1.example.com", "ns2.example.com"],
  "abuse_emails": ["abuse@example.com"]
}
```

#### User Analytics (If `user_analytics=True`)
```json
{
  "user_analytics": {
    "url_analytics": {
      "search_count": 100,
      "fp_reports_count": 50,
      "malicious_reports_count": 10,
      "user_blacklist_count": 5,
      "user_whitelist_count": 20
    },
    "domain_analytics": {
      "search_count": 150,
      "fp_reports_count": 70,
      "malicious_reports_count": 20,
      "user_blacklist_count": 8,
      "user_whitelist_count": 30
    }
  }
}
```

#### Threat Intelligence (If `kaavalan=True`)

[More Details](#threat-intelligence)

```json
{
  "threat_intel": {
    "listings": {},
    "tags": ["malware", "phishing"]
  }
}
```

#### Sandbox Analysis (If `sand_box=True`)
When enabled, the sandbox analysis captures:

- **Website Behavior**: Tracks cookies, scripts, and file downloads.
- **Indicators of Compromise (IOCs)**: Extracts malicious URLs, domains, IPs, and file hashes.
- **Network Connections**: Logs all outgoing requests made by the webpage.
- **Website Screenshot**: Captures a visual representation of the page.
- **SSL Certificate Details**: Provides certificate issuer and validity information.
- **Redirects**: Lists HTTP redirections during page load.
- **Unique Domains & IPs Contacted**: Identifies all external servers the page communicates with.

| Feature                          | Description                                                   |
|----------------------------------|---------------------------------------------------------------|
| **Website Behavior**             | Tracks cookies, scripts, and file downloads.                 |
| **Indicators of Compromise (IOCs)** | Extracts malicious URLs, domains, IPs, and file hashes.       |
| **Network Connections**          | Logs all outgoing requests made by the webpage.              |
| **Website Screenshot**           | Captures a visual representation of the page.                |
| **SSL Certificate Details**      | Provides certificate issuer and validity information.        |
| **Redirects**                    | Lists HTTP redirections encountered while loading the page.  |
| **Unique Domains & IPs Contacted** | Identifies all external servers the page communicates with.  |


```json
{
  "sand_box": {
    "site_screenshot": "image_url",
    "ssl_details": { ... },
    "redirects": [ ... ],
    "ip_address": "192.0.2.1",
    "behavior": { ... },
    "extracted_indicators": { ... }
  }
}
```

#### Domain Rankings (If `rankings=True`)
```json
{
  "domain_rankings": {
    "Cisco": { "rank": 123, "last_updated": "2023-01-01" },
    "Tranco": "456",
    "Majestic": "789",
    "Open PageRank": "321",
    "Cloudflare": "654"
  }
}
```

<!-- #### Cybercheck360 Feeds
```json
{
  "cybercheck360_feeds": {
    "confidence": "high",
    "category": "phishing",
    "tags": "malware, trojan",
    "verdict": "malicious"
  }
}
``` -->

## Error Responses

| Status Code | Description |
|------------|-------------|
| `400`      | Bad request. Ensure required parameters are correctly formatted. |
| `401`      | Unauthorized. Invalid or missing API key. |
| `403`      | Forbidden. Access to the requested resource is denied. |
| `404`      | URL not found. The requested URL does not exist. |
| `500`      | Internal Server Error. An unexpected error occurred on the server. |

