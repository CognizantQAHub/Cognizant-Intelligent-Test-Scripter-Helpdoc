# Web Actions 

## Basic

### Set


**Description**: This function is used to enter data in an object.

**Input Format** : @Expected Text



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           |

Inputs in the Input column can be either **hardcoded** (in this case the data is preceded by a "**@**"), passed from the data sheet (**datasheet name : column name**) or passed from a variable value (**%variable name%**), as given in the above example.


### Click


**Description**: This function is used to perform click operation on an object.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |              |           |


### rightClick

**Description**: This function is used to perform right click operation on an object or in the browser.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser    |              |           |
| Object	 |              |			|  

### SubmitIfExists

**Description**: This function will check if an object exists. If the object exists, it will submit else it will ignore that step.




**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |              |           |



### RestartBrowser


**Description**:  This function is used to restart browser.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |              |           |


### changeWaitTime


**Description**: This function is used to change the default wait time(Default 10 sec). 
The default wait time for all the wait actions defined after **changeWaitTime** action will be the same as defined in the **changeWaitTime** action.

**Input Format** : @Time in seconds

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |


### setElementTimeOut


**Description**: This function is used to change the default timeout for Cognizant Intelligent Test Scripter's Object finding logic.(Default 10 second). The same action needs to be called with the default time (10 sec) as parameter when there is a need to switch to the default time for the succeeding steps.


**Input Format** : @Time in seconds

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |






### setBrowserSize


**Description**: This function will Set the browser size

**Input Format** : In pixels for example **@700x800** or **@700,800** or **@700 800**



**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |






### clickIfExists


**Description**:  This function will check if an element exists. If the element exists, it will click the element, else it will ignore that step.



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |



### SetIfExists


**Description**: This function will check if an element exists. If the element exists, data will be set for that element or that step will be ignored.

**Input Format** : @Expected Text


**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           |




### setAndCheck


**Description**: This function is used to enter data in object and check if the element's value matches with the entered value.

**Input Format** : @Expected Text



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           |





### setEncrypted


**Description**: This function is used to enter encrypted data to the object specified

**Input Format** : @Encrypted text



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |



> **Note**: If the data is passed from a data sheet, the data in the datasheet should be encrypted



### filler


**Description**: This is an empty action (does nothing), useful in some cases like looping/debugging.




**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser    |        |           |



### StartBrowser


**Description**: This function is used to start a specified browser.

**Input Format** : @Browser's Name



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |


### StopBrowser


**Description**: This function is used to stop the current browser




**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |



### AddVar


**Description**: This function is used to add a user-defined variable with a desired value and the scope of this variable is till the end of the test case in which it is defined

**Input Format** : @Expected Text 

**Condition** : %variable name%



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |  %Variable%         |
| Browser     | Sheet:Column |   %Variable%        |
| Browser     | %dynamicVar% |  %Variable%         |



### AddGlobalVar


**Description**: Same as **AddVar** but scope is till the end of the test set execution. 


**Input Format** : Text in Input 


**Condition** : %variable name%


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       | %Variable%  |
| Browser     | Sheet:Column | %Variable%  |
| Browser     | %dynamicVar% | %Variable%  |



### clear


**Description**: This function is used to clear the object's text




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |   |




### moveTo


**Description**: Move the browser view to the specified element.




**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |   |



### Open


**Description**: This function will open the URL provided by the user in the default browser

**Input Format** : @Expected Text



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |





### highlight


**Description**:  Make a rectangular border around the element

**Input Format** : Color in hexcode like **@#ff44ff**. If it is left empty red will be taken as default.



**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
|Object     |              |    |
| Object     | @value       |      |
| Object     | Sheet:Column |          |
| Object     | %dynamicVar% |           |




## Verify Element 

### verifyElementNotPresent


**Description**: This function will check if the specified element is not present in the web page ie. In the DOM .




**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |




### verifyElementNotSelected


**Description**: This function will check if the specified element is not selected.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |              |           |




### verifyElementNotDisplayed


**Description**: This function will verify if the element is not displayed.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |              |           |



### verifyElementNotEnabled


**Description**:  This function will check if the specified element is not enabled



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |              |           |


### verifyElementDisplayed


**Description**: This function will check if the object is displayed on web page.




**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |




### verifyHSrollBarPresent


**Description**: This function will check if the horizontal scrollbar is present.



**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |




### verifyHSrollBarNotPresent


**Description**: This function will check if the horizontal scrollbar is not present.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |





### verifyVSrollBarPresent


**Description**:  This function will check if the vertical scrollbar is present.



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |






### verifyVSrollBarNotPresent


**Description**: This function will check if the vertical scrollbar is not present.




**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |



### verifyElementPresent


