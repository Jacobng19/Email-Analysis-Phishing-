# Email Analysis (Phishing)

## Objective

The Email Analysis (Phishing) Lab project aims to conduct a comprehensive email analysis by identifying and mitigating phishing attempts. This is done through a detailed examination of email content, headers, and attachments, this hands-on experience was designed to deepen my understanding of threat detection, email analysis, and common phishing red flags.

### Skills Learned

- Following Playbook
- Incident Response
- URL Investigation
- IP Address Investigation
- IOCs

### Tools Used

- Windows Virtual Machine
- SPF Record Check
- Notepad ++
- Whois Lookup From DomainTools
- VirusTotal
- URL2PNG
  
## Email Investigation

### Part 1: Email Header

![Screenshot 2024-04-23 214808](https://github.com/Jacobng19/Email-Analysis-Phishing-/assets/167641578/f685c4f1-161e-40af-9250-06a23552cfc8)

*Ref 1: Email Header

- The first immediate suspension I see is that in the from section not only is the name "Amazon" spelled wrong but the domain isn't actually coming from Amazon. Clearly, they are trying to impersonate Amazon.

- The intended recipient of the email appears to only go to one user but it would still be important to verify only one user in the company was affected.

- The subject line does raise a concern to me as it implies some urgency on the recipient, although not always an immediate reason for phishing it is a common breadcrumb

### Part 2: Email Body

![Screenshot 2024-04-23 215631](https://github.com/Jacobng19/Email-Analysis-Phishing-/assets/167641578/b6a9fda2-8d16-4c77-af68-acf386212e45)
 
*Ref 2: Email Body

- The body of the email also contains some weird grammar mistakes that I wouldn't expect from a professional company like Amazon, this can be seen with the misuse of periods and capitalization.

- The introduction also is a concern for me as it doesn't address the user by their actual name, often large companies like Amazon will have the user's name already and address them by it. Although this isn't always the case, it does catch my eye.

- Again, the last sentence of the email implies a sense of urgency telling the recipient they may lose their account if they don't act within 72 hours. This is common among phishing attempts.

### Part 3: Email Footer

![Screenshot 2024-04-23 215701](https://github.com/Jacobng19/Email-Analysis-Phishing-/assets/167641578/793c3cb1-980d-4852-a6ee-11b707424d87)

*Ref 3: Email Footer

- I was immediately intrigued by the "Review Account" button, after safely copying the link and using the TotalVirus tool for URL scanning. The tool flagged that the URL was malicious and directed to a dangerous landing page. The "Amazon Support Team" link was also flagged and appeared to be malicious.

- I also used the URL2PNG tool to safely view the landing page and double-check that it did look malicious. Below in reference photo 4 you can see what the page looked like. I did note that the landing page's copyright still says 2017, definitely something Microsoft wouldn't miss.

![704673c1b1f8fe63ad174ddf24577468c8eff570](https://github.com/Jacobng19/Email-Analysis-Phishing-/assets/167641578/13103ce9-8421-45b3-8480-fda68c5838d4)

*Ref 4: Malicious URL

### Part 4: Sender Domain & IP Address

![Screenshot 2024-04-23 225311](https://github.com/Jacobng19/Email-Analysis-Phishing-/assets/167641578/cca9152b-23c8-44b7-83d1-ef739b25f34a)

*Ref 5: Received SPF

- I wanted to also check out more about the sender. I did this by two means, one by checking if the SPF had failed to see if that domain was a permitted sender but also by checking the sender's IP address. (sidenote: the spf did pass, the IP address and domain weren't flagged but this is mostly due to this being a test lab email and not a real phishing attempt)

- To verify the IP Address I used the Whois Lookup tool, which told me that the IP address was coming from Russia. You can see this below in reference photo 6.


![Screenshot 2024-04-23 215229](https://github.com/Jacobng19/Email-Analysis-Phishing-/assets/167641578/78c5b895-92bd-4088-9a9e-a3c6e65c4109)

*Ref 6: IP Address From Whois

### Part 5: Wrap-up

- Through this email analysis project, several red flags of a phishing attempt were identified and examined. These included discrepancies in the email header, grammar mistakes in the email body, suspicious URL elements in the email footer, and insights gained from investigating the sender's domain and IP address. By investigating each component of the email and utilizing various online tools for verification, a complete understanding of the potential threat was achieved.

(For reference this email was a lab that I found on Blue Team Labs Online)
