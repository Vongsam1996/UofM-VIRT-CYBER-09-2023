Cybersecurity|
|Project 1 Technical Brief

Your Web Application
Enter the URL for the web application that you created:

|   |
|---|
|[<br><br>[https://samvsecurityportfolio.azurewebsites.net/](https://samvsecurityportfolio.azurewebsites.net/) <br><br>]|
 

Paste screenshots of your website created (Be sure to include your blog posts):

|   |
|---|
|[<br><br>![](https://lh7-us.googleusercontent.com/K7CkczCnyPA0xAOycTe_A0oEb1VXo1BZsQB6MTKgGWOlFrWiqYt4b1kfDRrimMc-tT3B5UktUkIq-GpYp-m38Op89F5wQ4xF5zjhRD5sgVM7637bwNk7TuYjHp857vgp01lu5oM0KKUu7SFyjOEY1GU)<br><br>![](https://lh7-us.googleusercontent.com/S4Viz4twqe9_blGnI9d-ii4qExA63IE-ZzNkjYhmR28-mkES0pd0PjuUicbIAVYrUvgi2_YX8ICeWAPSAyZJOzBZTPnHnAQRgiKUYzQUpC9Lq5XYO0mEdW09dPCYvIDAbLhuibCoafVnGoHcAJhZ7wA)<br><br>]|
## Day 1 Questions
### General Questions

1. What option did you select for your domain (Azure free domain,  GoDaddy domain)?

|   |
|---|
|[<br><br>Azure Free Domain<br><br>]|


2. What is your domain name?

|   |
|---|
|[<br><br>[samvsecurityportfolio.azurewebsites.net](https://samvsecurityportfolio.azurewebsites.net/)<br><br>]|

  

### Networking Questions 

1. What is the IP address of your webpage?  

|   |
|---|
|[<br><br>20.211.64.11<br><br>]|


2. What is the location (city, state, country) of your IP address?  

|   |
|---|
|[<br><br>Sydney, New South Wales , Australia, <br><br>]|

  

3. Run a DNS lookup on your website. What does the NS record show?

|   |
|---|
|[<br><br>![](https://lh7-us.googleusercontent.com/FAPTHR4WlDMPg16sOlN_mbL2A4AZ_IRR_Zc68s6Md9c0UPXnIdj7FSQZd4uSh0XvkJfIHNS-CWHdTkjqw9nCpRukNSSfbh-CTUHMddPSSuNPFpc-CwZ_BKuacq4EB3PC0h-RXAuBDu87jQqR2meF_E4)<br><br>- Ns4-224.azure-dns.info<br>    <br><br>  <br><br>Nslookup <br><br>  <br><br>]|

  

### Web Development Questions

1. When creating your web app, you selected a runtime stack.  What was it? Does it work on the front end or the back end? 

|   |
|---|
|[<br><br>PHP 8.2, back end<br><br>]|

2. Inside the /var/www/html directory, there was another directory called assets. Explain what was inside that directory.

|   |
|---|
|[<br><br>Instead this directory, I posted my HTML back up files that has control of my web browser<br><br>]|

  

3. Consider your response to the above question. Does this work with the front end or back end?

|   |
|---|
|[<br><br>Front end<br><br>]|

  
  

## Day 2 Questions

### Cloud Questions

1. What is a cloud tenant?  

|   |
|---|
|[<br><br>Cloud tenant provides consumers to interact with cloud services by a cloud service provider. In a sense, Cloud tenant would be individuals who wants to interact with the data/ website<br><br>]|

  
2. Why would an access policy be important on a key vault?  

|   |
|---|
|[<br><br>Access policy is important on a key vault because it grants security protocol to passwords. <br><br>]|

3. Within the key vault, what are the differences between keys, secrets, and certificates?

|   |
|---|
|[<br><br>Keys <br><br>- Keys are used for encryptions, decryptions, and signatures <br>    <br>- Symmetric or asymmetric<br>    <br><br>- Symmetric keys: Use the same key for both encryption and decryption <br>    <br>- Asymmetric keys: Uses of public and private key <br>    <br><br>  <br><br>Secret<br><br>- Protection of sensitive information <br>    <br><br>- Ie: Passwords and API keys<br>    <br><br>- It is corresponds with resrouces<br>    <br><br>  <br><br>Certification<br><br>- Contains public key and information about the entity associated with the key <br>    <br>- Many used by HTTPs to establish connection between client and server<br>    <br>- Cryptographic connections<br>    <br><br>]|
### Cryptography Questions
1. What are the advantages of a self-signed certificate?

|   |
|---|
|[<br><br>1. Quick Set-up<br>    <br>2. Low cost<br>    <br>3. Can be encrypted with HTTPS<br>    <br><br>]|

2. What are the disadvantages of a self-signed certificate?

|   |
|---|
|[<br><br>1. Not as credible because lack of double authorization <br>    <br>2. Not many flexibility <br>    <br>3. Private key is compromised, then issue will arise with communicating with the user and systems <br>    <br>4. More vulnerable to attacks if not secure properly <br>    <br><br>]|

3. What is a wildcard certificate?

|   |
|---|
|[<br><br>Wildcard certification are designed to secure multiple domain and subdomain with a single certificate<br><br>- When buying a Global certificates - You will be buying multiple certifications <br>    <br><br>- Ie. Subscripting Microsoft Office <br>    <br><br>- Excel <br>    <br>- Powerpoint <br>    <br>- Etc. <br>    <br><br>]|


4. When binding a certificate to your website, Azure only provides TLS versions 1.0, 1.1, and 1.2.  Explain why SSL 3.0 isn’t provided.

|   |
|---|
|[<br><br>- SSL 3.0 is more vulnerable than TLS 1.0, 1.1, amd 1.2 <br>    <br>- Webrowsers removed support for SSL 3.0 <br>    <br>- SSL 3.0 is outdated <br>    <br><br>]|


5. After completing the Day 2 activities, view your SSL certificate and answer the following questions:

1. Is your browser returning an error for your SSL certificate? Why or why not?

|   |
|---|
|[<br><br>No because we set up Azure to included SSL certification<br><br>]|
 

2. What is the validity of your certificate (date range)?

|   |
|---|
|[<br><br>  <br><br>Issued On<br><br>Wednesday, November 29, 2023 at 2:34:04 PM<br><br>Expires On<br><br>Friday, November 28, 2025 at 2:34:04 PM<br><br>]|

  
3. Do you have an intermediate certificate? If so, what is it?

|   |
|---|
|[<br><br>Yes, Microsoft Azure TSL Issuing Ca 02<br><br>]|

  

4. Do you have a root certificate? If so, what is it?

|   |
|---|
|[<br><br>Yes DigitCert Global Root <br><br>]|

  

5. Does your browser have the root certificate in its root store?

|   |
|---|
|[<br><br>Yes<br><br>]|

  

6. List one other root CA in your browser’s root store.

|   |
|---|
|[<br><br>1. Go Daddy Root Certificate <br>    <br><br>]|

  
  

## Day 3 Questions
### Cloud Security Questions 

1. What are the similarities and differences between Azure Web Application Gateway and Azure Front Door?

|   |
|---|
|[<br><br>Similarity:<br><br>Azure Front door and Azure application gateway are both load balancers for HTTP/HTTPs <br><br>  <br><br>Difference: <br><br>Front Door: Global Service that distributes request across regions<br><br>Application Gateway: Regional service that balancer request within regions <br><br>Duongau. “Azure Front Door - Frequently Asked Questions.” Azure Front Door - Frequently Asked Questions \| Microsoft Learn, learn.microsoft.com/en-us/azure/frontdoor/front-door-faq. Accessed 18 Dec. 2023.<br><br>]|

2. A feature of the Web Application Gateway and Front Door is “SSL Offloading.” What is SSL offloading? What are its benefits?

|   |
|---|
|[<br><br>SSL offloading handles encryption/decryption process on separate devices so performance for web server should not be affected <br><br>- Note: Idea of SSL is to encrypt operation anywhere but on the web server <br>    <br><br>on, Posted, et al. “Benefits of Offloading SSL (Certs) on F5 Devices, and How to Automate It.” AppViewX, 24 Mar. 2022, [www.appviewx.com/blogs/the-benefits-of-offloading-ssl-certs-on-f5-devices-and-how-to-automate-it/#:~:text=SSL%20offloading%20takes%20care%20of,than%20on%20the%20web%20server](http://www.appviewx.com/blogs/the-benefits-of-offloading-ssl-certs-on-f5-devices-and-how-to-automate-it/#:~:text=SSL%20offloading%20takes%20care%20of,than%20on%20the%20web%20server). <br><br>  <br><br>]|

  

3. What OSI layer does a WAF work on?

|   |
|---|
|[<br><br>AWF - Azure web application firewall works on layer 7 (application layer)<br><br>]|

  

4. Select one of the WAF managed rules (e.g., directory traversal, SQL injection, etc.), and define it.

|   |
|---|
|[<br><br>SQL injection is malicious SQL code for backend database manipulation to access private/secure information that is for the admin and not the users/customers<br><br>- In-band SQLi<br>    <br><br>- Error-based SQLi - Any access to certain data, produces an error message <br>    <br>- Union-based SQLi - fuse multiple select statement generated by database to get a single HTTP response <br>    <br><br>  <br><br>- Inferential (Blind) SQLi - <br>    <br><br>- Boolean - Sending SQL Query to database prompting the application to return a result <br>    <br><br>- True or false <br>    <br>- If they have access to root or admin privilege<br>    <br><br>- Time-based - Attacks Database request <br>    <br><br>- IE: DoS - Deny of Service attack <br>    <br><br>“What Is SQL Injection: SQLI Attack Example & Prevention Methods: Imperva.” Learning Center, 14 Mar. 2023, www.imperva.com/learn/application-security/sql-injection-sqli/. <br><br>  <br>  <br><br>]|

  
5. Consider the rule that you selected. Could your website (as it is currently designed) be impacted by this vulnerability if Front Door wasn’t enabled? Why or why not?  

|   |
|---|
|[<br><br>Yes, because restricting front door will allow vulnerability in the front end <br><br>- This will allow SQL injections and other vulnerability from accessing the website’s information  <br>    <br><br>]|


6. Hypothetically, say that you create a custom WAF rule to block all traffic from Canada. Does that mean that anyone who resides in Canada would not be able to access your website? Why or why not?
  
No, because, Custom WSF blocks any IP address from canada
- If they are from Canada and they travel to a different location 
	- They will still be blocked even though they are outside of canada 
- VPN is a loophole that can mask their IP address and redirect their IP address to a different location 
	- The site will read the TCP as the chosen Ip address instead of the canada Ip Address]

  

7. Include screenshots below to demonstrate that your web app has the following: 

1. Azure Front Door enabled
 

|   |
|---|
|[<br><br>![](https://lh7-us.googleusercontent.com/Brt_54YUiWZms8r0R2N6kEKPhvQi46_RHyBvY7DON2myhLamI6s02RTwoO7K1eVswzxv5Qic_4-IYGgtVSAnetCAoNINaAMGaQJjVPTzuSBgry8CpPlTeHWyMuSALMc-gDPHZZUbadQSCt5R-nEV1J0)<br><br>]|

  
2. A WAF custom rule 

|   |
|---|
|[<br><br>![](https://lh7-us.googleusercontent.com/E6rpab8PUYyuoueyOg2DkVfahqsMENxEPYr4WzLE96l8GwfLloZSQtrU6u1UBehZr0ynwFwJ4_6rIYa1VWfdGMRK6UE-YBd4AQrJC46LpsfFW-jlmXZn2CRRpJjd21vpuWIT4-H_YyqhhsWYK9I6BUM)<br><br>If not <br><br>- United states, Canada, Austria <br>    <br><br>![](https://lh7-us.googleusercontent.com/V50ss-4_S0p0RpF0_XRjq8ktE3rJkW_sXKiEYFpBQ6w1SdyfXtn7rXKBdxUzYodmJMMEv4W5LWH3I8j-jXlRC1Cuxu9rim6pyZhKQS9l8vkg96KqvmeUlB1CmwRcp8Emqvp3K_cnRI8HcXI3QCUi9E0)<br><br>  <br><br>Note: This reject any connections other than United states, canada, Austria<br><br>]|

## Disclaimer on Future Charges 
 

Please type “YES” after one of the following options:

- Maintaining website after project conclusion: I am aware that I am responsible for any charges that I incur by maintaining my website. I have reviewed the [guidance](https://docs.google.com/document/d/1ZzC4oTJFdlkkeWuzuJAyVSqtDFbuAWilmwXg8PZgzMs/edit) for minimizing costs and monitoring Azure charges.
	- Yes

- Disabling website after project conclusion: I am aware that I am responsible for deleting all of my project resources as soon as I have gathered all of my web application screen shots and completed this document.
	- Yes