###Apex Base

Use this project to test your CI configuration with the Force.com platform.  The project has sample objects and provides an ant-force.com build script to test deployments.  Make sure that you configure the build.properties file with your environment settings.


## Pre-Requisites
* Java 1.7 or greater
* Apache **ant**
* Salesforce ant (ant-salesforce.jar)

## Example Task
From the command line: ant retrieveCode
The ant tasks will need a package.xml as input.  The objects that you want to retrieve must be defined in the package.xml file.
Make sure that you update the directories to reflect your workspace/desktop.
```
 <target name="retrieveCode">
        <!-- Retrieve the contents listed in the file codepkg/package.xml into the codepkg directory -->
        <sf:retrieve username="${sf.username}" password="${sf.password}" serverurl="${sf.serverurl}" retrieveTarget="codepkg" unpackaged="codepkg/package.xml" />
    </target>
    
```
