# **Lab Report 2**
## Part 1

* Creating a web server will require Server.java and StringServer.java

* Here is the code for the file StringServer.java after the changes made:
![image](/cse15llab2f.png)

* As asked, the handleRequest() method stores the new string added using add-message concatenating the message onto a new line.

* Then I ran the file by writing this in the terminal:
![image](/cse15llab2g.png)

* The server shows the url to the server started. So I copied it into my browser and this is what it exhibited:
![image](/cse15llab2h.png)

* I had added this message if the string str is empty and has no message, "The string contains no message.".

* To add a message, we add /add-message at the end of the url and any message we want. For instance, I will try to add the messages "Hi" and "I love Cristiano Ronaldo".
![image](/cse15llab2i.png)

![image](/cse15llab2j.png)

* The method handleRequest() successfully finds the string "/add-message" in the url. Therefore, it detects where the string "=" appears and splits it, and then detecting the first element of the array, verifying whether it is "s".

* I used "%20" in order to write a message that was separated by spaces.


## Part 2

* I created a failure inducing output for the method reversed() in ArrayExamples.java

![image](/cse15llab2a.png)

* I created a non-failure inducing output for the method reversed() in ArrayExamples.java

![image](/cse15llab2b.png)

* Then I ran the two tests I created by compiling and running the file as shown:

![image](/cse15llab2c.png)

* Lastly, in order to correct the code in the method reversed() in the file ArrayExamples.java, I changed the order of the left hand side and right hand side of the equation in line 4 in the method. The first image shows the code before change and the second image shows the code after change.

![image](/cse15llab2d.png)

![image](/cse15llab2e.png)

## Part 3

In week 2, I learned about how to code an image in github, how to make repositories, and the basic syntax for coding headers or using font characterstics (bold, italics). Moreover, I recently learned about how to write a string that encompasses spaces, in the local server. I found "%20" extremely useful and innovative at the time.



