# Custom Function & Source Code Maintenance


Cognizant Intelligent Test Scripter mostly covers all the functions under the predefined list of available actions. But some times your scenario might demand a new action to be implemented, for example performing PDF or Excel validation.This can be done by creating your own custom method.


### Constraints For Custom Function

> Any custom function that is written to fulfill your requirements should follow the below conditions.


* Custom Functions should be **public**.
 
* The return type of custom function should be **void**.

* Do not provide any package declarations when you inject through **Inject Script**.
 
* Custom Function should not contain parameters (use **Data** or **Input** or **Condition** variable for fetching data from the test case).

* Custom method should contain the **Action** annotation in order for it to get auto suggested in the UI.

 
Ensure that you import all the necessary jar files from the lib folder of the tool installation directory containing the custom method. Also, any third party libraries needed for your custom method should be referenced.

----------

###  Sample Custom Method 

For creating any Custom Method, a java class is required. A sample code for understanding the usage of various variables and functions that you can access in your custom method is available in the Engine (in the file **SampleScript.java** under the package named **com.cognizant.cognizantits.engine.commands**).