# Linux Configuration

### How to Install


 **Make sure you have downloaded and extracted the cognizant-intelligent-test-scripter-*-setup.zip from releases**


**Launching UI**

Open the terminal and navigate to tool location and type **./Run.command** to launch the CITS IDE

**Note:** If Permission denied. Run the below steps

> ![](faqImage\permission.png)

**Driver Configuration**

**Browser Version**

To verify Chrome Browser version in Linux Platform use the below command

> ![](faqImage\chrome_v.png)

Download the compatible driver for the browser , refer the below links to download latest driver

Browser | Latest Driver Download links
--------|-----------------------------
Google Chrome | [Chrome Driver!](https://sites.google.com/a/chromium.org/chromedriver/downloads)
Mozilla Firefox | [Gecko Driver!](https://github.com/mozilla/geckodriver/releases)

Update the driver path in the “Configure Browser” dialog with no .exe Extension

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

