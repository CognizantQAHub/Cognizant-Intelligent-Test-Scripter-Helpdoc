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
Google Chrome | [Chrome Driver](https://sites.google.com/a/chromium.org/chromedriver/downloads)
Mozilla Firefox | [Gecko Driver](https://github.com/mozilla/geckodriver/releases)

Update the driver path in the “Configure Browser” dialog with no .exe Extension

> ![](faqImage\browser_cfg.png)

**Browser Version**

To Verify the Chrome driver version in Linux platform. Navigate to the folder where you downloaded chrome driver and perform the below operation

> ![](faqImage\driver_v.png)

> **NOTE**: While execution, If you get the below error for chrome driver 

> **NOTE**: [SEVERE] com.cognizant.cognizantits.engine.core.Task onError: The driver is not executable: /home/<user>/linuxdemo/linuxdemo/EdevCare/lib/Drivers/chromedriver java.lang.IllegalStateException: The driver is not executable: /home/<user>/linuxdemo/linuxdemo/EdevCare/lib/Drivers/chromedriver

Navigate to the lib/Drivers folder in terminal, perform the below steps to resolve

> ![](faqImage\driver_per.png)

**Command Line Syntax**

To trigger test set execution through command line in Linux Platform perform the below steps

> ![](faqImage\cmd.png)

By Default, the command line syntax generated for Windows Platform (with “Run.bat”)

**E.g.**: Run.bat -run -project_location “\Projects\test" -release "NewRelease" -testset "NewTestSet"

Manually modify the above syntax like below for Linux Platform

> **NOTE**: ./Run.command -run -project_location "\Projects\test" -release "NewRelease" -testset "NewTestSet"

> ![](faqImage\run_cmd.png)

**Command Line Syntax**

To start selenium node, Navigate to the GridNode folder and open terminal and type **./init.command**

> **NOTE**: If Permission denied. Run the below steps

> **NOTE**: chmod 777 init.command

