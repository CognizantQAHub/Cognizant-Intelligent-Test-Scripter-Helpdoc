# Cognizant Intelligent Test Scripter Migration guide


> **Audience** : The document intended to CITS 1.1 and 1.2 Users


## 1.	Pre-requisites** (Mandatory)


1.	Backup the CITS 1.1 (or) 1.2 Project folder and Custom Method Project/Jars to avoid data loss
2.	Ensure the project to be migrated, is a successfully working in CITS 1.1/1.2
3.	Download CITS 1.4 Zip from GitHub and Unzip
4.	It is recommended to have project from older version of CITS into CITS 1.4/Projects folder
5.	Install Java 11 
6.	Use Eclipse IDE for Java Developers version 4.12.0



## 2	Java and Eclipse Configuration

### 2.1.	Java

CITS 1.4 Supports only Java 11. Install Java 11 and configure the Java bin folder in System path.

**Note**: CITS 1.4 is not backward compatible with Java 8


### 2.2.	Eclipse Configuration

The below error would occur when configuring CITS 1.3 Engine code, if Java 11 is not configured in Eclipse.

![](faqImage\migrationguide_images\one.jpg)


To mitigate the Java Error, Add Java 11 in Eclipse > Installed JREs Window.

![](faqImage\migrationguide_images\two.jpg)



## 3.	Migration Steps

### 3.1.	Manual Steps

#### 1.	Cognizant Fastest Customization: 


As part of Cognizant Fastest Customization, user has to enter following list of capabilities in CITS 1.1/1.2. 


- Username
- Password
- seleniumVersion
- Packagename
- triggerId
- executionType
- consoleSessionId


From CITS 1.4 onwards, we had reduced the list of browser capabilities. Therefore, retain the following capabilities from Driver Settings dialog. Refer the below screenshot.


- Username
- Password
- servicerequestid
- seleniumversion



![](faqImage\migrationguide_images\three.jpg)



| CITS 1.1 and 1.2 | CITS 1.4  |
|------------|--------------|
| username, password  | username  |         
| packagename, servicerequestid   | password |           
| triggered,seleniumVersion     | servicerequestid |   
| executionType,consoleSessionId     | seleniumVersion |           



#### 2.	Exploratory Testing

In CITS 1.1 and 1.2, **Exploratory Testing > JIRA Configurations (Username and Password)** were encoded.If user has JIRA, configuration they recommended to configure it newly in CITS 1.4


#### 3.	Custom Method Migration

The Custom Method Project / Engine code recommended compiling and exporting as Jar again. 

Refer the below table for Custom Method Migration.

|**Custom Action** |**Migration Steps**|
|-------|-------|
|Custom Actions present in Custom Method Project | •	Create Custom Method Project in CITS 1.4 and copy the code from old CITS CM Project
•	Export it as Jar and verify in 1.4 IDE |
|Custom Actions present in Engine Project|•	Take a backup of old Engine Jar from lib folder
•	Copy the source from old Engine project to CITS 1.4 Engine Project
•	Export it as Engine Jar and verify in 1.4 IDE |
|Custom Actions using **Base64** encoding and decoding|Please change it to Encryption logic|




> **Note**: If Custom Methods have compile error because of new dependency jars, change the implementation of the method to match with current version.



### 3.2.	Automatic Migration

#### 1.	Tool Launch

Launch the CITS 1.4 tool using Run.bat and open the CITS 1.1 (or) 1.2 project. Refer the below screenshot

![](faqImage\migrationguide_images\four.jpg)

CITS 1.4 will automatically migrate CITS old version projects and make it 1.4 compatible project. Success notification shown in right corner of the tool. Check the tool logs (if there are any migration errors).

![](faqImage\migrationguide_images\five.jpg)

The following features gets automatically migrated.


#### 2.	Encryption

In Old version of CITS, we used Base64 Encoding. From CITS 1.4, the sensitive data(s) encrypted using AES 256 Algorithm. Therefore, the Base64 values in the following CITS 1.1 (or) 1.2 feature will be migrated to encryption values.

| **Feature (If Base64 data present)** |
|------------|
|Test Management Configuration|
|Test Data Cell/Test Step (Test Data Column)|
|Driver Settings|

Following CITS Actions using Base 64 values will be migrated to Encryption in CITS 1.4

| **Actions** |
|------------|
|setEncrypted|
|setEncryptedByJS|
|imgSetEncrypted|


#### 3.	Mail Settings

In CITS 1.4, we have introduced new property “**mail.smtp.starttls.required**” in mail configuration, which is used to enforce the usage of TLS (For Encrypting the SMTP traffic) in mail server. 

The below property is automatically added in CITS 1.4 Migration.


|Key|Value|
|-------|-------|
|mail.smtp.starttls.required|true|


> **Note**: The Connection fails if mail server does not have TLS Configuration


#### 4.	Test Management

In CITS 1.4, we have added Test Management Support for the below list of servers

- 	qTest
- 	JIRA On Cloud
- 	TestRail


These servers automatically gets added while Migration.


#### 5.	Excel Reporting

Excel Reporting feature in CITS 1.4 will start showing in old version of CITS Projects.

![](faqImage\migrationguide_images\six.jpg)


## 4.	Migration Checklist

1.	Check the Tool log file to ensure successful migration
2.	In Migrated Project , verify “**version=1.4**” sentence in “**.project**” file
3.	Verify the list of features in **Automatic Migration** are migrated successfully
4.	Check if Test Case / Reusable with Encrypted Actions execution is successful
5.	Perform Dry run from Migrated Project
6.	If Migration is not successful refer the Tool log for which feature the migration is broken
7.	If an error occurs, while converting Encoding > Encryption, in **Test data/Driver configuration/ Encrypted Action**. perform below steps,
 
- 	Delete an Encoded value in IDE (ends with “**Enc**”)
- 	Enter the correct value
- 	Right click and Choose an “**Encrypt**” option

8.	If an error occurs, while converting Encoding > Encryption, in Test Management Configuration and TM Settings

- 	Delete an Encoded value in IDE (Starts with “**TMENC**:”)
- 	Enter the correct value
- 	Right click and Choose an “**Encrypt**” option


9.	After migration ensure that project with the newly encrypted data (test data, password fields in test management tabs and similar data) are checked for its successful execution.






