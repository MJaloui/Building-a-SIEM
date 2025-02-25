![github-header-image](https://github.com/user-attachments/assets/bf835ec8-a7fb-41d1-933f-6de15c3dd1e7)

&nbsp;

&nbsp;

&nbsp;

&nbsp;

## **Steps:**

### 1.	Head to www.splunk.com
### 2.	Click “products” above
### 3.	Underneath “Platform” click “Splunk Enterprise”
### 4.	Click “Free Trial” underneath Splunk Enterprise.
### 5.	After signing up and verifying email, log in.
### 6.	A landing page will appear to install your package.

![image](https://github.com/user-attachments/assets/90bcc22e-0b10-4ffc-9a73-e01bba519046)




### 7. For the Linux OS click "Copy wget link" for the ".deb" package.
 
![image](https://github.com/user-attachments/assets/71fa5e98-4f97-48fc-92ef-4e76e1e67fb5)

![image](https://github.com/user-attachments/assets/f03e0a97-744c-4346-8ecd-d91ff21aaccb)



### 8. Paste the copied wget command into the VM.

![image](https://github.com/user-attachments/assets/da396f25-74d8-44f3-8fd8-8ce135846260)




### 9. In the VM enter "ls" to verify you have your ".deb" package file.

![image](https://github.com/user-attachments/assets/6c195896-5bc8-42f2-b3f3-f5ef31ba0f6e)




### 10. Enter the command "sudo apt-get update" to ensure you have the latest package.

```bash
sudo apt-get update
```

### 11. Enter the command "apt-get install curl" to be able to be able to install deb. package.

```bash
apt-get install curl
```

### 12. Enter cmd "ls" to view and Copy the ".deb" file to download the package.

![image](https://github.com/user-attachments/assets/02a6f1a9-4c77-4527-828a-85595dd5ce8d)



### 13. Enter the downlaod package command along with the copied .deb file in your VM to download the package.

 ```bash
sudo dpkg -i splunk-9.3.1-0b8d769cb912-linux-2.6-amd64.deb
```

![image](https://github.com/user-attachments/assets/fe18dfcd-cd23-4896-a207-57e78be5c856)




### 14. Enter the command to enable start at boot.

 - This will also prompt the Splunk license agreement .
 - Enter "y" to agree

![image](https://github.com/user-attachments/assets/e8b46275-a67c-4998-bb5e-85cb35c83320)

![image](https://github.com/user-attachments/assets/71467f21-a47d-4d59-98f2-1c9ed78c8df2)





### 15. select username and password to log in Splunk Enterprise from the browser.

![image](https://github.com/user-attachments/assets/a4c236f7-141f-4d34-94ec-0e609c8c813e)

![image](https://github.com/user-attachments/assets/3893ef76-96bf-470e-9850-d95d6ab34a6d)





### 16. Enter command to allow SSH port on firewall.
    (If "sudo ufw alow openSSH" doesn't work then try "sudo ufw allow 22/tcp")

![image](https://github.com/user-attachments/assets/4d707e8b-c57d-48d3-958c-c22ac6375af9)




### 17. Enter command to allow port 8000 on firewall.

![image](https://github.com/user-attachments/assets/054e0b6c-0da1-4d95-928a-60c6440d12aa)




### 20. Enter command to enable firewall.

![image](https://github.com/user-attachments/assets/5bd42993-b8e2-4344-b85f-31921b8ab54d)




### 21. Enter command to find your IP address.
Enter "ip a" or "ipconfig" to view IP

![image](https://github.com/user-attachments/assets/38163049-75dc-459f-aeeb-8bab62f26493)




### 22. Enter command to start splunk.

![image](https://github.com/user-attachments/assets/51d0058d-721f-4c81-9807-62da2a6c6049)



    
### 23. After start command is submitted, you will recieve web browser credentials for Splunk web interface.
    (http://MJBuildsSIEM:8000) or (http:INSERTIPADDRESS:8000)

![image](https://github.com/user-attachments/assets/a133cb0f-0ab0-45e1-bddd-7d1e7d5f3779)




### 24. Open up a browser and enter Splunk web interface credentials "IPADRRESS:8000"
    
![image](https://github.com/user-attachments/assets/b5f94a0f-6c8d-4be8-b27f-973d2fff7336)

![image](https://github.com/user-attachments/assets/924a642c-d205-47e7-aa28-f4912fc630de)





### 25. On the top navigation bar, click "Settings". Underneath "Data" click "Forwarding and receiving"

![image](https://github.com/user-attachments/assets/54019fe4-1186-4ae8-854c-0ce1a2e31dcc)

![image](https://github.com/user-attachments/assets/f90bb45e-d875-47b7-90d0-ad12a50fbf04)

    

### 26. Click green button "New Recieving Port" on the top right.
    In the "Listen on this port" text box, enter port number "9997" 

![image](https://github.com/user-attachments/assets/f9613a1a-ce7f-4fb3-b31e-21e23f8fc164)

![image](https://github.com/user-attachments/assets/33438ba8-167c-4fb5-ae32-8b710c8e2bae)




### 27. Verify your new added port is there and set to "Enabled".

  ![image](https://github.com/user-attachments/assets/1dede8fd-a32a-4831-b0a0-64b74b17ec59)




### 28. Click "Settings" and under "Data" click "Indexes"

![image](https://github.com/user-attachments/assets/0921d5fb-42a5-4e2e-a7f0-4104fbc416f0)

![image](https://github.com/user-attachments/assets/3f08966e-81e3-4432-a395-d1e9031f6202)





### 29. On the top right, click the green button "New Index"

 ![image](https://github.com/user-attachments/assets/0e29c4b8-8514-41d8-8a94-ba821f974085)
   
![image](https://github.com/user-attachments/assets/44a761ba-861c-4a89-9bcc-b80f30b0a264)





### 30. In the "Index Name" field, enter in the text box "wineventlog" (or any name 
    you want to name it).

### 31. Click "Save".

![image](https://github.com/user-attachments/assets/880c2b11-dfc6-4373-944a-f59e23e7a18f)





### 31. Verify the new created Index is there.

![image](https://github.com/user-attachments/assets/d495cb00-c75e-42a8-b93c-e76d5ae014a8)




### 32. Open a browser, log into your account on splunk.com to download Splunk 
    Universal Forwarder.



### 33. After signing in, click "Products' on the top bar.
    
![image](https://github.com/user-attachments/assets/73d1571f-5af2-4067-97b2-f8a7ffdd509f)




### 34. Underneath "products" click "Free Trials & Downloads".

![image](https://github.com/user-attachments/assets/4a495655-4e10-4ee8-80a0-492d966e47d2)





### 35. Underneath "Splunk Enterprise" click "Get My Free Trial". 

![image](https://github.com/user-attachments/assets/3bd0dcaa-0587-4287-9c16-69609b00045a)





### 36. Choose your installation package under Linux for the deb. package, click 
    "Copy wget link" to copy the link in the textbox.

![image](https://github.com/user-attachments/assets/6537af72-8021-49f4-a563-17d82f9bab84)




 
### 37. Enter the copied link in the VM. 

![image](https://github.com/user-attachments/assets/272028f3-488c-4417-a557-800b0dec751f)

![image](https://github.com/user-attachments/assets/f3dbc209-2758-47d3-b27f-c72202011d6f)





### 38. Enter the command to install .deb package.

![image](https://github.com/user-attachments/assets/e386b4b8-c40d-42f8-94f0-f8e03c688d07)

![image](https://github.com/user-attachments/assets/8136d956-cc6a-4a49-8439-322b38abf2f4)





### 39.  Enter the command "sudo apt-get install -f" to fix any broken dependencies from installations.

![image](https://github.com/user-attachments/assets/886bbacf-b66c-4bbc-b8c5-4b0a89d3aff3)





### 40.  Enter command to start the splunk forwarder.

![image](https://github.com/user-attachments/assets/f9d13bdf-9e72-426d-901c-953cb2a13875)





### 41. After forwarder is started you will be prompt to answer yes or no to the lisense agreement.
    Enter "y" to agree.

![image](https://github.com/user-attachments/assets/adc181fe-936b-4a17-bd1f-7a5d990e9e2e)


### 42. Navigate to the local directory to create and edit the inputs.conf file in the Splunk Forwarder configuration directory: /opt/splunkforwarder/etc/system/local/.

## Enter Cmd:

``` bash
sudo nano /opt/splunkforwarder/etc/system/local/inputs.conf
```

### 43. Copy the configuration below and paste it in the inputs.conf file, On your keyboard press "^X" (ctrl+x) to exit, then press "Y" to save the file, press "Enter" to confirm the file name. Look on the bottom left to verify you are entering the right thing.

## After saving this file, you can enter the command "sudo cat inputs.conf" command to verify it was saved.

```bash
[monitor:///var/log/syslog]
disabled = false
index = main
sourcetype = syslog
```

![image](https://github.com/user-attachments/assets/1e382d53-dc04-4608-bad7-0ac0bbabf544)



### 44. Create and edit output.conf. Copy and paste the configuration below.

## Enter Cmd: 

```bash
sudo nano outputs.conf
```

## Copy and paste configuration in outputs.conf file you created. Add your Ip address and port number for your indexer. Then exit and save it.

```bash
[tcpout]
defaultGroup = splunk_indexer

[tcpout:splunk_indexer]
server = <IP_Address>:<Port_Number>
```

![image](https://github.com/user-attachments/assets/24bd5aae-1964-457f-b5d1-e29356873981)




### 45. On your keyboard press "^X" (ctrl+x) to exit, press "Y" to save the file, press "Enter" to confirm the file name. Look on the bottom left to verify you are entering the right thing. Enter the Cmd "sudo cat outputs.cong" if you'd like to verify it's saved.


### 46. After saving the configuration files, enter the "stop" and "restart" Splunk command to update the settings.

```bash
sudo /opt/splunkforwarder/bin/splunk stop
```       

![image](https://github.com/user-attachments/assets/728e1f91-a7e0-4d6e-a1d5-9e74568aa77e)

 - Enter Cmd to restart

```bash
sudo /opt/splunkforwarder/bin/splunk restart
```

![image](https://github.com/user-attachments/assets/adea019a-afc6-48d9-96f6-7af195a073ab)




### 46. Log into Splunk Enterprise interface on your browser.



### 47. Navigate back to Splunk in your browser. In the top navigation bar, click "Settings", and then click "Add Data" on the top left-hand side.

![image](https://github.com/user-attachments/assets/a3b14f4a-d85e-4159-8039-f6f75037aa9f)





### 48. On the bottom right, click "Forward".

![image](https://github.com/user-attachments/assets/f1dd7838-b7ad-4b7b-b1c1-389b549e3b38)

![image](https://github.com/user-attachments/assets/0162bcdd-9915-4844-8621-e954cf361ac7)





### 49. Click on your available host under "Available host(s) to move it to "selected host(s). 

![image](https://github.com/user-attachments/assets/488d4dee-6e64-499b-9835-342717613689)

![image](https://github.com/user-attachments/assets/d1a62aad-36ad-4ee1-98f8-bbeea83acee9)



#### 50. Enter 'New Server Class Name" in the text box and then click "Next" in the top right.

![image](https://github.com/user-attachments/assets/dc80e486-775d-4ef0-bd5b-97bd3d70603e)

![image](https://github.com/user-attachments/assets/56d7dad2-1066-43de-b81b-13d3bf6f4ab4)





### 51. If you not see "Local Event Logs" (see screenshot) as an option on the your list follow steps 48-51(permissions is required to view Local Event Logs). If you do see "Local Event Logs" continue with step 52. 

![image](https://github.com/user-attachments/assets/47f13ddd-8b26-49b0-bb1e-3a3a0009e60f)





### 52. On the top of the navigation bar click "Settings", underneath "Users And Authentication" click "Users". 

![image](https://github.com/user-attachments/assets/3bd4753e-1c11-4c40-a2ee-487905d493ea)

![image](https://github.com/user-attachments/assets/6356fffd-d8a9-40e6-8876-d867cec92fd2)





### 53. click on your name to add permissions.

![image](https://github.com/user-attachments/assets/79566248-c432-44d5-a58c-9b3f98c67d77)




### 54. Next to "Assign roles" click all items under "Available item(s)" to move 
    over to "Selected item(s). All items should be under "Selected Items"
    Click "Edit after changes are made"

![image](https://github.com/user-attachments/assets/aa60170b-0315-4c0e-a9f2-563c1805921c)

![image](https://github.com/user-attachments/assets/ff5f9a46-ab8e-451d-a875-b6418ac1dda2)





### 55. on the top navigation bar, click "Settings" and then "Add Data" on the top 
    left.

![image](https://github.com/user-attachments/assets/a3b14f4a-d85e-4159-8039-f6f75037aa9f)





### 56. On the bottom right, click "Forward".

![image](https://github.com/user-attachments/assets/f1dd7838-b7ad-4b7b-b1c1-389b549e3b38)




### 57. Click on "Existing".

![image](https://github.com/user-attachments/assets/ad72eaf1-f3db-4eda-b0d5-0436b44315e8)



### 58. Under "Existing" Select your "Server Class" you created previously.
    Click "Next" on the top right after selection in made.

![image](https://github.com/user-attachments/assets/51e30828-c6e7-47a0-b21f-361085c96bac)

![image](https://github.com/user-attachments/assets/42c910ff-69ad-48c3-8a6c-8026c3b8ad5c)




### 59. Click "Local Event Logs", then click all event logs under "Available 
    item(s)" to move over to "Selected item(s)" 
    *Items to select: Application, ForwardedEvents, Security, Setup, System*
     Click "Next" on the top right.
    
![image](https://github.com/user-attachments/assets/a34c440c-1c1b-409b-b2a5-a7208a42bb7f)

![image](https://github.com/user-attachments/assets/2558457c-2880-4d1d-bcd6-bbbb3c242888)

![image](https://github.com/user-attachments/assets/760c8816-234b-48c0-b863-776f5b8f7089)




### 60. Select the Index you created under "Default".
    Click "wineventlog"
    Click "Review" on the top right.

![image](https://github.com/user-attachments/assets/87cbd7a2-b45b-43e5-9f56-142304638d3c)

    



### 61. Click "Submit" after you've reviewed your selections. 
   
![image](https://github.com/user-attachments/assets/2b121b5d-84f8-4e40-ad3e-f1a77c2189f5)





### 62.  After configuring the log forwarding settings, click 'Start Searching'

![image](https://github.com/user-attachments/assets/f4419e3f-951c-4f4c-8566-e066648f07cd)



### 63. Navigate to "Settings" on the top and click "Indexes" under "Data" to verify logs are generating in the Index you created.

![image](https://github.com/user-attachments/assets/ced6d1d0-a8c2-4ed1-a8f4-afe279f144b4)



### 64. You will notice the amount on data is a higher number than before. Notice my index that was created is now 15 MB, it was originally 1 MB.


 - ## Before
 
 ![image](https://github.com/user-attachments/assets/1e739324-42f8-4b2f-9c96-19630f5f5ab2)

 
 
 - ## After

![image](https://github.com/user-attachments/assets/9f889bd0-dda4-4d5f-91b5-61a848e499cd)



### 65. Navigate to home the page and click "Search & Reporting" or "Find" on the top taskabar to search the index you created and the new generated logs. 


  - ## On the search page, enter this query below to generate logs from the index you've created.

```bash
index='Your_Index_Name'
```

![image](https://github.com/user-attachments/assets/cae29992-a08a-49e9-9ed3-6031487d175e)


### 66. After entering the query, the data will be visable as shown below.

 - You should see atleast one or mulitple events if you verfied that your index storage is a higher amount. The log below is one example of one event in the index I created.

![image](https://github.com/user-attachments/assets/9b45512a-8284-4002-8dc6-48fc3bbc0ef2)



### 67. Finally, test a crendtial scan using nmap in a network traffic index inside a Docker container. You will need to:

 - Create a new index for network traffric
 - Install Nmap (if you don't have this tool)
 - Install Docker (if you don't have this tool)



### 68. Click "Settings" and under "Data" click "Indexes"

![image](https://github.com/user-attachments/assets/0921d5fb-42a5-4e2e-a7f0-4104fbc416f0)

![image](https://github.com/user-attachments/assets/3f08966e-81e3-4432-a395-d1e9031f6202)





### 69. On the top right, click the green button "New Index"

 ![image](https://github.com/user-attachments/assets/0e29c4b8-8514-41d8-8a94-ba821f974085)
   
![image](https://github.com/user-attachments/assets/44a761ba-861c-4a89-9bcc-b80f30b0a264)





### 70. In the "Index Name" field, enter in the text box "network_data" (or any name 
    you want to name it).



### 71. Click "Save" and verify your network data index was created.

![image](https://github.com/user-attachments/assets/880c2b11-dfc6-4373-944a-f59e23e7a18f)



### 72. Navigate back to your virtual machine and go to the local directory and open inputs.conf file to edit network_data configuration.

```bash
cd /opt/splunkforwarder/etc/system/local
```

```bash
nano inputs.conf
```

![image](https://github.com/user-attachments/assets/9a738041-a2ad-4894-9c2e-22784a200c77)

![image](https://github.com/user-attachments/assets/49a18acc-debb-4ddf-bef7-774ab3b0abb2)




### 73. Paste the the last five lines of the script, the whole script should look similar to the screen shot below. 

 - ## On your keyboard press "^X" (ctrl+x) to exit, then press "Y" to save the file, press "Enter" to confirm the file name.

```bash
[monitor:///var/log/syslog]
disabled = false
index = main
sourcetype = syslog

# listen for incoming TCP data on port 9998
[tcp://9998]
disabled = false
sourcetype = _json
index = network_data
```

![image](https://github.com/user-attachments/assets/2eb1106c-821e-4f89-956c-112df27ded6c)


### 74. Install nmap if you do not have this tool. 

 - ## Verify if you have nmap. If no version is shown, then you do not have it.

```bash
nmap --version
```

 - ## If you don't have namp, enter the apt install command.

```bash
sudo apt install nmap
```



### 75. Verify if you have Docker. If no version is shown, then you don't have it.

```bash
docker --version
```

![image](https://github.com/user-attachments/assets/950ea5d6-686b-406c-b7c3-6888bdc8a44d)

 - ## If you don't have docker, watch this quick video below to install docker or go to www.docker.com and follow the direction to download docker.

- ## [Click here to learn how to install Docker.](https://youtu.be/cqbh-RneBlk?si=Wg7GHXnyzsOrAzMH)


### 76. Download the Nmap Docker image to your Virtual Machine.

```bash
sudo docker pull instrumentisto/nmap
```
![image](https://github.com/user-attachments/assets/1d489ad4-4e50-4467-a5c7-4e8d6c61b52d)


### 77. After pulling the Nmap Docker image, you can run a SYN scan on the target IP (your IP address) by executing the following command:

 ## - Replace <target_ip> with the IP address of the system running Splunk.

```bash
docker run --rm --network host instrumentisto/nmap -sS <target_ip>
```

![image](https://github.com/user-attachments/assets/1547475c-bf2f-49da-a532-530951d67437)




### 78. Verify the scan was a success. Check your index logs in Splunk for recent updates, You will see a credential scan. Enter search query to find the latest scan.



```bash
index=wineventlog
```

![image](https://github.com/user-attachments/assets/71430e76-7ea0-4b52-938f-1fe425f8bf8e)




### 79. There will be new generated logs for credential scans. 

 - ## You can also click "Show all 21 lines" to view more details. 

- ## The "EventCode" listed on the log can be searched directly in splunk for more details, you can use Google or Chaptgpt to find general information as well.


![image](https://github.com/user-attachments/assets/11cda3d7-3b47-4220-a2f0-de990f94eff7)

 

### 80. Key indicators and ways to identify a credential scan occured.

 - ## "Message": will indicate Credentials Manager were read.
   
 - ## "Read Operation": If it shows "Enumerate Credentials", it's suggesting there are signs of someone possibly attemping to obtain usernames and passwords or there's a security scan.
 
 - ## Before line 21, you will recieve a brief explantion to why that particular event occured.

 - ## You can research specific keywords to find related logs. For example, adding "Audit Success" to your query will generate more logs similar to the current one. This can be found on your logs  next to "Keywords"
      
![image](https://github.com/user-attachments/assets/088f8079-ffef-48b5-9042-57d4e58c01ae)









