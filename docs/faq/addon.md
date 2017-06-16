# **Troubleshooting**

### ** Error in Connection **


 Follow the below steps for such scenario:

**Checking Connection status and establishing the same**


**For Chrome and Firefox:**

Follow the steps below to troubleshoot the "error in Connection" error message,

- Open the **options window**, **right-click** the add-on to launch options window in **chrome** and use the shortcut **Ctrl+Shift+O** in firefox for the same.
 
- Launch **spy or heal or record** from the UI

- Click on **Test Connection**, use the default port **8887**, this port can also be changed as per your choice.


- If you are getting a **red bulb**, the certificate is not installed properly, so click on the bulb again, you will be navigated to the url **https://localhost:8887/status**, you need to give "**Proceed to unsafe**" in chrome and **Add exception** in Firefox to get to this link, 

> ![](faqImage\connected.png)


- If you do not get this message then you need to install the certificates manually.



> **NOTE**: A green bulb indicates that the connection between browser extension and the UI is established and is working fine.


> **NOTE**: For IE, you need to launch the record or spy or heal from the the UI and **launch** the URL **https://localhost:8887/status** to see the above **connected**. If you do not get the above message then you need to install the certificate manually.


**If the issue**, still persists, then do the following steps,

- **Configuring Proxy Setting**

	- If you are behind any proxy then add **localhost** in the Exceptions.  

- **Changing Java Version**


	- If the above troubleshooting didn't help you. please update your System Java version by updating System Java Path to latest Java

		- Go to **location Where Java is installed>java>jdkx.x.x_xx>jre>bin and copy the path**
		- Click on Windows **StartButton>Computer>RightClick>Properties>Advance system settings>Environmentvariables** under system variable append the path copied in step to the PATH environment variable.
	
	
	- After updating Java path restart Cognizant Intelligent Test Scripter.

	- Check the connection status and establish the same once again

 
----------

