## Lab Report 2: Servers and SSH Key.

## Part 1:
### Code for StringServer
```java
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {

    String message = "";
    int count = 1;
    String text = "";
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Strings: %s" + "\n", message);
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    text = parameters[1];
                    text = text.replaceAll("\\+", " ");
                    message += (Integer.toString(count) + ". " + text + "\n");
                    count++;
                    return message;
         
                }
            }
            return "404 Not Found!";
        }
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
Here I put in the url /add-message?s=hello
This stored stored the word "hello" in the variable message which was previously empty.
![Alt text](images/ex1.png "Example 1")

Here I append "How are you" to the variable message, again using /add-message?s=how are you. 
Previously, message just had "hello" stored but after executing the query it appended "how are you"
to the variable message
![Alt text](images/ex2.png "Example 2")

### 1. Which methods in your code are called?
  For each request the method being called is the handleRequest() method. Which handles queries
### 3. What are the relevant arguments to those methods, and the values of any relevant fields of the class?
  The most relevant argument to this method is the path /add-message and the query after the ? called "s" which tell us that user is inputing a message
### 4. How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
  The values that changed are the variables message, count, parameters, and text. Message stores all the text that has been inputed. 
  count, keeps track of the order. Parameters is changed per request. Finally, text is where we get rid of the + signs from the spaces in the query. In addition, the code detects
  the message by looking at the url after the ? sign. In addition, in the example I showed above (screenshots) everytime I add a query to add a message, the variable message changes
  and appends the input of the variable s in the query.
  
## Part 2:
### 1. The path to the private key for your SSH key for logging into ieng6 (on your computer or on the home directory of the lab computer)
The file that contain the private key is id_rsa in .ssh.

![Alt text](images/try2.png "Example 3")

### 2. The path to the public key for your SSH key for logging into ieng6 (within your account on ieng6)

![Alt text](images/keyinserver.png "Example 3")

### 3. A terminal interaction where you log into ieng6 with your course-specific account without being asked for a password.

![Alt text](images/login.png "Example 3")

## Part 3:
I learned very useful things this week. I learned about the scp comnmand and the mkdir command. scp command is used to transfer files securely
between servers. mkdir, is used to create a directory. In addition, I learned how to create a key that allows me to not have to put in my
password every time I login into the ieng6 server.
