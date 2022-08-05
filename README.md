# Cyber-Portfolio
Collection of Cybersecurity related projects to showcase to potential employers.

Vulnerability Management:

Vulnerability management is the continual assessment of assets, discovery of vulnerabilites, remediation of vulnerabilites to an accepted risk level, and repetition of that process for as long as the business is in operation.

Goals of the project:  
1.  Gain experience instaling and configuring Nessus Essentials to perform credentialed vulnerability scans against a Windows 10 host.  
2.  Gain experience executing vulnerability management functions on a sandbox network: Discover, Prioritise, Assess, Report, Remediate, and Verify.  
3.  Gain experience conducting a vulnerability assessment with Nessus and remediating the discovered vulnerabilities.


There were four scans performed as part of this project:  
1.  Non-credentialed scan.  
2.  Credentialed scan with the Windows user's credentials.  
3.  Credentialed scan after the installation of legacy software.  
4.  Credentialed scan to verify remediation of vulnerabilities.  

Scan 1  
A non-credentialed scan to gain an understanding of what a basic network scan would deliver.  The scan itself was performed after a fresh installation of Windows 10.  The installation also had no license key provided.  The image below showcases that most of the detected vulnerabilities were merely informational and not necessarily something to consider remediating immediately.  The only exception was the lone medium risk at the top which centred around SMB signing.
![image](https://user-images.githubusercontent.com/109834780/181453006-bf3a7506-7fbe-4fbc-95f5-e8c851878e38.png)

Scan 2  
A credentialed scan was performed to gain an understanding of a credentialed scan would deliver.  The option to provide credentials on Nessus only allows either SSH or Windows credentials to be offered.  Since the user on the sandbox network is also the administrative user, the scan was performed at an administration access level.  It should be noted that for Windows vulnerability scanning; Nessus requires administration level access to perform a credentialed scan.
![image](https://user-images.githubusercontent.com/109834780/181453632-70fdd6d2-4c38-4de1-b485-d9f010b8a1e7.png)

Scan 3  
Scan was performed after the installation of legacy software onto the VM.  In this case, it was Mozilla Firefox v. 3.6.12.  The purpose behind this scan is to gain an understanding of what to expect if faced with an extremely vulnerable system as well as look over the suggested remediations as provided by Nessus.  In the image below, you'll see that Firefox is listed as a critical vulnerability.  The remediations that Nessus recommended for this scan was the update Firefox as well as update various aspects of Windows.
![Legacy Vulnerabilities](https://user-images.githubusercontent.com/109834780/182989768-df726a45-c6c4-4e11-87d1-8a2f9494e73b.png)

Scan 4  
This scan was performed after remediation activities were executed to secure the Windows user.  The scan was to validate that the vulnerabilities in question were remediated.  The steps taken to remediate the majority of the vulnerabilities included removing Firefox from the system as well as running Windows Update until no more updates were detected.  The image below you can see that the Firefox entry is removed as well as a good chunk of Windows vulnerabilities.  The bulk of the remaining vulnerabilities centred around Microsoft Edge and its remediation centred around simply updating Edge.
![image](https://user-images.githubusercontent.com/109834780/181454192-b0fc5fa0-35fe-4bf6-aa5e-2d0bc215eb1e.png)