**Description**: This function will check if the specified element is present in the web page ie) in the DOM.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |





### verifyElementSelected


**Description**: This function will check if the element is selected.




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |







### verifyElementEnabled


**Description**: This function will check if the element is enabled.




**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object    |        |           |




### verifyPageSource

**Description**: This function will check if the page source content of the current page is matching with the expected page source content provided by the user.

**Input Format** : @Expected PageSource Content



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |



## Browser Utility

### maximize

**Description**:This function is used for maximizing the browser window.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |


### authenticate

**Description**:This function is used for handing the authentication window. Supports IE only. If executed for other browsers the script will fail. You can skip this by setting **optional** value in the Condition field.

**Input Format** : @username##password

**Condition** : optional

**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |   @data     |           |
| Browser     |   @data     |optional   |


## By Label

### setInputByLabel

**Description**: This function will set an input element, with the given data,  that is adjacent to the provided label element.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           |


### clickInputByLabel

**Description**: This function will click an input element that is adjacent to the provided label element.





**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |



### clickInputByText


**Description**: This function will click an input element that is adjacent to the provided text 

**Input Format** : @Expected Text



**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |




### submitInputByLabel


**Description**: This function will submit input element adjacent to the provided label element.




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |       |           |






### assertElementTextContainsByLabel

**Description**: This function will check if the text of the input element adjacent to provided label element contains the given text(in the Input Column) 


**Input Format** : @Expected Text.


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           |



###  assertElementTextByLabel

**Description**:  This function will check if the text of the input element adjacent to provided label element equals the given text(in the Input Column)



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           |





## Verifications

### verifyVariableFromDataSheet

**Description**: This function will validate the value of a given variable against data in a datasheet cell.

**Input Format** : Datasheet:column

**Condition**: %variable%

**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | sheet:column       | 	%variable%          |



### verifyCookiePresent

**Description**: This function will check if the cookie is present. Search will occur based on the cookie name.

**Input Format**:@Cookie name.



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |



### verifyCookieByName


**Description**: This function will search for the cookie by name and then compare the cookie value with the user-provided value.

**Input Format** : @Cookie name:Cookie value.




**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           |





### verifyAlertText


**Description**: This function will match the alert text with the expected value.

**Input Format** : @Expected Text



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |





### verifyAlertPresent

**Description**:This function will verify the presence of an alert.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |




###  verifyVariable



**Description**:  This function will check if the stored variable value matches the expected value.

 **Input Format** : @VariableName=Value



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value        |           |




### verifyTextPresentInPage

**Description**: This function will search for the text inside html tag of the page.


**Input Format**:@Expected Text



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |







## Wait for

### waitForElementToBeVisible

**Description**:  This function will wait till the element is visible on the screen

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |     Time in seconds      |


### waitForElementToBeInVisible

**Description**: This function will wait till the element becomes invisible.

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |        Time in seconds     |



### waitForElementToBeClickable


**Description**: This function will wait till the element becomes clickable.

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |        Time in seconds     |



### waitForElementToBeSelected

**Description**: This function will wait till the element is selected

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |        Time in seconds     |






### waitForElementToContainText

**Description**: This function will wait till the element contains the given text


**Input Format** : @Text to check.

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "**ChangeWaitTime**" function with the desired wait time



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |     Time in seconds       |
| Object     | Sheet:Column |  Time in seconds          |
| Object     | %dynamicVar% |   Time in seconds         |


### waitForElementToContainValue

**Description**:  This function will wait till the element contains the given value


**Input Format** : @Text to check.

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |     Time in seconds       |
| Object     | Sheet:Column |  Time in seconds          |
| Object     | %dynamicVar% |   Time in seconds         |



### waitForElementToBePresent

**Description**: This function will wait till the element loads in the DOM.

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        | 	Time in seconds          |



### waitForFrameAndSwitch

**Description**:  This function will wait for the frame to be available and switch to it.

**Input**: @id or name or index

The input is optional if you choose to give the web element (the frame itself) under the object name.This element can be added as an object under the Object repository.

If the object name used is "Browser", then you need to give the frame **id or name or index** under the input column

**Condition** : Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "**ChangeWaitTime**" function with the desired wait time


**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |   frame id or name or index     |   Time in seconds  (optional)|
|Frame itself as an element| |Time in seconds  (optional)|



### waitForPageLoaded

**Description**: This function will wait till the page is loaded. **Note: This is not for Ajax calls**

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time




**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |   Time in seconds        |




### waitForAlertPresent

**Description**:  This function will wait for alert to appear on the page.

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |   Time in seconds        |




### waitForTitleToBe


**Description**:  This function will wait till the title of the page matches with the given text.

