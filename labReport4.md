**Lab Report 4: Speeding Command Line Tasks**
**Step 1: Timer**
* Start a timer.
**Step 2: Logging in**
* On the terminal, type your course specific account name command. My couse specific name character's are 'nj': ``` ssh cs15lsp23nj@ieng6.ucsd.edu ```

* The output from the command should be as follows:

```
Last login: Mon Jun  5 23:03:01 on ttys004
Aryan@MacBook-Air-2 ~ % ssh cs15lsp23nj@ieng6.ucsd.edu
(cs15lsp23nj@ieng6.ucsd.edu) Password: 
Last login: Thu May 11 18:11:34 2023 from 69.196.43.180
Hello cs15lsp23nj, you are currently logged into ieng6-203.ucsd.edu

You are using 0% CPU on this system

Cluster Status 
Hostname     Time    #Users  Load  Averages  
ieng6-201   01:55:01   4  1.65,  0.79,  0.40
ieng6-202   01:55:01   3  1.69,  1.17,  0.73
ieng6-203   01:55:01   7  0.20,  0.35,  1.57

 
Tue Jun 06, 2023  1:59am - Prepping cs15lsp23
```
**Step 3: Cloning**
* Create a fork of the repository, 'lab7' from github. Then press the button 'Code', which is in a green box, and copy the https link.

![image](/cse15lLab4a.png)

* Run the command ``` git clone ```, and paste the copied https link into the terminal as shown below:
```
[cs15lsp23nj@ieng6-202]:~:117$ git clone https://github.com/achowdhry/lab7.git
Cloning into 'lab7'...
remote: Enumerating objects: 38, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 38 (delta 0), reused 1 (delta 0), pack-reused 35
Receiving objects: 100% (38/38), 372.59 KiB | 1.42 MiB/s, done.
Resolving deltas: 100% (12/12), done.
[cs15lsp23nj@ieng6-202]:~:118$ 
```
**Step 4: Testing**
* To start with testing, run the command ``` cd lab7 ``` to get into the lab7 directory.
```
[cs15lsp23nj@ieng6-202]:~:118$ cd lab7
[cs15lsp23nj@ieng6-202]:lab7:119$          
```
* Then run the command ``` bash test.sh ``` to run the files in the lab 7 directory.
```
[cs15lsp23nj@ieng6-202]:~:118$ cd lab7
[cs15lsp23nj@ieng6-202]:lab7:119$ bash test.sh
JUnit version 4.13.2
.E
Time: 0.002
There was 1 failure:
1) initializationError(org.junit.runner.JUnitCommandLineParseResult)
java.lang.IllegalArgumentException: Could not find class [TestListExamples]
	at org.junit.runner.JUnitCommandLineParseResult.parseParameters(JUnitCommandLineParseResult.java:100)
	at org.junit.runner.JUnitCommandLineParseResult.parseArgs(JUnitCommandLineParseResult.java:50)
	at org.junit.runner.JUnitCommandLineParseResult.parse(JUnitCommandLineParseResult.java:44)
	at org.junit.runner.JUnitCore.runMain(JUnitCore.java:72)
	at org.junit.runner.JUnitCore.main(JUnitCore.java:36)
Caused by: java.lang.ClassNotFoundException: TestListExamples
	at java.base/jdk.internal.loader.BuiltinClassLoader.loadClass(BuiltinClassLoader.java:641)
	at java.base/jdk.internal.loader.ClassLoaders$AppClassLoader.loadClass(ClassLoaders.java:188)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:521)
	at java.base/java.lang.Class.forName0(Native Method)
	at java.base/java.lang.Class.forName(Class.java:495)
	at java.base/java.lang.Class.forName(Class.java:474)
	at org.junit.internal.Classes.getClass(Classes.java:42)
	at org.junit.internal.Classes.getClass(Classes.java:27)
	at org.junit.runner.JUnitCommandLineParseResult.parseParameters(JUnitCommandLineParseResult.java:98)
	... 4 more

FAILURES!!!
Tests run: 1,  Failures: 1

[cs15lsp23nj@ieng6-202]:lab7:120$ 
```
* As we can see one test is run and failed. 

