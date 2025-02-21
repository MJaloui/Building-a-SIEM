![github-header-image](https://github.com/user-attachments/assets/bf835ec8-a7fb-41d1-933f-6de15c3dd1e7)

&nbsp;

&nbsp;

&nbsp;

&nbsp;

## **Steps:**

### 1.	Head to splunk.com
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

# listen for incoming TCP data on port 9998
[tcp://9998]
disabled = false
sourcetype = _json
index = network_data
```

![image](https://github.com/user-attachments/assets/9b1d186b-6d92-43c4-90a2-db73d732f71b)


### 44. Create and edit output.conf. Copy and paste the configuration below.

## Enter Cmd: 

```bash
sudo nano outputs.conf
```

## Copy and paste configuration in outputs.conf file you created.

```bash
Enter the following script, then save and exit
[tcpout]
defaultGroup = splunk_indexer

[tcpout:splunk_indexer]
server = <indexer-ip>:9998
```

![image](https://github.com/user-attachments/assets/3cbd8a5f-57c3-4d40-8b28-e33d9ad6e2ef)



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



### 47. on the top navigation bar, click "Settings" and then "Add Data" on the top left.

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