**Input Format** : @Text to check

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |  Time in seconds         |
| Browser     | Sheet:Column |  Time in seconds          |
| Browser     | %dynamicVar% |     Time in seconds       |








### waitForTitleToContain


**Description**:  This function will wait till the title of the page has the given text.

**Input Format** : @Text to check

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |  Time in seconds         |
| Browser     | Sheet:Column |  Time in seconds          |
| Browser     | %dynamicVar% |     Time in seconds       |





### waitTillCustomScript


**Description**:   This function will wait till the given javascript condition returns true. It is applicable only for JavaScript functions that return a boolean value.

**Input Format** : @Javascript to evaluate 

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |  Time in seconds         |
| Browser     | Sheet:Column |  Time in seconds          |
| Browser     | %dynamicVar% |     Time in seconds       |




### clickAndWait


**Description**: This function is used for clicking and waiting for the page to be loaded.



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |



### waitForElementSelectionToBeTrue

**Description**:  This function will wait till the element selection becomes true

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use "ChangeWaitTime" function with the desired wait time



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        | Time in seconds          |



### waitForElementSelectionToBeFalse


**Description**: This function will wait till the element selection becomes false.

**Condition** :Time in seconds [Optional]. If left empty default waitTime[10 sec] will be considered. If you want to increase the default wait time then you can use **ChangeWaitTime** function with the desired wait time



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        | Time in seconds          |




## Switch to 

To switch to a new frame, you can either go for these actions or you can set the frame id or name under the frame property of your object in the UI of the tool.


### switchToFrameByIndex


**Description**:  This function is used for switching control to a frame by given index.

**Input Format** :  @Frame's Index



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |            |
| Browser     | %dynamicVar% |          |


### switchToWindowByTitle


**Description**:   This function is used for switching control to a window by  given title.

**Input Format** : @Window's Title



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |            |
| Browser     | %dynamicVar% |          |




### switchToWindowByIndex


**Description**:  This function is used for switching control to a window by  given index.

**Input Format** : @Window's Index




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |          |
| Browser     | Sheet:Column |            |
| Browser     | %dynamicVar% |           |



### switchToFrame


**Description**:  This function is used for switching control to  frame with id or name specified.

**Input Format** : @Frame Name or Id



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |          |
| Browser     | Sheet:Column |            |
| Browser     | %dynamicVar% |           |



### switchToWindowByTitleStartsWith


**Description**: This function is used for switching control to another window whose title begins with the provided data.

**Input Format** : @Expected text



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |          |
| Browser     | Sheet:Column |            |
| Browser     | %dynamicVar% |           |



### switchToWindowByTitleContains


**Description**: This function is used for switching control to another window whose title has the provided data.

**Input Format** : @Expected text





**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |          |
| Browser     | Sheet:Column |            |
| Browser     | %dynamicVar% |           |






### switchToWindowByTitleEndsWith


**Description**: This function is used for switching control to another window whose title ends with the provided data

**Input Format** : @Expected text



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |          |
| Browser     | Sheet:Column |            |
| Browser     | %dynamicVar% |           |






### switchToWindowByTitleMatches


**Description**: This function is used for switching control to another window whose title matches with the provided data (can use regex also). 

**Input Format** : @Expected text



**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |          |
| Browser     | Sheet:Column |            |
| Browser     | %dynamicVar% |           |


### switchToDefaultContent


**Description**:  This function is used for switching control to the default window.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |




### createAndSwitchToWindow


**Description**:  This function is used to create a new window and then for switching control to the newly created window.

**Input Format** :  @url to open after creating a new window. If this input column is empty then empty url will be loaded



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |
| Browser     | @value       |           |
| Browser     | Sheet:Column |        |
| Browser     | %dynamicVar% |         |



### closeAndSwitchToWindow


**Description**:  This function will close the current window and switch back to the default window.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser   |       |            |





## Drop down

### selectByIndex

**Description**:  This function will select an option from a drop down whose index matches the given index.

**Input Format** :  @Expected Value's Index



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### deSelectAll

**Description**:  This function will clear all the selected entries. This is only valid when there is support for multiple selections in the drop down.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |       |          |



### selectByVisibleText

**Description**:  This function will select an option from a drop down whose visible text matches the given text.

**Input Format** :  @Expected Value's Index


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |



### selectMultipleByText

**Description**:  This function will select all options that display the text matching the given text.

**Input Format** :  @Expected Text1,Expected Text2


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |



### selectMultipleByValue

**Description**:  This function will select all options that have value matching the given value.

**Input Format** :  @Expected value1,Expected value2



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### selectByValue

**Description**:  This function will select an option from a drop down whose value ('value' attribute of option HTML tag) matches the given value.

