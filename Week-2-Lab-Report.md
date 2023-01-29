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


## Part 2: Identifying and Fixing Bugs

---------------------------------------------------------


## Part 3: Conclusion

---------------------------------------------------------







1) Go to [this link](https://sdacs.ucsd.edu/~icc/index.php), and sign in with your school username and Student ID.

<br/>

2) Find your CSE15L account and account username.
> Ex: For Winter 2023, the account username would be cs15lwi23___, where at the end is a personalized random sequence of characters.

<br/>

> You should see a similar button as to the one in the image below with your account username. You can click on it to view more of your CSE15L account details.
> 
<img width="650" height="250" alt="cse15L-acc" src="https://user-images.githubusercontent.com/66851491/212466395-66094f19-d6ba-4c63-9b6d-ed500cc667ed.png">

<br/>

3) If you need to change your password, go to [this link](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit).

<br/>
<br/>
