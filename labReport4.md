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
* Then run the command ``` bash test.sh ``` to run the files in the lab 7 directory. The code blaock below presents that 2 tests were run, 1 failed.
```
[cs15lsp23nj@ieng6-202]:~:118$ cd lab7
[cs15lsp23nj@ieng6-202]:lab7:119$ bash test.sh
JUnit version 4.13.2
..E
Time: 0.002
There was 1 failure:
1) testMerge2(ListExamplesTests)
org.junit.runners.model.TestTimedOutException: test timed out after 500 milliseconds
	at ListExamples.merge(ListExamples.java:44)
	at ListExamplesTests.testMerge2(ListExamplesTests.java:19(

FAILURES!!!
Tests run: 2,  Failures: 1

[cs15lsp23nj@ieng6-202]:lab7:120$ 
```

**Step 5: Rectification**

* To enter the file, type the command, ``` vim ListExamples.java ```.
* Then type ``` /index1 ``` and type ``` <Shift N> ```.
* Then press right arrow key five times.
* At ``` 1 ```, type ``` X ```, then type ``` I ```
* Then type ``` 2 ``` and press .
* Then exit the file using ``` :wq ```

![image](/cse15lLab4b.png)

**Step 6: Testing**

* Go back to the terminal and type ``` vim ListExamples.java ```, in order to enter the file.
* Then type ``` bash test.sh ``` , in order to compile and run the file.

```
[cs15lsp23nj@ieng6-202]:~:169$ cd lab7
[cs15lsp23nj@ieng6-202]:lab7:160$ bash test.sh
JUnit version 4.13.2
..
Time: 0.002

OK (2 tests)

[cs15lsp23nj@ieng6-202]:lab7:161$ 
```

* Here, we can observe that there are no errors anymore.

**Step 7: Commit & Push**

* In order to commit the changes, we first need to type ``` git add ```
* In order to commit ramifications, type ``` git commit -m "Committed" ``` and then push the ramifications with the command ``` git push ```, inside the repository.

```
[cs151sp23nj@ieng6-202:lab7:339$ git commit -m "Committed" 
[main 2432387] Committed
 Committer: Aryan Chowdhry <cs151sp23nj@ieng6-202.uesd. edu>
Your name and email address were configured automatically based 
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the 
following command and follow the instructions in your editor to edit 
your configuration file:
	
	git config --global --edit
	
After doing this, you may fix the identity used for this commit with:

	git commit --amend --reset-author

4 files changed, 1 insertion(+), 1 deletion (-) 
 create mode 100644 ListExamples.class 
 create mode 100644 ListExamplesTests.class 
 create mode 100644 StringChecker.class 
[cs151sp23nj@ieng6-202]:1ab7:340$ git push
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 1.90 KiB | 649.00 KiB/s, done.
Total 6 (delta 1), reused © (delta 0), pack-reused 0 
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:achowdhry/lab7.git
   603ed81.2432246 main -> main 
[cs151sp23nj@ieng6-202]:1ab7:341$

```

			** That is the end of Lab Report 4.**