**Input Format** :  @Expected Text


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### selectMultipleByIndex

**Description**:  This function will select all multiple options that have index matching the given set of indices.

**Input Format** : @Expected index1,Expected index2


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### deSelectByVisibleText

**Description**:  This function will de-select an option that displays text matching the given text.

**Input Format** :  @Expected Text


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### deSelectByValue

**Description**:  This function will de-select an option that has value matching the given value.

**Input Format** : @Expected value



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### deSelectByIndex

**Description**:  This function will de-select an option that has index matching the given index.

**Input Format** :  @Expected index


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### assertSelectContains

**Description**: This function will assert if the selected element from the drop down matches the user-specified input.

**Input Format** :  @Expected Text


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### selectValueFromUnorderedList

**Description**:  This function will select the value based on the visible text from an unordered list.

**Input Format** :  @Expected Text


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### selectIndexFromUnorderedList

**Description**:  This function will select the value from an unordered list based on the index.

**Input Format** :  @Expected Value's index


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### deSelectMultipleByText

**Description**:  This function will deselect all options that display text matching the given text.

**Input Format** :  @Expected Text1,Expected Text2


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### deSelectMultipleByValue

**Description**:  This function will de-select all options that has value matching the given values.

**Input Format** :  @Expected value1,Expected value2


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### deSelectMultipleByIndex

**Description**:  This function will de-select all options that has index matching the given indices. This is done by examining the "index" attribute of an element, and not merely by counting.If there is no index attribute used then option identified by the count

**Input Format** :  @Expected index1,Expected index2


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### selectAll

**Description**:   This function will select all options from a select element.





**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |          |
|



## Table


### getCellValue

**Description**:   This function is used to get data from the desired cell of the web table and store it in a user-defined variable.


**Input Format** : @RowNo;ColNo,%variableName%


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |



### getColCount

**Description**:   This function is used to count the number of columns in a desired row in a web table and store it in a user-defined variable.


**Input Format** : @RowNo,%variableName%

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |


### getRowNumber

**Description**:   This function is used to get the number of the row of the desired data in a web table and store it in a user-defined variable.


**Input Format** : @Expected Data,%variableName%



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |



### getColNumber

**Description**:  This function is used to get the column number of the desired data in a web table and store it in a user-defined variable.


**Input Format** : @Expected Data,%variableName%



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |


### getRowCount

**Description**:   This function is used to count the number of rows in a web table and store it in a user-defined variable.


**Input Format** : %variableName%


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


## Relative Command


### set_Relative


**Description**:   This function will set data in an element based on the property of its parent (Useful when a page has objects with similar properties but their parents are unique).




**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |



### click_Relative


**Description**:   This function will click an element based on the property of its parent (Useful when a page has objects with similar properties but their parents are unique)



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |          |


## Dynamic Object

### setglobalObjectProperty

**Description**:   This function is used to customize all objects’ property based on the requirement at runtime.User can give his desired value as an input which will replace the matching condition in the object's property. **For more details, please refer to Help>Faq>Dynamic Object Handling>How to change Object property at runtime? **

**Input Format** :Input Column : @User Defined Text String

 **Condition Column** : #Variable name


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |      %var%     |
| Browser     | Sheet:Column |      %var%       |
| Browser     | %dynamicVar% |      %var%      |


### setObjectProperty

**Description**:  This function is used to customize any object property based on the requirement during the runtime. User can give a desired value as an input which will replace the matching condition in the object property. **For more details, refer to: Help>Faq>Dynamic Object Handling>How to change Object property at runtime?**

**Input Format** : @User Defined Text String

**Condition Column** : #Variable name




**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |   %var%       |
| Object     | Sheet:Column |    %var%         |
| Object     | %dynamicVar% |   %var%         |



## Checkbox

### uncheck

**Description**:  This function will uncheck the specified check box.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |          |

### checkAllCheckBoxes

**Description**:  This function will check all the checkboxes on a page.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |          |

### check

**Description**:  This function will check the specified checkbox element.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |          |


## JS Commands

### clickByJS


**Description**:  This function will use JavaScript to click an object (useful when selenium functions do not work).



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |          |


### setByJS

**Description**:  This function will use JavaScript to set data in an object (useful when selenium functions do not work).

**Input Format** : @Expected data

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |


### setEncryptedByJS

**Description**:  This function will use JavaScript to set encrypted data in an object (useful when selenium functions do not work).

**Input Format** : @Expected encrypted data



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |            |
| Object     | %dynamicVar% |           |




### clearByJS


**Description**:  This function will use JavaScript to clear an objects text content  (useful when selenium functions do not work).


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |          |


### selectByJS


**Description**: This function is used to select a given option from a drop down and is useful when selenium functions do not work.  


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           |


