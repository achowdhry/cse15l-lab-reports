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
```
* After compiling the following message will appear. Left click the link in the message below in order to open the server created, in your browser.
```
Server Started! Visit http://localhost:4007 to visit.
```

* The server shows the url to the server started. So I copied it into my browser and this is what it exhibited:
![image](/cse15llab2h.png)

* The message, "The string contains no message." is displayed because handleRequest method is called upon, which checks the if statement in order to check whether the string str is empty. Therefore, this message is displayed as the string str contained no message.

* To add a message, we add /add-message at the end of the url and any message we want. For instance, I will try to add the message "Hi" by concatenating the url, "localhost:4000/" with "/add-message?s=Hi".
![image](/cse15llab2i.png)


* Then concatenating the url, "localhost:4000/" with "/add-message?s=I%20love%20Cristiano%20Ronaldo". Here the command "%20" adds a space " " between the words. This url gives the output:
![image](/cse15llab2j.png)

* While adding the above message, "Hi", the above url typed calls handleRequest method, wherein url is the parameter. It runs through the if statement, checking whether the url parameter input contains "/add-message". After checking, it determines that if the condition is true, the method makes a string array parameter created by splitting the string with "=", regex. Then the iterator checks the first element of the array, whether it is "s" or not. If the condition is deemed true then the iterator concatenates the string to the variable str, then the method concludes by returning the string, displaying it on the server.


* Then when we add the second phrase "I love Cristiano Ronaldo", it displays it in a different line as compared to the message "Hi" because when the second message was added to str, it created a new line as well.

* If any condition is deemed false while the iterator runs through the loop then the  message "404 Not Found" is displayed.

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

```
Aryan@Vandans-MacBook-Pro lab3-main % javac -cp .:lib/hamcrest-core1.3.jar:lib/junit 4.13.2.jar *.java
Aryan@Vandans-MacBook-Pro lab3-main % java -cp .:lib/hamcrest-core-1.3.jar:lib/junit 4.13.2.jar org.junit.runner.JUnitCore ArrayTests JUnit version 4.13.2
..E
Time: 0.013
There was 1 failure:
1) testReversed3 (ArrayTests)
arrays first differed at element [0]; expected: <5> but was:<0>
    at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
    at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28) 
    at org.junit.Assert.internalArrayEquals(Assert.java:534)
    at org.junit.Assert.assertArrayEquals(Assert.java:418) 
    at org.junit.Assert.assertArrayEquals(Assert.java:429) 
    at ArrayTests.testReversed3 (ArrayTests.java:16)
    ... 32 trimmed
Caused by: java.lang.AssertionError: expected: <5> but was: <0>
    at org.junit.Assert.fail(Assert.java:89)
    at org.junit.Assert. failNotEquals(Assert.java:835)
    at org.junit.Assert.assertEquals(Assert.java:120)
    at org.junit.Assert.assertEquals(Assert.java:146)
    at org.junit.internal.ExactComparisonCriteria.assertElementsEqual(ExactComparisonCriteria.java:8)
    at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:76)
    ... 38 more
FAILURES!!!
Tests run: 2, Failures: 1
```

* Lastly, in order to correct the code in the method reversed() in the file ArrayExamples.java, I changed the order of the left hand side and right hand side of the equation in line 4 in the method. 
This first image shows the code before correction:
```
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

This second image shows the code after correction made, changing the order of the body of the for loop statement and the output of the return statement:

```
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[arr.length - i - 1] = arr[i];
    }
    return newArray;
  }
```

## Part 3

In week 2, I learned about how to code an image in github, how to make repositories, and the basic syntax for coding headers or using font characterstics (bold, italics). Moreover, I recently learned about how to write a string that encompasses spaces, in the local server. I found "%20" extremely useful and innovative at the time.



