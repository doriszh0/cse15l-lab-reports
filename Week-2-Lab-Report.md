# Week 2 Lab Report

## Part 1: Writing a Web Server

---------------------------------------------------------

The code in StringServer.java
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String currentString = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return "String Builder Website\n" + String.format("Hello, %s", 
                    System.getProperty("user.name"));
        } 
        else if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                if (currentString.equals("")) {
                    currentString += parameters[1];
                }
                else {
                    currentString += "\n" + parameters[1];
                }
                return currentString;
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
The screenshots of using /add-message

![image](images/add-message-test.png)

Screenshot 1:
The method main method is executed when StringServer.java is run on my computer. The main method has the parameter `args`, which takes the arguments in the command prompt. This will be important because the first argument `args[0]` is used to determine the port number for the server. 

In the main method is the method call `Server.start(port, new Handler());`. The start method call is what starts the server, and it takes in two arguments. The first argument is the port number, which, as mentioned before, is taken from the command prompt argument. In this case, I entered 7011 as the server number. The second argument is a new Handler object in order to handle requests in the URL. 

The Handler class has a single method called handleRequest with a URI object `url` as a parameter, and it returns a string to be displayed on the website. The URL passed into the method will be the URL of the website server. The string displayed is determined by what is in the path and query in the URL. 

In order to add a message, the path must include `/add-message` after the domain, followed by the query in the format of `?s=`. The argument that follows the equal sign (the delimiter) is the string that is added to the existing string, and then it is all displayed on the website. In this screenshot, I entered `Hello` as the query argument, and you can see that it is now on the website.

The Handler has a String instance variable `currentString`, which is initially just an empty string. However, every time a message is added through the query in the URL, the variable is updated so that the message string is concatenated to `currentString` on a new line (except for the first time). In this screenshot, because this is the first time a message is added, the string is concatenated without a new line. 

![image](images/add-message-test2.png)



## Part 2: Identifying and Fixing Bugs

---------------------------------------------------------



## Part 3: Conclusion

---------------------------------------------------------


