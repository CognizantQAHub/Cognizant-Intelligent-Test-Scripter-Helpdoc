

**Is CITS compatible with latest Chrome browser versions?**

 Please update the chrome driver version, to the most compatible one for your specific chrome browser version.
 [http://chromedriver.chromium.org/downloads](http://chromedriver.chromium.org/downloads)

 This can be done by replacing the compatible driver in "CITS installation location/lib/Drivers".

<br>
**Can CITS be integrated with Jenkins?**

CITS integration with CI/CD tools is feasible through command line argument support. Navigate to the CITS IDE,right click on the test case or test set and choose the option "Get CmdLine Syntax”. This command can be executed from any batch or shell console which makes the integration possible. In order to integrate with Jenkins, follow the steps below,

  - Create a Jenkins job and place all CITS  files in the Jenkins jobs workspace. 
  - Further, in the “build” tab click on “execute windows batch command” or “execute shell”
  - Place the command to call the CITS Run.bat file in the batch console.
  - This job can further be configured for a scheduled execution or triggered based on a commit in the central repository

<br>
**Do I need to set JDK path while trying to inject scripts?**

Inject script requires JDK to compile your .java files to .class files for execution. If JDK path is not set in the Run.bat file or system Path variable or in **JAVA_HOME** a prompt “Select JDK bin path” is displayed in the CITS IDE.

<br>
**Where do I get the log files in case of a test execution failure?**

The console log of execution and other HTML reports is available in the CITS “**Project location/Results folder**”. To get the project location, right click on the project from the Test design panel and choose "Details" from the context menu. The log file for CITS IDE, is available in CITS installation location as log.txt.


<br>
**Does CITS support API Automation?**

CITS is predominantly for functional testing of web applications leveraging Selenium WebDriver. To achieve API automation users can write custom methods in CITS. One such a way is to leverage the command line execution support offered by SOAPUI. The test cases are to be created and saved in SOAPUI, however the execution can be done via SOAPUI command line support through custom methods in CITS.


<br>
**Which CITS action can be used to assert element’s attribute values from the web application under test?**

The CITS action "assertElementAttrEquals" can be used. Similar actions are available here,
[https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/actions/webactions.html#assertelementattrequals](https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/actions/webactions.html#assertelementattrequals)


<br>
**How to use the reusable components created in CITS?**

Please use the keyword "**Execute**" under ObjectName column and double click on the actions column to choose the reusable component from the auto suggest. The above action can also be performed by dragging the reusable component in to the test case workspace, in order to add a step to call the respective reusable component in the test case.


<br>
**Does CITS generate java code?**

CITS projects are stored as flat files and all the actions called in your script are already coded in the engine project. There is no dynamic code generation. Please right click on your project in the design panel (under test plan) and choose “Details” from the context menu, to open the project location and the flat files created under a project. 


<br>
**How to introduce your project specific customized actions in CITS?**

Navigate to “Automation> Create CM project” from CITS IDE and create a custom method project which can be imported in Eclipse IDE. Write your custom methods and build a standalone jar of this source code in to “lib/commands”. Please refer here for more information,
[https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/faq/customfunction.html](https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/faq/customfunction.html)
[https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/faq/engine.html](https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/faq/engine.html)

<br>
**Does CITS support script execution in mobile safari browser?**

CITS supports mobile automation through Appium and hence script execution in mobile Safari is supported. However, the pre requites for mobile execution in Appium in any environment should be satisfied in the case of CITS as well. For more information, please refer here,
[http://appium.io/](http://appium.io/)


<br>
**How does CITS make a BDD feature file executable?**

CITS creates compatible test cases by reading the feature files. You can try using this feature, from **Tools>BDD>import feature file** from the CITS IDE.

- The scenario names in your feature file is your corresponding CITS test case names 
- The step names in the feature file are your corresponding reusable component names 
- The test data from Example table are also fetched as part of CITS test data sheet


<br>
**Demo Project is not executing in Chrome when tried in Mac OS. Do we have any prerequisites for the same?**

Please download the chrome driver binaries for Mac (since "exe" will not work in Mac environment) and navigate to "Browser configuration” from the CITS IDE in order to remove ".exe" from the chrome driver path.


<br>
**What is the purpose of sub iteration column in CITS test data sheet?**

- Within a test case the various sub iteration counts under iteration 1 represent the different sets of data against which the test case is going to be executed in a loop
- In general, there can be any number of sub iterations under an iteration and at the same time there can be any number of iterations in a datasheet. Execution of an iteration is nothing but executing all the sub iterations under that iteration.
- In the design panel only the sub iterations of iteration 1 is executed, the sub iterations of other iterations are considered only from the execution panel.


<br>
**How to map VSTS with automated scripts in CITS tool?**

CITS supports out of the box integration with TFS version 2017. Please ensure the below pre-requisites are met for establishing the integration,

- In TFS, ensure that the Test Suit under the Test Plan has the same name as the scenario containing the test cases
- Similarly, the test cases created in TFS, should have the same name as the test cases whose results need to be uploaded
- Execute the Test Set. Now the results will be updated to TFS once the execution is completed.
- In TFS, click the Runs Option to view the various runs and the status of each runs


<br>
**How to use Object Spy?**

You can either record your flow or use the object spy to add objects to the object repository. The objects, in the repository, can also be added manually in cases when a custom xpath needs to be introduced for the object. Refer steps below to use object spy,
-	Start object spy from CITS IDE
-	Click on the add on in the browser to get “S” in green
-	Move to object and perform “Ctrl+ Right click” to add the same to the web object repository. 

**Note**: If you see the message “error in connection”, please refer "Exception FAQs" question 1.


<br>
**How to read input from user, at run time?**

CITS has provisions to create data sheets for your project, which can be leveraged for parameterizing the test cases. Please use the action "Set" for sending any test data to the web application. Refer here for more information on actions in CITS,

[https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/actions/webactions](https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/actions/webactions)


<br>
**Where to get CITS IE toolbar latest version?**

Please use the latest IE Toolbar from
[https://github.com/CognizantQAHub/Cognizant-Intelligent-Test-Scripter-IE-Toolbar/releases](https://github.com/CognizantQAHub/Cognizant-Intelligent-Test-Scripter-IE-Toolbar/releases)

<br>
**Do we have any user manual or help documentation for CITS?**

CITS help artifact can be accessed from here,
[https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/](https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/)

All web actions available out of the box in CITS are here,
[https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/actions/webactions](https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/actions/webactions)

<br>
**How to execute CITS script from command prompt without using the IDE?**
CITS supports command line execution and the syntax for executing a test case or test set from any batch console can be obtained by following the steps,

- Navigate to Test plan (or Test lab) and right click on any test case (or test set)
- Click on “Get CmdLine Syntax” context menu option in order to copy the command to clipboard 
- Open command prompt and execute this command from the location where “Run.bat” file is available


<br>
**How to handle Conditions in script execution?**

Conditions can be handled in custom methods in CITS. Please refer here for understanding custom methods in CITS,
[https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/faq/engine](https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/faq/engine)

[https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/faq/customfunction](https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/faq/customfunction)

 <br>

### Exception FAQs

**How to handle the error message - 'Error in connecting App Refer FAQ' obtained while working with the CITS add on?**

Please refer the documentation here.
[https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/faq/addon.html#error-in-connection](https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/faq/addon.html#error-in-connection)

<br>
**How to handle the exception – “Exception in thread "UI:MainUI - java.lang.ExceptionInInitializerError”, triggered while launching CITS IDE?**

Please ensure that Java 8 is added to system path variable or CITS Run.bat file is hard coded with java 8 before working with the tool.

<br>
**How to handle the exception - "Your connection is not secure” faced during execution in Firefox?**

If you are trying to navigate to HTTPS site, a  Firefox capability “acceptInsecureCerts” can help in                                    overcoming this issue. This can be done by following steps below,

-	Navigate to “**Browser Configuration - -> Manage Browsers - > Choose Firefox from the dropdown**” from the CITS IDE.
-	Add the capability “**acceptInsecureCerts**” and a value for the same as “true”. 
-	Save the settings and execute your test case

<br>
**How to handle the exception - “protected mode settings are not same for all the browsers”, encountered during script execution in IE browser? **

For automating in IE (With Selenium) there are some pre-requisites, please refer the below link,
[https://stackoverflow.com/questions/38222259/unable-to-launch-ie-browser-in-selenium-webdriver](https://stackoverflow.com/questions/38222259/unable-to-launch-ie-browser-in-selenium-webdriver)

As suggested in the above links, please ensure two things,
- Set the same protected mode settings for all the zones
- Add the site's URL to the list of trusted sites in the trusted site zone under the security tab in Internet options

Please ensure that user has sufficient rights and permission in the network to perform the above two suggestions.


<br>
**How to handle the exception - “Could not resolve dependencies” encountered while building the CITS tool?**

Some jars may not be downloaded with the proxy or maven configuration in your environment. Hence please download them manually and place them in the remote maven repository (m2 folder in your system). However, built version of CITS is available at,
[https://github.com/CognizantQAHub/Cognizant-Intelligent-Test-Scripter/releases](https://github.com/CognizantQAHub/Cognizant-Intelligent-Test-Scripter/releases)
and can be used in case you have not performed any changes to the source code, instead of building the source code from scratch.
 
<br>
**How to handle the exception – “java. lang.ClassNotFoundException” triggered during database testing in CITS?**

Please place the driver jar file under "lib/clib" folder and provide the connection string "jdbc:<Database>://<Host>:<Port>/<Database name>" under database settings. Proceed to test for a successful connection.


<br>
**How to handle the exception “Seems Like the Element is Not Visible or hidden at the moment” that is triggered during a test case execution?**

Please check the following,
- Analyze how the web element are identified during execution (with which property/attribute) from the console log of execution.  
- Check if that property (with which CITS is identifying the element) is a unique match for the element
Try adding a “**waitforelementobeclickable**” action before performing the actual operation on the element 

<br>

**Can CITS be integrated with Applitools?**

CITS is built on top of Selenium webdriver and Selenium can be integrated with Applitools, so is the case with CITS tool as well.

Refer here to integrate Applitools with Selenium webdriver,
https://applitools.com/tutorials/selenium-java.html

This code can be then introduced as custom methods in CITS, refer here to know more about custom methods in CITS,
https://cognizantqahub.github.io/Cognizant-Intelligent-Test-Scripter-Helpdoc/faq/customfunction.html

<br>

**Can CITS read data from external spreadsheets?**

CITS supports only .csv formatted files. External test data in CITS csv format, can be opened in CITS tool directly. Navigate to "Test Data> Import TestData" in the Test Design panel, in order to open an external test data sheet.




