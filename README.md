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




7. For the Linux OS click "Copy wget link" for the ".deb" package.
 
![image](https://github.com/user-attachments/assets/71fa5e98-4f97-48fc-92ef-4e76e1e67fb5)

![image](https://github.com/user-attachments/assets/f03e0a97-744c-4346-8ecd-d91ff21aaccb)



8. Paste the copied wget command into the VM.

![image](https://github.com/user-attachments/assets/da396f25-74d8-44f3-8fd8-8ce135846260)




9. In the VM enter "ls" to verify you have your ".deb" package file.

![image](https://github.com/user-attachments/assets/6c195896-5bc8-42f2-b3f3-f5ef31ba0f6e)




10. Enter the command "sudo apt-get update" to ensure you have the latest package.
11. Enter the command "apt-get install curl" to be able to be able to install deb. package.
12. Copy the ".deb" file to download the package.
13. Enter this command in the VM "sudo dpkg -i splunk-9.3.1-0b8d769cb912-linux-2.6-amd64.deb" (the .deb file you have on your vm).

![image](https://github.com/user-attachments/assets/fe18dfcd-cd23-4896-a207-57e78be5c856)




14. Enter the command to enable start at boot.
15. This will also prompt the Splunk license agreement .
16. Enter "y" to agree

![image](https://github.com/user-attachments/assets/e8b46275-a67c-4998-bb5e-85cb35c83320)

![image](https://github.com/user-attachments/assets/71467f21-a47d-4d59-98f2-1c9ed78c8df2)





17. select username and password to log in Splunk Enterprise from the browser.

![image](https://github.com/user-attachments/assets/a4c236f7-141f-4d34-94ec-0e609c8c813e)

![image](https://github.com/user-attachments/assets/3893ef76-96bf-470e-9850-d95d6ab34a6d)





18. Enter command to allow SSH port on firewall.
    (If "sudo ufw alow openSSH" doesn't work then try "sudo ufw allow 22/tcp")

![image](https://github.com/user-attachments/assets/4d707e8b-c57d-48d3-958c-c22ac6375af9)




19. Enter command to allow port 8000 on firewall.

![image](https://github.com/user-attachments/assets/054e0b6c-0da1-4d95-928a-60c6440d12aa)




20. Enter command to enable firewall.

![image](https://github.com/user-attachments/assets/5bd42993-b8e2-4344-b85f-31921b8ab54d)




21. Enter command to find your IP address.
Enter "ip a" or "ipconfig" to view IP

![image](https://github.com/user-attachments/assets/38163049-75dc-459f-aeeb-8bab62f26493)




22. Enter command to start splunk.

![image](https://github.com/user-attachments/assets/51d0058d-721f-4c81-9807-62da2a6c6049)



    
23. After start command is submitted, you will recieve web browser credentials for Splunk web interface.
    (http://MJBuildsSIEM:8000) or (http:INSERTIPADDRESS:8000)

![image](https://github.com/user-attachments/assets/a133cb0f-0ab0-45e1-bddd-7d1e7d5f3779)




24. Open up a browser and enter Splunk web interface credentials "IPADRRESS:8000"
    
![image](https://github.com/user-attachments/assets/b5f94a0f-6c8d-4be8-b27f-973d2fff7336)

![image](https://github.com/user-attachments/assets/924a642c-d205-47e7-aa28-f4912fc630de)





25. On the top navigation bar, click "Settings". Underneath "Data" click "Forwarding and receiving"

![image](https://github.com/user-attachments/assets/54019fe4-1186-4ae8-854c-0ce1a2e31dcc)

![image](https://github.com/user-attachments/assets/f90bb45e-d875-47b7-90d0-ad12a50fbf04)

    

26. Click green button "New Recieving Port" on the top right.
    In the "Listen on this port" text box, enter port number "9997" 

![image](https://github.com/user-attachments/assets/f9613a1a-ce7f-4fb3-b31e-21e23f8fc164)

![image](https://github.com/user-attachments/assets/33438ba8-167c-4fb5-ae32-8b710c8e2bae)




27. Verify your new added port is there and set to "Enabled".

  ![image](https://github.com/user-attachments/assets/1dede8fd-a32a-4831-b0a0-64b74b17ec59)




28. Click "Settings" and under "Data" click "Indexes"

![image](https://github.com/user-attachments/assets/0921d5fb-42a5-4e2e-a7f0-4104fbc416f0)

![image](https://github.com/user-attachments/assets/3f08966e-81e3-4432-a395-d1e9031f6202)





29. On the top right, click the green button "New Index"

 ![image](https://github.com/user-attachments/assets/0e29c4b8-8514-41d8-8a94-ba821f974085)
   
![image](https://github.com/user-attachments/assets/44a761ba-861c-4a89-9bcc-b80f30b0a264)





30. In the "Index Name" field, enter in the text box "wineventlog" (or any name you want to name it).
31. Click "Save".

![image](https://github.com/user-attachments/assets/880c2b11-dfc6-4373-944a-f59e23e7a18f)





31. Verify the new created Index is there.

![image](https://github.com/user-attachments/assets/d495cb00-c75e-42a8-b93c-e76d5ae014a8)




32. Open a browser, log into your account on splunk.com to download Splunk Universal Forwarder.
33. After signing in, click "Products' on the top bar.
    
![image](https://github.com/user-attachments/assets/73d1571f-5af2-4067-97b2-f8a7ffdd509f)




34. Underneath "products" click "Free Trials & Downloads".

![image](https://github.com/user-attachments/assets/4a495655-4e10-4ee8-80a0-492d966e47d2)





35. Underneath "Splunk Enterprise" click "Get My Free Trial". 

![image](https://github.com/user-attachments/assets/3bd0dcaa-0587-4287-9c16-69609b00045a)





36. Choose your installation package under Linux for the deb. package, click "Copy wget link" to copy the link in the textbox.

![image](https://github.com/user-attachments/assets/6537af72-8021-49f4-a563-17d82f9bab84)




 
37. Enter the copied link in the VM. 

![image](https://github.com/user-attachments/assets/272028f3-488c-4417-a557-800b0dec751f)

![image](https://github.com/user-attachments/assets/f3dbc209-2758-47d3-b27f-c72202011d6f)





38. Enter the command to install .deb package.

![image](https://github.com/user-attachments/assets/e386b4b8-c40d-42f8-94f0-f8e03c688d07)

![image](https://github.com/user-attachments/assets/8136d956-cc6a-4a49-8439-322b38abf2f4)





39.  Enter the command "sudo apt-get install -f" to fix any broken dependencies from installations.

![image](https://github.com/user-attachments/assets/886bbacf-b66c-4bbc-b8c5-4b0a89d3aff3)





40.  Enter command to start the splunk forwarder.

![image](https://github.com/user-attachments/assets/f9d13bdf-9e72-426d-901c-953cb2a13875)





41. After forwarder is started you will be prompt to answer yes or no to the lisense agreement.
    Enter in  "y" to agree.

![image](https://github.com/user-attachments/assets/adc181fe-936b-4a17-bd1f-7a5d990e9e2e)





42. Log into Splunk Enterprise interface on your browser.
43. on the top navigation bar, click "Settings" and then "Add Data" on the top left.

![image](https://github.com/user-attachments/assets/a3b14f4a-d85e-4159-8039-f6f75037aa9f)





44. On the bottom right, click "Forward".

![image](https://github.com/user-attachments/assets/f1dd7838-b7ad-4b7b-b1c1-389b549e3b38)

![image](https://github.com/user-attachments/assets/0162bcdd-9915-4844-8621-e954cf361ac7)





45. 



































































































