### assertInsideBounds

**Description**: To function is used to check if the given object is inside the boundary.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |          |


### executeEval

**Description**: This function is used to execute the JavaScript commands 

**Input Format** : @java script scripts

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |          |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           |


## AssertElement 


### assertElementNotPresent


**Description**: This function will check if the specified element is not present in the web page ie. In the DOM itself.


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |




### assertElementNotSelected


**Description**:  This function will check if the specified element is not selected


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |              |           |




### assertElementNotDisplayed


**Description**: This function will check if the specified element is not displayed.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |              |           |



### assertElementNotEnabled


**Description**:  This function will check if the specified element is not enabled.


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |              |           |


### assertElementDisplayed


**Description**:  This function will check if the object is displayed on web page.


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |







### assertHScrollBarPresent


**Description**: This function will check if horizontal scrollbar is present.


**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |







### assertHScrollBarNotPresent


**Description**: This function will check if horizontal scrollbar is not present.


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |




### assertVScrollBarPresent


**Description**:   This function will check if vertical scrollbar is present.


**Example:**




| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |




### assertVScrollBarNotPresent


**Description**: This function will check if vertical scrollbar is not present.


**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |



### assertElementPresent


**Description**:  This function will check if specified element is present in the web page ie. In the DOM of the page


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |





### assertElementSelected


**Description**: This function will check if the element is selected.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |







### assertElementEnabled


**Description**: This function will check if the element is enabled.



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object    |        |           |




### assertPageSource

**Description**: This function will check if the page source content of the current page is matching with the expected page source content provided by the user.

**Input Format** : @Expected PageSource content

**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |




## Common methods



### refreshDriver

**Description**: This function will refresh the current web page.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |


### forward

**Description**:  This function is used for navigating forward to next page.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |




### submit

**Description**:  This function will Submit an element.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |




### dragElement

**Description**: This function will drag the specified element(under Object column) which can be later dropped on to other element by using **dropElement**.




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |



### dropElement

**Description**: This function will drop the element which is dragged by using **dragElement** over the object specified here.




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |



### dragAndDropBy

**Description**: This function will drag and drop an object by specified coordinates in the input column. 

**Input Format** :@x-coordinate,y-coordinate



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           |



### addCookie

**Description**:  This function will add a cookie defined in the input column.

**Input Format** : @Cookie Name:Cookie Value



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |



### back

**Description**: This function is used for navigating to the previous page.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |




### pause

**Description**:This function is used for giving a pause (Thread.sleep) in execution.

**Input Format** :  @Time in miliseconds



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |



### doubleClickElement

**Description**: This function will double-click on an object.





**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |




### mouseOverElement

**Description**: This function will perform the mouse over action on the object.




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |


### dragToAndDropElement

**Description**: This function is used to perform drag and drop operation. Specify the object which you want to drag, in the 'Object' column and specify the object on which you want to drop ,in the 'input' column.

**Input Format** : @PageName:ObjectName(Destination)



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |




### releaseElement

**Description**:  This function is used to release the element held by **clickAndHoldElement**



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |        |           |


### saveScreenshot

**Description**: This function will capture the screenshot and save in the specific location.

**Input Format** : @File destination (eg. @D:\filename.png)



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |

### takeScreenshot

**Description**:  This function will take a screenshot


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |        |           |


### saveElementScreenshot

**Description**: This function will take a screenshot of the web element and save it in the location specified under the Input column. If no location is specified then the default location is **your project folder\ObjectRepository\Pagename\objectname**.

This function can also be used to save screenshots for the entire set of page objects, under the default location which is inside the **ObjectRepository** folder.


**Input Format (Optional)** : @File destination (eg. @D:\foldername) 




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |  @File destination(optional)     |           |
| Browser     |  @PageName from the object repository     |           |





### storeCurrentUrl

**Description**:  This function will store the current URL into a user defined variable.

**Input Format** : %variable name%




**Example:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | %dynamicVar% |           |


### storeTextinDataSheet

**Description**: This Function will store the element's text into respective column of a given datasheet.

**Input Format** : @Expected datasheet name:column name



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |  Sheet:Column |           |



**Note**: Ensure that your data sheet doesn't contain column names with spaces.


### storeTextPresent

**Description**: This function will check if the element has expected text and store the flag 'True' or 'False' in the variable.

**Input Format** : @Expected text

**Condition** : %variable name%



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |    @value     |    %var%       |
| Object     |  Sheet:Column |       %var%     |
| Object     |  %dynamicVar%  |      %var%      |


### storePageSource

**Description**: This function will store the page source content into a user-defined variable.

**Input Format** : %variable name%




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    %variable name%     |           |



### storeElementSelected

