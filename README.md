# Email Analysis (Phishing)

## Objective

The Email Analysis (Phishing) Lab project aims to conduct a comprehensive email analysis by identifying and mitigating phishing attempts. This is done through a detailed examination of email content, headers, and attachments, this hands-on experience was designed to deepen my understanding of threat detection, email analysis, and common phishing red flags.

### Skills Learned

- Following Playbook
- Incident Response
- URL Investigation
- IP Address Investigation
- Common Red Flags

### Tools Used

- Windows Virtual Machine
- SPF Record Check
- Notepad ++
- Whois From DomainTools
- VirusTotal
- URL2PNG
  
## Steps

Step 1: Identification 

![Screenshot 2024-04-23 214808](https://github.com/Jacobng19/Email-Analysis-Phishing-/assets/167641578/f685c4f1-161e-40af-9250-06a23552cfc8)

*Ref 1: Email Header

-The first immediate suspension I see is that in the from section not only is the name "Amazon" spelled wrong but the domain isn't actually coming from Amazon. Clearly, they are trying to impersonate Amazon.

-The intended recipient of the email appears to only go to one user and therefore likely has only been sent to this one user.

-The subject line does raise a yellow flag to me as it implies some urgency on the receiver, although not always an immediate reason for phishing it is a common breadcrumb

![Screenshot 2024-04-23 215631](https://github.com/Jacobng19/Email-Analysis-Phishing-/assets/167641578/b6a9fda2-8d16-4c77-af68-acf386212e45)
 
*Ref 2: Email Body

-The body of the email also contains some weird grammar mistakes that I wouldn't expect from a professional company like Amazon, this can be seen with the misuse of periods and capitalization.

-The introduction also is a yellow flag for me as it doesn't address the user by their actual name, often in emails the company will have the user's name and address them by it. Although this isn't always the case, it does catch my eye.

-Again, the email is implying a sense of urgency telling the recipient they may lose their account if they don't act within 72 hours. This is common among phishing attempts.


![Screenshot 2024-04-23 215701](https://github.com/Jacobng19/Email-Analysis-Phishing-/assets/167641578/793c3cb1-980d-4852-a6ee-11b707424d87)

*Ref 3: Email Footer

-I was immediately intrigued by the "Review Account" button, after safely copying the link and using the TotalVirus tool for URL scanning. The tool flagged that the URL was malicious and directed to a dangerous landing page. The "Amazon Support Team" link was also flagged and appeared to be malicious.

-I also used the URL2PNG tool to safely view the landing page and double-check that it did look malicious. Below in reference photo 4 you can see what the page looked like.

![704673c1b1f8fe63ad174ddf24577468c8eff570](https://github.com/Jacobng19/Email-Analysis-Phishing-/assets/167641578/13103ce9-8421-45b3-8480-fda68c5838d4)

*Ref 4: Malicious URL



(For reference this email was a lab that I found on Blue Team Labs Online)
