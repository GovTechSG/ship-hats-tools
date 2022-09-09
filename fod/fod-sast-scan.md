# SAST Scan


Complete the following steps to conduct a SAST scan:

1. [Package source code in ZIP file](#package-source-code-in-zip-file)
1. [Upload ZIP to FOD server for processing and scanning](#upload-zip-to-fod-server-for-processing-and-scanning)
1. [Generate report based on scan results](#generate-report-based-on-scan-results)

Two Gitlab templates are available for SAST scans:

- One specifically for MSBuild which will be utilising the Gitlab Windows runner. - TODO
- Another for all other language agnostic languages such as Python, Ruby which will utilise the Linux runner. You can access them here: https://gts.gitlab-dedicated.systems/templates/ship-hats-templates/-/tree/main/templates#file-gitlab-ci-run-fod-sastyml

Please use the MSBuild template only for .NET/MSBuild projects as the template is specifically catered for it.

## Package source code in ZIP file


FOD uses scancentral to package the source code into a ZIP file. The translation and scanning will be done in the SaaS server. 

Below are some examples on how to package your source code based on the programming language in use.

> **Note:** Packaging dependencies in your zip file will include your SAST scan duration. We recommend that you use Nexus IQ to scan your software dependencies.

|Objective|Command|
|---|---|
Create a package from a Gradle project |`scancentral.bat package -bt gradle -o package.zip`
Create a package from a Maven project with a custom pom.xml|	`scancentral.bat package -bt mvn -bf myCustomPom.xml -o package.zip`
Create a package from an MSBuild project 	|`scancentral.bat package -bt msbuild -bf mySolution.sln -o package.zip`
Create a package from a JavaScript/TypeScript project	|`scancentral.bat package -bt none - o package.zip`
Create a package from a JavaScript/TypeScript project and include the node_modules <br> <br> **Caution:** This may greatly increase the package size as well as the scan time.|`scancentral.bat package -bt none - -scan-node-modules -o package.zip`
Create a package from a Python 3 project	|`scancentral.bat package -bt none - yv 3 -pyr -o package.zip`
Create a package from a Ruby project	|`scancentral.bat package -bt none - o package.zip`
Create a package from a PHP 7.1 project	|`scancentral.bat package -bt none - hv 7.1 -o package.zip`
Create a package from other unlisted projects	|`scancentral.bat package -bt none - o package.zip`

## Upload ZIP to FOD server for processing and scanning
A utility tool (https://github.com/fod-dev/fod-uploader-java) is used to upload your ZIP file to the FOD server. Based on the table below, assuming you have a Python 3 project, your FOD_UPLOADER_OPTS should look something like this.

```
FOD_UPLOADER_OPTS: "-apf -ts 10 -l 18"
```

`-apf` is recommended since it will fail your build whenever your scan results fails the security policy set in FOD.

|Parameter|	Description|
|---|---|
-ts	|Technology stack as an integer: <br><br>1 (.NET), 23 (.Net Core), 2 (ABAP), 21 (Apex/Visualforce), 3 (ASP), 5 (CFML), 6 (COBOL), 22 (Go), 7 (JAVA/J2EE), 16 (JS/TS/HTML), 18 (MBS/C/C++/Scala), 9 (PHP), 10 (PYTHON), 17 (Ruby), 12 (Swift/Objective C/C++), 11 (VB6), 14 (VBScript)
-l	|Language level as an integer:<br><br>.NET: 2 (2.0), 3 (3.0), 4 (3.5), 5 (4.0), 11 (4.5), 15 (4.6), 16 (4.7), 30, (4.8), 32 (5.0)<br><br>.NET Core: 23 (1.0), 24 (1.1), 25 (2.0), 26 (2.1), 27 (2.2), 28 (3.0), 29 (3.1)<br><br>Java: 8 (1.5), 9 (1.6), 10 (1.7), 12 (1.8), 17 (1.9), 19 (10), 20 (11), 21 (12), 22 (13)<br><br>Python: 13 (2), 14 (2 Django), 18 (3)
-apf|	Whether to return exit(0) instead of exit(1) if the scan fails the security policy specified in Fortify on Demand


## Generate report based on scan results

After the scan is completed and your build passes, a report is automatically generated for your job. You can view the vulnerabilities under the **Gitlab Vulnerability Dashboard**.