**Description**:  This function will check if the element is selected and store the flag 'True' or 'False' in the variable.

**Input Format** : %variable name%



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |    %variable name%     |           |



### storeElementAttribute

**Description**:  This function will store the element's attribute value into a user-defined variable.

**Input Format** : @Elements_Attribute_Name

**Condition** : %variable name%



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |    @value     |    %var%       |
| Object     |  Sheet:Column |       %var%    |
| Object     |  %dynamicVar%  |    %var%       |



### storeElementValue

**Description**:   This function will store the element's ‘value‘ attribute into a user-defined variable.

**Input Format** : %variable name%


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |    %variable name%     |           |


### storeCookiePresent

**Description**:   This function will check if the given cookie is present and store the flag 'True' or 'False' in the variable.

**Input Format** : @cookieName

**Condition**: %variable%



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |


### storeCookieByName

**Description**:   This function will store the given cookie's value in the variable.

**Input Format** : @cookieName 

**Condition**: %variable%



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |    %variable%       |





### storeAlertText

**Description**:   This function will store alert text into a user defined variable.


**Input Format**: %variable%



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |



### storeAlertPresent

**Description**:   This function will check if alert is present and store the flag 'True' or 'False' in a given variable.

**Input Format**: %variable%



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |   %variable%      |           |




### sendKeysToElement

**Description**:  This function is used to perform keyboard events with respect to object.

**Input Format** :  @Keyboard_Keys(like Enter,Shift,Ctrl,Ctrl+A) 




**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |    @value     |           |
| Object     |  Sheet:Column |           |
| Object     |  %dynamicVar%  |           |


### sendKeysToWindow

**Description**:  This function is used to perform the keyboard actions with respect to window.

**Input Format** : @Keyboard_Keys(like Enter,Shift,Ctrl,Ctrl+T) 



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |

### deleteCookie

**Description**:  This function will delete the cookie specified by the user.

**Input Format** : @Cookie Name



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |

### answerAlert

**Description**:  This function is used for switch control to alert and answer it.


**Input Format** : @Expected Text



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |

### acceptAlert

**Description**:  This function is used for switch control to alert and accept it.


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |         |           |


### dismissAlert

**Description**:  This function is used to switch control to alert and  to dismiss it.


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |         |           |

### storeVariable

**Description**:  This function will store the given data (in the input column) into a user-defined variable.This function is same as **AddVar** action.


**Input Format** : @Desired Value

**Condition**: %variable name%



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |


### storeVariableInDataSheet

**Description**:  This function will store the variable's value (as given in the condition column) in the given data sheet and data column

**Input Format**: Sheetname:columnname

**Condition**: %variable name%



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |  Sheet:Column |   %var%        |





### storeTitle

**Description**:   This function will store the current web page title into a user-defined variable.

**Input Format** : %variable name%


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |



### storeText

**Description**:  This function will store the element's text into a user-defined variable.

**Input Format** : %variable name%


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     |  %dynamicVar%  |           |


### storeEval

**Description**:  Function to store a Javascript expression's value in a variable.

**For example** if you have a variable as **'a' and 'b'** and want to add them and store the sum in a variable, you can follow the following syntax.

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @var a=20;var b=30;return c=a+b;  |   %var%    |

Now the value 50(a+b), will be stored in var.

**Input Format** :  javascript 


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |    %var%       |

### print

**Description**:  This function can be used for printing expected data in report.

**Input Format** : @Expected Text or variable can also be printed like %var_name%


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |


### close

**Description**:  This function will close the selenium Web Driver.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |         |           |




## Scroll

### scrollHorizontallyTo

**Description**:  This function will scroll horizontally to a user defined position.

**Input Format** : @left|right|number


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |


### scrollVerticallyTo

**Description**:  This function will scroll vertically to a user defined position.


**Input Format** : @left|right|number



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |



### scrollToBottom

**Description**:  This function will scroll to the bottom of the page



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |         |           |



### scrollTo

**Description**:  This function will scroll to a user specified position. 

**Input Format** :  @x co-ordinate,y co-ordinate



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |

### scrollToTop

**Description**:  This function will scroll to the top of the page



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |         |           |


### scrollToLeft

**Description**:  This function will scroll to the left of the page


**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |         |           |


### scrollToRight

**Description**: This function will scroll to the right of the page



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |         |           |



## Assertions

### assertTextPresentInPage


**Description**:  This function will search for the expected text within the html tag of the page and assert the same

**Input Format** :   @Expected Text



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |



### assertVariable


**Description**:  This function will assert a stored variable's value with the value given by the user.

**Input Format** : @%var_name%=Expected Value



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |

### assertCookiePresent


**Description**: This function will assert the presence of a cookie by it's specified name and store the result in a variable.

