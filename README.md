# RightMoveWork
Searching of non feature property

Script Instructions
1 \src\test\java

1.1 >> actions Folder

Common class >> This is a common class in which i created functions that will use repeatedly in the whole project like launch and exit browser, URL, getvalue from config file, Select value from dropdown. These are the reusable functions.

1.2 pageObject Folders

RightMovesPO >> in this file all the locators are stored in variables which we are using using for the scenario. In future if any locator is changed then you just need to change the locator as each locator is given a variable name so there is no need to update locator in code. It will automatically fetch by locator variable name.
1.3 Step Definition
This is the main folder for scripts
stepDefinition >> Test execution starts from this file. This is working with cucumber option. Here we are giving the path of the feature file. Here we need to gives the tags which automatically detect the feature file scenario (You can see in feature file). Here we can also use TestNG annotation to run the execution in a symmetric way.

RightMove.java >> in this class test script is written for RightMove case study.

2. \src\test\resources
2.1 configuration
Config.properties >> in this file all inputs are stored. Here you can change values as per your scenario.
2.2 feature
In this feature file we have the steps, mentioned as per the requirement. There should not be any change in the feature file as it will affect the test cases and break. We are using gherkin here so if any mismatch between scenario and feature file then it will not run. In all feature files we give a tag name that will be used in stepDefinition class to map the feature file with scenario to be executed. Tag name should not be mismatch at both file (feature and stepDefinition).

3. Driver Folder In this folder we store chromedriver that will help us to launch the chrome browser. In Common class you can see we give the path of that chromedriver. There are also other drivers for IE, Safari, and Firefox etc. but for now script is written for only chrome browser.
4. Logs Folder After completing the execution a file will be updated in this folder and you can check the logs(Steps) for all script execution.
5. Results  After completing the execution a file will be updated in this folder and you can check the execution status like how many test cases pass, Fail and error.
6.  target   these files are generated at run time (No Need )
7. test-output this file is also generated during execution and also provides TestNG report. No need as we are using Cucumber+Extent report.
8. pom.xml  In this file we give all dependencies/library. It automatically fetches dependencies from the internet. We can also call it dynamic dependencies.
9. Run.bat  This is shortcut file to execute the tests as we just double click to run test. In this file we wrote the command to run maven. If the project is imported in eclipse IDE then you can also run it by run button or any other ide like Intellij
10. testing.xml  In this file we give the class name which is needed to execute. In this project stepDefinition file is the main class from where all the test cases are executed by given tag name. So here we only mention this class.

