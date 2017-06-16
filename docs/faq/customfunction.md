# ** Custom Function & Source Code Maintenance **


Cognizant Intelligent Test Scripter mostly covers all the functions under the predefined list of available actions. But some times your scenario might demand a new action to be implemented, for example performing PDF or Excel validation.This can be done by creating your own custom method.


### **Constraints For Custom Function**

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

----------

### **How To Execute A Specified Test Case From Your Custom Method?**


There is an inbuilt method available with Cognizant Intelligent Test Scripter called **executeTestCase**,
which can be used to execute a particular test case under a particular scenario.

``` java
    public void executeTestCase(String scenarioName, String testCaseName);
    public void executeTestCase(String scenarioName, String testCaseName, int subIteration);
```

The above method will execute the test case under the particular scenario and for that particular **subiteration**.

----------

### ** How To Execute An Action From A Custom Method? **


A function called **executeMethod** is available with the Engine and is overloaded in 4 different ways as follows.The action name passed as an argument should be the same as the method for the corresponding action in the Engine.

- `public void executeMethod(WebElement element, String Action);`

This will just call the method of the action that was instructed. 
Any of these overloaded methods can be used that suits your requirements best.


----------

### ** How To Access An Object From The Object Repository? **


It is possible to access a specific object from the object repository using the function **AObject.findElement** as shown below.

``` java
     WebElement element=AObject.findElement(ObjectName, Reference);
```

Now all element related functions can be used for this `element` variable like;


``` java
    element.sendKeys(Data);
```

> **Note:** For more information, please refer the SampleScript.java file available in the Engine.


----------

### ** How To Handle Conditions Inside A Custom Function? **

 It is possible to write a custom function, that checks for a condition and if the condition passes it will execute a set of code and if it fails then it will execute a different set of code.The custom method **handleCondition** defined below, will check if the element is displayed and if so, it will execute the test case **cancelTicket** but if it is not displayed then it will just update the report with a "**DONE**" status.

``` java
 public void handleCondition()

  if (element.isDisplayed()) {

   executeTestCase("testscenario1", "cancelTicket", 1);
   Report.updateTestLog("Userdefined Action ", "inside reusable", Status.PASS);

 
  }
```

----------


### ** How To Access A Test Data Sheet In Your Custom Method? **


**Local Data sheet**

> We have dedicated functions to access the data from the datasheet. The **getData** function is overloaded in the following ways and can be used accordingly in your custom method. 

    public String getData(String DataSheetName, String ColumnName);

Provide the name of the sheet (**Sample**) and column (**Data1**) that contains the data and this function will return a string which is the value of the required data.For instance,


    String input = userData.getData("Sample", "Data1");

  > **Note:** To acess the data mapped to different iterations and subiterations, please refer the SampleScript.java file available in the Engine.  

----------

### ** How To Get The Properties Of A Web Element? **


It is possible to access the specific property of an element using the function **AObject.getObjectProperty** described below.


    String prop = AObject.getObjectProperty("pageName", "objectName", ObjectProperty.Id);

----------

### How To Define/Access A Variable's Value In Your Custom Function?

 Suppose you want to create a variable and define a value to it, you can go for `addVar(arg1,arg2)` function or `addGlobalVar(arg1,arg2)` function.

The value of a variable created in your test case can be accessed using the function `getVar(String key)` which is defined under the `com.cognizant.cognizantits.engine.commands.Command` java file (available in the Engine).


----------