**Input Format** :   @CookieName



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |   %variable%        |
| Browser     |  Sheet:Column |    %variable%       |
| Browser     |  %dynamicVar%  |   %variable%        |

### assertCookieByName


**Description**:  This function will assert the cookie's (the name of the cookie is given is specified in the input column) value with the one in the input column

**Input Format** :   @CookieName:CookieValue



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @data     |          |


### assertAlertText

**Description**:  This function will assert the text present in alert with the given text.


**Input Format** :  @Expected Text



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |           |
| Browser     |  Sheet:Column |           |
| Browser     |  %dynamicVar%  |           |



### assertAlertPresent

**Description**:  This function will assert the presence of an alert



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |         |           |


### assertEval

**Description**:   This function will assert if the evaluated javascript expression equals the expected value provided.

**Input Format** :   @javascript:expectedvalue.



**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |    @value     |         |
| Browser     |  Sheet:Column |       |
| Browser     |  %dynamicVar%  |          |



### assertVariableFromDataSheet

**Description**:   This function will check if the variable given in the condition column has a value equals to the value from the datasheet mentioned in the input column. 

**Input Format** :   Datasheet name:Column name

**Condition Format**: %Variable name%

**Example:**



| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     |  Sheet:Column |    %variable%     |




## Title


### assertTitleIStartsWith

**Description**: This function will validate if the current page title begins with the user-provided data. This function will ignore case of the user-provided data.

**Input Format** : @Expected text

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |



### assertTitleEquals


**Description**:  This function will validate if the title of the current page is equals the user-provided data.

**Input Format** : @Expected text

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           |

### assertTitleContains


**Description**:  This function will validate if the title of the current page has the user-provided data.

**Input Format** : @Expected text

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           | 

### assertTitleStartsWith


**Description**:   This function will validate if the title of the current page begins with the user-provided data.

**Input Format** : @Expected text

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           | 


### assertTitleEndsWith


**Description**:   This function will validate if the title of the current page ends with the user-provided data.

**Input Format** : @Expected text

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           | 



### assertTitleMatches


**Description**:   This function will validate if the title current page matches  the user-provided data. You can also use regular expression in the Input field.


**Input Format** : @Expected text

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           | 


### assertTitleIEquals


**Description**:  This function will validate if the title of the current page is equals the user-provided data. This function will ignore case of user provided data.

**Input Format** : @Expected text


**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           | 

### assertTitleIContains

**Description**:  This function will validate if the title of the current page contains the user-provided data. This function will ignore case of the user-provided data.

**Input Format** : @Expected text

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           | 

### assertTitleIEndsWith

**Description**:  This function will validate if the title of the current page ends with the user-provided data. This function will ignore case of the user-provided data.

**Input Format** : @Expected text

**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Browser     | @value       |           |
| Browser     | Sheet:Column |           |
| Browser     | %dynamicVar% |           | 


## Attribute

### assertElementAttrEquals

**Description**: This function will validate if specified attribute for an element is equal to the user-provided data.

**Input Format** : attributeName attributeValue



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 

### assertElementAttrContains

**Description**:  This function will validate if the specified attribute for an element contains the user-provided data.

**Input Format** : attributeName attributeValue



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 

### assertElementAttrStartsWith

**Description**:   This function will validate if specified attribute for an element begins with the user-provided data.

**Input Format** : attributeName attributeValue



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 

### assertElementAttrEndsWith


**Description**:   This function will validate if specified attribute for an element ends with user provided data.

**Input Format** : attributeName attributeValue



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 


### assertElementAttrMatches


**Description**:    This function will validate if specified attribute for an element matches with the user-provided data. You can also use regular expression in the Input field.

**Input Format** : attributeName attributeValue



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 


### assertElementAttrIEquals


**Description**:    This function will validate if specified attribute for an element is equals the user-provided data.This function will ignore case of the user-provided data.

**Input Format** : attributeName attributeValue



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 


### assertElementAttrIContains


**Description**:   This function will validate if specified attribute contains user-provided data.This function will ignore case of the user-provided data.

**Input Format** : attributeName attributeValue



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 



### assertElementAttrIStartsWith


**Description**:    This function will validate if specified attribute for an element begins with the user-provided data. This function will ignore case of the user-provided data.

**Input Format** : attributeName attributeValue



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 

### assertElementAttrIEndsWith


**Description**:  This function will validate if specified attribute for an element ends with the user-provided data. This function will ignore case of the user-provided data.

**Input Format** : attributeName attributeValue



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 


### verifyElementAttribute


**Description**: This function will check if the value of the specified attribute of the element matches the user provided value.

**Input Format** : attributeName attributeValue



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 

## Text

