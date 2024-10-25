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
4.	Click “Free Trial” underneath Splunk Enterprise
5.	After signing up and verifying email, log in
6.	A landing page will appear to install your package

![image](https://github.com/user-attachments/assets/90bcc22e-0b10-4ffc-9a73-e01bba519046)




8. For the Linux OS click "Copy wget link" for the ".deb" package
 
![image](https://github.com/user-attachments/assets/71fa5e98-4f97-48fc-92ef-4e76e1e67fb5)

![image](https://github.com/user-attachments/assets/f03e0a97-744c-4346-8ecd-d91ff21aaccb)



9. Paste the copied wget command into the VM

![image](https://github.com/user-attachments/assets/da396f25-74d8-44f3-8fd8-8ce135846260)




10. In the VM enter "ls" to verify you have your ".deb" package file

![image](https://github.com/user-attachments/assets/6c195896-5bc8-42f2-b3f3-f5ef31ba0f6e)




11. Copy the ".deb" file to download the package
12. Enter this command in the VM "sudo dpkg -i splunk-9.3.1-0b8d769cb912-linux-2.6-amd64.deb"

![image](https://github.com/user-attachments/assets/8cfa6b12-b03b-4f48-ab49-7b1f79009f4d)








