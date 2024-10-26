# Building a SIEM

## Objective

This project aims to develop an open-source Security Information and Event Management (SIEM) solution that efficiently collects, analyzes, and correlates security event data from diverse resources, enabling enhanced threat detection, incident response, and overall security posture. This project seeks to deliver flexible components, thorough documentation, and user-friendly interfaces to assist both beginner and advanced security professionals.

### Skills Learned
[Bullet Points - Remove this afterwards]

- Building a SIEM
- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
[Bullet Points - Remove this afterwards]

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps

1.	Head to splunk.com
2.	Click “products” above
3.	Underneath “Platform” click “Splunk Enterprise”
4.	Click “Free Trial” underneath Splunk Enterprise.
5.	After signing up and verifying email, log in.
6.	A landing page will appear to install your package.

![image](https://github.com/user-attachments/assets/90bcc22e-0b10-4ffc-9a73-e01bba519046)




8. For the Linux OS click "Copy wget link" for the ".deb" package.
 
![image](https://github.com/user-attachments/assets/71fa5e98-4f97-48fc-92ef-4e76e1e67fb5)

![image](https://github.com/user-attachments/assets/f03e0a97-744c-4346-8ecd-d91ff21aaccb)



9. Paste the copied wget command into the VM.

![image](https://github.com/user-attachments/assets/da396f25-74d8-44f3-8fd8-8ce135846260)




10. In the VM enter "ls" to verify you have your ".deb" package file.

![image](https://github.com/user-attachments/assets/6c195896-5bc8-42f2-b3f3-f5ef31ba0f6e)




11. Enter the command "sudo apt-get update" to ensure you have the latest package.
12. Enter the command "apt-get install curl" to be able to be able to install deb. package.
13. Copy the ".deb" file to download the package.
14. Enter this command in the VM "sudo dpkg -i splunk-9.3.1-0b8d769cb912-linux-2.6-amd64.deb" (the .deb file you have on your vm).

![image](https://github.com/user-attachments/assets/fe18dfcd-cd23-4896-a207-57e78be5c856)




15. Enter the command to enable start at boot.
17. This will also prompt the Splunk license agreement .
16. Enter "y" to agree

![image](https://github.com/user-attachments/assets/e8b46275-a67c-4998-bb5e-85cb35c83320)

![image](https://github.com/user-attachments/assets/71467f21-a47d-4d59-98f2-1c9ed78c8df2)





17. select username and password to log in Splunk Enterprise from the browser.

![image](https://github.com/user-attachments/assets/a4c236f7-141f-4d34-94ec-0e609c8c813e)

![image](https://github.com/user-attachments/assets/3893ef76-96bf-470e-9850-d95d6ab34a6d)






















    
