<div style="display: flex; justify-content: center;">
  <img src="https://kaavalanpublic.s3.eu-west-1.amazonaws.com/logos/Cybercheck360_Logo_Blue_500.png" style="width: auto; height: 100px;" alt="CyberCheck360.com Logo"/>
</div>

  <!-- ![CyberCheck360.com Logo](https://kaavalanpublic.s3.eu-west-1.amazonaws.com/logos/Cybercheck360_Logo_Blue_500.png "CyberCheck360 Powered by Kaavalan") -->

**Cybercheck360.com** is a cutting-edge SaaS-based Threat Intelligence Platform developed by **Kaavalan Limited**. Designed to empower security professionals, **Cybercheck360** offers advanced threat-hunting capabilities from a single, unified interface, integrating data from multiple vendors to enhance your security operations.

But we're not just for security experts. **Cybercheck360** also caters to everyday users who may be receiving suspicious SMS messages from unknown numbers. Curious whether that unexpected text is legitimate? Our platform leverages AI and sophisticated URL analysis techniques to validate the authenticity of SMS messages, helping users stay safe in the digital world.

We aggregate threat intelligence from over 100+ open-source feeds, ensuring a robust and dynamic database that evolves with emerging threats. A special thanks to the open-source community for their invaluable contributions, making the internet safer for everyone.

For personal use, our platform is free, offering essential tools for those with light usage needs. However, for users requiring advanced features and curated threat intelligence feeds, we offer a commercial plan. This premium option combines the power of both Premium and Open Source feeds to deliver a superior threat intelligence experience.

Additionally, Cybercheck360 allows registered users to integrate their own API keys from third-party vendors, providing a tailored solution that enables informed decision-making—all from one centralized dashboard.

**Cybercheck360** is a proud product of **Kaavalan Limited**, reflecting our commitment to innovation and security in the digital age.

# Features
1. [**Search IOCs**](#search-iocs) with 100+ Threat Intelligence Feeds
	- IP Lookup
	- Bulk IP Lookup
	- URL Lookup with Screenshot and Lot more
	- Domain Lookup
 	- SMS Validation
2. **IOCs List**
	- Private List
	- Public List
3. **Integartions**
	- [AbuseIPDB](#abuseipdb-integration)
	- [VirusTotal](#virustotal-integration)
	- [OTX](#otx-integration)
 4. **Browser Extension**
	- [Chrome WebStore](https://chromewebstore.google.com/detail/cybercheck360/kokegkiimgecajiaaefcoknbdaaddpdd)
	- [Firefox add-ons](https://addons.mozilla.org/en-US/firefox/addon/cybercheck360/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)
5. **Upcoming Features**
   	- API Functionality
   	- External Dynamic Lists
   	- Highly Reliable Kaavalan's Threat Intelligence Feed
   	- Automated Advisory Reports
   	- Automated Threat Detection and Blocking Engine
   	
## Search IOCs 
This section is designed to help you search for indicators such as IP addresses, domains, and URLs, and even validate SMS messages containing links to check if they are legitimate. You can search across multiple open-source threat intelligence feeds and benefit from AI-powered insights that enhance the accuracy of the information gathered. 

We are constantly working on bringing more trusted feeds that are widely used by the security community. ***Special thanks to all the open-source threat intelligence feed providers for their invaluable support to the community.*** If you feel any feed is missing and it’s open-source, feel free to submit a feature request to add the feed using the **chat** icon at the bottom right.
<div style="display: flex; justify-content: center;">
  <img src="https://kaavalanpublic.s3.eu-west-1.amazonaws.com/PicsforDocs/IP_Search_Basic_Top+Screen.png" alt="CyberCheck360.com IP Lookup Results"/>
</div>


### Catgeories
	> Malware
Malware is harmful software designed to damage or exploit systems, networks, or devices. We categorize any IP, domain, or URL involved in malware-related activities under the "Malware" category. 
### 
	> Phishing
Phishing involves deceptive practices where attackers try to trick individuals into revealing sensitive information, such as login credentials or personal details, by pretending to be trustworthy entities. Any IP, domain, or URL involved in phishing activities is categorized under the "Phishing" category.
### 
	> Botnet
Botnets consist of networks of compromised computers that are controlled remotely to perform malicious activities, often without the users' knowledge. IPs involved in **scanning** or exhibiting **bot-like behaviors** are categorized under the "Botnet" category. 
### 
	> Anonymizers
Anonymizers are services or tools that protect users' privacy by masking their IP addresses or routing their traffic through multiple servers. This category includes proxies, VPNs, and the Tor network, which anonymizes internet activity by routing traffic through a distributed network of relays. IPs and domains associated with these services are categorized under "Anonymizers" feeds. 
### 
	> Exploits
Exploits are methods used to take advantage of vulnerabilities in systems, applications, or networks to gain unauthorized access or cause damage. These vulnerabilities can exist in software, hardware, or configurations, and exploits are designed to exploit these weaknesses to compromise security.
### 
	> Spam
Spam refers to unsolicited and often irrelevant or inappropriate messages sent over the internet, typically in bulk, to promote products or services, or simply to flood inboxes. These messages can appear in various forms, including emails, comments, or social media posts, and are often used to distribute malicious content or scams. Many of the spam feeds we use are based on an older technology known as DNS-based Blackhole Lists (DNSBLs). 

`If you notice any issues or have suggestions for improvements, please reach out. We're always ready to review and update our data to ensure it meets your needs.`
<!--### Methods for Collecting Threat Intelligence Feeds

[**API Method**]
  We integrate with various APIs provided by threat intelligence services. These APIs deliver real-time data about threats, including IP addresses, domains, and URLs associated with malicious activities. This method allows us to obtain up-to-date and accurate threat information directly from the source.

[**Crawling Files**]
  Our system performs automated crawling of publicly available threat intelligence files. These files are often hosted on security community websites or by organizations that share their findings. By regularly scanning and downloading these files, we can incorporate new threat data into our feeds.

#### [**Crawling RSS Feeds**]
  We monitor RSS feeds from reputable security blogs and threat intelligence platforms. These feeds provide timely updates on the latest security threats and vulnerabilities. By crawling these feeds, we ensure that our threat intelligence is current and relevant.

#### **Manual Extraction from Reports**  
  We manually review and extract data from security reports published by experts and organizations. This method allows us to gather detailed and context-rich information about threats that might not be available through automated methods.

	- **DNSBL (DNS-based Blackhole Lists)**  
  DNSBLs are a traditional technology used to block or filter spam and malicious traffic by checking IP addresses against a blacklist. While not as commonly used today due to advancements in threat detection, DNSBLs still provide valuable data for identifying known sources of spam and malicious activities.
-->

## Lists (IOC Lists)
Our Lists organized into two main types: Public and Private. Private and Public List can be categorised into Malware, Botnet, Exploit, Spam, Phishing, Anonymizers, and Whitelist. These categories are designed to ensure clarity and prevent excessive fragmentation into subcategories, allowing you to quickly access the most pertinent data.

###
	> Public
A Public List conatins indicators that are publicly accessible to any of the Cybercheck360.com users. It has ssome minor configuration to make users to Subscribe to view the Indicators or everyone can View the Indicators. Public lists are the best way to share to community and showcase your best efforts of your Threat Hunting and Users can Subscribe to Make better use of it. Lists can hold a maximum on 10,000 indicators.

`Users can report false positives, and these reports are visible to everyone. A high number of false positive reports can affect the trustworthiness of your list, potentially leading to reduced interest from users.`

###
	> Private
A List that contains indicators that are private only to you and thelist can be shared to other cybercheck360 user and the user you share this list with gets an admin permission to update Indicators on the List and also gets privillege to report to any False positive reports on the List.


## Integrations
Integrations are essential tools that allow you to seamlessly connect **Cybercheck360** with your trusted **threat intelligence feeds**. By integrating these feeds, you can consolidate diverse threat data sources into a single, unified dashboard improving efficiency and decision making. With a comprehensive view of your threat landscape, you can better manage and respond to potential threats, making your security operations more effective.

### [**AbuseIPDB Integration**]
[AbuseIPDB's](https://www.abuseipdb.com/about.html) mission is to provide an easy way for sysadmins to both report malicious IP addresses, and gain access to a crowdsourced list of bad IPs before they've even had the chance to attack your infrastructure.

#### How to Enable AbuseIPDB Integration with Cybercheck360
##### **Steps**:
1. Login to CyberCheck360.com
2. Naviagte to "Integtaions" from the Top Nav Bar
3. Naviagte to "Add Integations"
4. Expland "AbuseIPDB" Integartion.
5. Accept the submision of sending Searched indicators to AbuseIPDB (Check the Checkbox)
6. Click on "Save and Enable"

#### Sample Result Screenshot
<div style="display: flex; justify-content: center;">
  <img src="https://kaavalanpublic.s3.eu-west-1.amazonaws.com/PicsforDocs/AbuseIPDB_Sample+Response2.png" style="width: 600px; height: auto;" alt="CyberCheck360.com Results for AbuseIPDB Integration"/>
</div>



### [**Virustotal Integration**]
[Virus Total](https://www.virustotal.com/gui/home/upload) is an online service that analyzes suspicious files and URLs to detect types of malware and malicious content using antivirus engines and website scanners. It provides an API that allows users to access the information generated by VirusTotal.

#### How to Enable VirusTotal Integration with Cybercheck360
Before you begin configuring the Integration you may need to register with Virustotal and Obtain an API Key that will be used in the Later Steps in configuring the integration. 
##### **Steps**:
1. Login to CyberCheck360.com
2. Naviagte to "Integtaions" from the Top Nav Bar
3. Naviagte to "Add Integations"
4. Expland "VirusTotal" Integartion.
5. Select the IOC Types you want the Virustotal Integration to be used when you search an IOC in CyberCheck360.
6. Provide a "Reference Name" an Unique Name that can help you identify if you create multiple Integrations for the same Integration Provider.
7. Provide API Key from "Virustotal". Check this [link](https://docs.virustotal.com/reference/authentication) for more details.
8. Set RateLimits if required, if not leave it to default.
9. Accept the submision of sending Searched indicators to VirusTotal (Check the Checkbox)
10. Save Data for re-lookup 7 Days - This option will cache the result for you for 7 days.

    <div style="display: flex; margin: 0; align-items: center;">
    <img src="https://kaavalanpublic.s3.eu-west-1.amazonaws.com/PicsforDocs/cached_icon.png" alt="CyberCheck360.com Cache" style="margin-right: 3px;"/>
    <p style="margin: 0;">This represents the result is from cache.</p>
    </div>

    `For example, if you search for an indicator on Monday at 10 AM, we will cache the response from VirusTotal. For the next 7 days, until the following Monday at 9:59 AM, we will return the cached result for subsequent searches of the same indicator. This approach helps prevent overuse of your valuable API subscription.`

11. Click on "Save and Enable"

#### Sample Result Screenshot
<div style="display: flex; justify-content: center;">
  <img src="https://kaavalanpublic.s3.eu-west-1.amazonaws.com/PicsforDocs/VT_Sample+Response.png" style="width: auto; height: 150px;" alt="CyberCheck360.com Results for Virustotal Integration"/>
</div>



### [**OTX Integration**]
[OTX](https://otx.alienvault.com/) Open Threat Exchange is the neighborhood watch of the global intelligence community. It enables private companies, independent security researchers, and government agencies to openly collaborate and share the latest information about emerging threats, attack methods, and malicious actors, promoting greater security across the entire community.

#### How to Enable OTX Integration with Cybercheck360
Before you begin configuring the Integration you may need to signup with OTX and Obtain an API Key that will be used in the Later Steps in configuring the integration. 
Once you sign up, follow the steps in the below screnshot to get the API Key
<div style="display: flex; justify-content: center;">
  <img src="https://kaavalanpublic.s3.eu-west-1.amazonaws.com/PicsforDocs/OTX_API_KEY_Generation.png" alt="Where to get OTX API Key"/>
</div>

##### **Steps**:
1. Login to CyberCheck360.com
2. Naviagte to "Integtaions" from the Top Nav Bar
3. Naviagte to "Add Integations"
4. Expland "OTX" Integartion.
5. Select the IOC Types you want the OTX Integration to be used when you search an IOC in CyberCheck360.
6. Provide a "Reference Name" an Unique Name that can help you identify if you create multiple Integrations for the same Integration Provider.
7. Provide API Key from "OTX".
8. Set RateLimits if required, if not leave it to default.
9. Accept the submision of sending Searched indicators to OTX (Check the Checkbox)
10. Save Data for re-lookup 7 Days - This option will cache the result for you 7 days.
	
 	<div style="display: flex; margin: 0; align-items: center;">
	<img src="https://kaavalanpublic.s3.eu-west-1.amazonaws.com/PicsforDocs/cached_icon.png" alt="CyberCheck360.com Cache" style="margin-right: 3px;"/>
	<p style="margin: 0;">This represents the result is from cache.</p>
	</div>
	
 	`For example, if you search for an indicator on Monday at 10 AM, we will cache the response from OTX. For the next 7 days, until the following Monday at 9:59 AM, we will return the cached result for subsequent searches of the same indicator. This approach helps prevent overuse of your valuable API subscription.`

12. Click on "Save and Enable"

#### Sample Result Screenshot
<div style="display: flex; justify-content: center;">
  <img src="https://kaavalanpublic.s3.eu-west-1.amazonaws.com/PicsforDocs/OTX+Sample+Response.png" style="width: auto; height: 150px;" alt="CyberCheck360.com Results for Virustotal Integration"/>
</div>


## Browser Extentions

We have passionately designed our Extention  to easily perform IP lookup, URL lookup, Domain lookup, and Blacklist lookup with CyberCheck360's advanced Threat Intelligence platform. By simply highlighting text, you can instantly extract and analyze IP addresses, domains, and URLs for rapid threat intelligence and insights. The platform supports informed cybersecurity decisions by integrating various vendors, allowing users to bring their own API keys and conduct extensive searches across multiple sources within a single TIP. Additionally, users can configure which websites have the URL scanner feature enabled. All settings and integrations are fully customizable in the extension's Options page, ensuring seamless threat lookup and intelligence gathering.

We've made every effort to ensure that all configurations are self-explanatory. However, if you need further guidance, we've also prepared a comprehensive training video that walks you through the process step by step. Feel free to check it out using the link provided.

Our extension is currently available on:

<!--- [_**Google Chrome**_](https://chromewebstore.google.com/detail/cybercheck360/kokegkiimgecajiaaefcoknbdaaddpdd)
- [_**Mozilla Firefox**_](https://addons.mozilla.org/en-US/firefox/addon/cybercheck360/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)-->


- <a href="https://chromewebstore.google.com/detail/cybercheck360/kokegkiimgecajiaaefcoknbdaaddpdd" target="_blank"><b><i>Google Chrome</i></b></a>
- <a href="https://addons.mozilla.org/en-US/firefox/addon/cybercheck360/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search" target="_blank"><b><i>Mozilla Firefox</i></b></a>

We’re excited to announce that we're working on expanding support to:

- Other web browsers
- Email clients
Stay tuned for updates!

**Upcoming Features**
   	
- _**API Functionality**_
API is always a key functionaly for any Saas product and we are also working on with it and should be released very soon helping you lookup indicators at scall from any of your prefered automation platforms. 
   	
- _**External Dynamic Lists**_
Unlock the power of your Private and Public IOCs with Cybercheck360.com's advanced integration features. Our platform allows you to effortlessly consume IOC lists through public endpoints, making it easy to connect directly with your firewall or any text file consumers like automation platforms and scripts. With enhanced granular control, you can customize your exports by implementing custom whitelisting, domain ranking exclusions, filtering based on recent searches, scores, and categories, and much more.

Ensure the security of your data with IP-based ACL controls, limiting access to your hosted lists and preventing unauthorized users from viewing your private IOCs. Cybercheck360.com is meticulously designed to provide you with the control you need, allowing direct use of exported data without requiring additional filtering platforms. Experience secure, hassle-free IOC management tailored to your needs.
   	
- _**Highly Reliable Kaavalan's Threat Intelligence Feed**_
We are excited to announce the development of our very own threat intelligence feed, meticulously curated from a wide range of sources. This includes multiple open-source feeds, commercial data streams, and exclusive insights gathered through our in-house honeypot detection platform, deployed across multiple regions.

Our feed is designed with reliability as a core principle, ensuring a very low false positive rate. You can trust this manually curated intelligence for direct blocking and informed decision-making. Stay tuned for a new level of threat intelligence that will elevate your cybersecurity strategy!
   	
- _**Automated Advisory Reports**_
We’re thrilled to announce that we’re working on a cutting-edge feature that will revolutionize how you stay ahead of the latest cybersecurity threats. Our new vulnerability advisory service is coming soon, and it will offer:

**Early Alerts:** Get notified about newly discovered vulnerabilities as soon as they are published.
**Comprehensive Guidance:** Receive detailed steps to mitigate risks and prevent exploitation.
**Indicators of Compromise:** Access critical indicators related to each vulnerability to help you identify and respond to threats swiftly.
Our team is meticulously curating information from top security blogs and news sources to ensure you get the most relevant and timely updates without the hassle of searching through multiple sources.

Stay tuned for the launch of this valuable service, designed to keep you informed and secure with minimal effort. We can’t wait to help you stay one step ahead of emerging threats!
   	
- _**Automated Threat Detection and Blocking Engine**_
We’re excited to announce our new cloud-based log aggregation system, specifically designed to enhance your network security by focusing on network logs.

Key Features:

**Centralized Log Collection:** Collect and aggregate network logs from various sources for a comprehensive view of your network activity.
**Automated Threat Detection:** Our system scans your network traffic against millions of suspicious indicators, automatically identifying potential threats.
**Real-Time Alerts:** Receive immediate notifications about detected threats and actionable suggestions for blocking them.
Network logs play a crucial role in identifying and preventing malicious activities. Our system ensures you stay ahead of threats with minimal manual effort.

