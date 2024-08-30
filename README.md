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
	- Private List(*A List that contains indicators that are private only to you and can be shared to other cybercehck360 users*)
	- Public List(*A List that is accessible to anyone who uses Cybercheck360.com, this is athe best way to share to community and showcase your best efforts of your Threat Hunting and Users can Subscribe to Make better use of it*)
3. **Integartions**
	- [AbuseIPDB](#abuseipdb-integration)
	- [VirusTotal](#virustotal-integration)
	- [AlienVault OTX](#alienvault-otx-integration)
 4. **Browser Extension**
	- [Chrome WebStore](https://chromewebstore.google.com/detail/cybercheck360/kokegkiimgecajiaaefcoknbdaaddpdd)
	- [Firefox add-ons](https://addons.mozilla.org/en-US/firefox/addon/cybercheck360/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)

## Search IOCs 
This section is designed to help you search for indicators such as IP addresses, domains, and URLs, and even validate SMS messages containing links to check if they are legitimate. You can search across multiple open-source threat intelligence feeds and benefit from AI-powered insights that enhance the accuracy of the information gathered. 

We are constantly working on bringing more trusted feeds that are widely used by the security community. ***Special thanks to all the open-source threat intelligence feed providers for their invaluable support to the community.*** If you feel any feed is missing and it’s open-source, feel free to submit a feature request to add the feed using the **chat** icon at the bottom right.

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

### Methods for Collecting Threat Intelligence Feeds

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




If you notice any issues or have suggestions for improvements, please reach out. We're always ready to review and update our data to ensure it meets your needs.
## **AbuseIPDB Integration**
This Section should explain who is AbuseIPDB and how to Enable AbuseIPDB and show screenshot of how results will look like when enabled. 

## **Virustotal Integration**
This Section should explain who is Virustotal and how to Enable Virustotal and show screenshot of how results will look like when enabled. 

## **AlienVault OTX Integration**
This Section should explain who is AlienVault and how to Enable AlienVault and show screenshot of how results will look like when enabled.

# Getting Started with Create React App


This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).


## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `yarn build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
