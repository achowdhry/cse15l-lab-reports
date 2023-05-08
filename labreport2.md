# **Lab Report 2**
## Part 1

* Creating a web server will require Server.java and StringServer.java

* Here is the code for the file StringServer.java after the changes made:

```
import java.io.IOException;
import java.net.URI;
class Handler implements URLHandler {

    String str = "";
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            if (str.isEmpty()){
                return "The string contains no message.";
            }
            else{
                return str;
            }
        }
        else if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                str +=parameters[1] +"\n";
                return str;
            }
        } 
        return "404 Not Found!";
        
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

* As asked, the handleRequest() method stores the new string added using add-message concatenating the message onto a new line.

* Then I ran the file by writing this in the terminal:

```
Aryan@Vandans-MacBook-Pro wavelet-master % javac Server.java StringServer.java
Aryan@Vandans-MacBook-Pro wavelet-master % java StringServer 4007
Server Started! Visit http://localhost:4007 to visit.
```

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

```
  @Test
  public void testReversed3() {
    int[] wrongTest = {2, 4, 5};
    assertArrayEquals(new int[]{5, 4, 2}, ArrayExamples.reversed(wrongTest));
  }
```

* I created a non-failure inducing output for the method reversed() in ArrayExamples.java

```
  @Test
  public void testReversed2() {
    int[] rightTest = {0, 0, 0};
    
    assertArrayEquals(new int[]{0, 0, 0}, ArrayExamples.reversed(rightTest));
    
  }
```

* Then I ran the two tests I created by compiling and running the file as shown:

![image](/cse15llab2c.png)

* Lastly, in order to correct the code in the method reversed() in the file ArrayExamples.java, I changed the order of the left hand side and right hand side of the equation in line 4 in the method. The first image shows the code before change and the second image shows the code after change.

![image](/cse15llab2d.png)

![image](/cse15llab2e.png)

## Part 3

In week 2, I learned about how to code an image in github, how to make repositories, and the basic syntax for coding headers or using font characterstics (bold, italics). Moreover, I recently learned about how to write a string that encompasses spaces, in the local server. I found "%20" extremely useful and innovative at the time.