### assertElementTextEquals


**Description**:  This function will validate if a specified element text is equal to the user-provided text.

**Input Format** : @Expected Text



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 

### assertElementTextContains


**Description**:  This function will check if an element text contains the expected text.

**Input Format** : @Expected Text



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 




### assertElementTextStartsWith

**Description**:  This function will validate if specified element text starts with user provided data.

**Input Format** : @Expected Text



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 


### assertElementTextEndsWith

**Description**:   This function will validate if the specified element text ends with user-provided data.

**Input Format** : @Expected Text



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 



### assertElementTextMatches


**Description**:  This function will validate if a specified element text matches with the user-provided data. You can also use regular expression in the Input field .

**Input Format** : @Expected Text



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 


### assertElementTextIEquals

**Description**:  This function will validate if a specified element text is equal to the user-provided data. This function will ignore case of the user-provided data.

**Input Format** : @Expected Text



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 

### assertElementTextIContains

**Description**:  This function will validate if a specified element text contains the user-provided data. This function will ignore case of the user-provided data.

**Input Format** : @Expected Text



**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 


### assertElementTextIStartsWith

**Description**: This function will validate if a specified element text begins with the user-provided data. This function will ignore case of the user-provided data.


**Input Format** : @Expected Text




**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 


### assertElementTextIEndsWith

**Description**:  This function will validate if a specified element text ends with the user-provided data. This function will ignore case of the user-provided data.


**Input Format** : @Expected Text




**Example:**

| ObjectName | Input        | Condition |
|------------|--------------|-----------|
| Object     | @value       |           |
| Object     | Sheet:Column |           |
| Object     | %dynamicVar% |           | 




## URL

### assertUrlEquals


**Description**:This function will validate if the current URL equals the user-provided data.

**Input Format** : @Url value 



**Syntax:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
|   Browser     | 	@value  |   	   |
|   Browser     | 		Sheet:Column  |   	   |
|   Browser     | 	%dynamicVar%  |   	   |

### assertUrlContains


**Description**:This function will validate if the current URL has the user-provided data.

**Input Format** : @Url value 



**Syntax:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
|   Browser     | 	@value  |   	   |
|   Browser     | 		Sheet:Column  |   	   |
|   Browser     | 	%dynamicVar%  |   	   | 

### assertUrlStartsWith


**Description**:This function will validate if the current URL beings with the user-provided data.

**Input Format** : @Url value 



**Syntax:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
|   Browser     | 	@value  |   	   |
|   Browser     | 		Sheet:Column  |   	   |
|   Browser     | 	%dynamicVar%  |   	   | 

### assertUrlEndsWith


**Description**:This function will validate if the current URL text ends with user-provided data.


**Input Format** : @Url value 



**Syntax:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
|   Browser     | 	@value  |   	   |
|   Browser     | 		Sheet:Column  |   	   |
|   Browser     | 	%dynamicVar%  |   	   | 

### assertUrlMatches


**Description**: This function will validate if the current URL matches with the user-provided data. You can also use regular expression in the Input field.

**Input Format** : @Url value 



**Syntax:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
|   Browser     | 	@value  |   	   |
|   Browser     | 		Sheet:Column  |   	   |
|   Browser     | 	%dynamicVar%  |   	   | 

### assertUrlIEquals


**Description**: This function will validate if the current URL is equal to the user-provided data. This function will ignore case of user-provided data.

**Input Format** : @Url value 



**Syntax:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
|   Browser     | 	@value  |   	   |
|   Browser     | 		Sheet:Column  |   	   |
|   Browser     | 	%dynamicVar%  |   	   | 


### assertUrlIContains


**Description**: This function will validate if the current URL has the user-provided data.This function will ignore case of user-provided data.

**Input Format** : @Url value 



**Syntax:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
|   Browser     | 	@value  |   	   |
|   Browser     | 		Sheet:Column  |   	   |
|   Browser     | 	%dynamicVar%  |   	   | 

### assertUrlIStartsWith


**Description**: This function will validate if the current URL begins with the user-provided data. This function will ignore case of user provided data.

**Input Format** : @Url value 



**Syntax:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
|   Browser     | 	@value  |   	   |
|   Browser     | 		Sheet:Column  |   	   |
|   Browser     | 	%dynamicVar%  |   	   | 



### assertUrlIEndsWith


**Description**: This function will validate if the current URL ends with the user-provided data. This function will ignore case of user-provided data.

**Input Format** : @Url value 



**Syntax:**


| ObjectName | Input        | Condition |
|------------|--------------|-----------|
|   Browser     | 	@value  |   	   |
|   Browser     | 		Sheet:Column  |   	   |
|   Browser     | 	%dynamicVar%  |   	   | 



