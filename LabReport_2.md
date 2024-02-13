## `ChatServer` code:

```
import java.io.IOException;
import java.net.URI;

class ChatHandler implements URLHandler {
    private String chatInput = "";

    public String handleRequest(URI url) {
        if(url.getPath().equals("/add-message")){
            String[] parameters = url.getQuery().split("&");
            String message = parameters[0].split("=")[1];
            String user = parameters[1].split("=")[1];

            chatInput += user + ": " + message + "\n";
        }

        return chatInput;
    }

}

public class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new ChatHandler());
    }
}

```

## Screenshot 1 of using `/add-message`:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-30%20at%203.39.42%20PM.png?raw=true)

* Which methods in your code are called?
  The `handleRequest` method in the `ChatHandler` class is called to handle the incoming request.
  Example:
  ```
  ChatHandler.handleRequest(URI url);
  ```
* What are the relevant arguments to those methods, and the values of any relevant fields of the class?
  The arguments (url) for this method in this screenshot `/add-message?s=Hello&user=jpolitz` and `/add-message?s=How Are You Doing!&user=Sohum`. The relevant field of this class is the `chatInput` field, which originally has a value of an empty string:
  ```
  private String chatInput = "";
  ```
* How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
  The value of the `chatInput` field changes from an empty string ```""``` to ```"jpolitz: Hello\n"``` as the method finds the user and the    message from the url argument and append it to the String `chatInput`. The value of the `chatInput` field then changes again from string ```"jpolitz: Hello\n"``` to ```"jpolitz: Hello\nSohum: How Are You Doing!\n"``` as the method finds the user and the message from the next url argument and appends it to the String `chatInput`. 

## Screenshot 2 of using `/add-message`:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-30%20at%203.41.59%20PM.png?raw=true)

* Which methods in your code are called?
  The `handleRequest` method in the `ChatHandler` class is called to handle the incoming request.
  Example:
  ```
  ChatHandler.handleRequest(URI url);
  ```
* What are the relevant arguments to those methods, and the values of any relevant fields of the class?
  The arguments (url) for this method in this screenshot `/add-message?s=Im Good thanks!&user=OtherPerson` and `/add-message?s=How Are You     Doing!&user=Sohum`. The relevant field of this class is the `chatInput` field, which from the previous call to the `/add-message` had a      value 
  ```
  private String chatInput = "jpolitz: Hello\nSohum: How Are You Doing!\n";
  ```
* How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
  The value of the `chatInput` field changes from an empty string ```jpolitz: Hello\nSohum: How Are You Doing!\n``` to ```"jpolitz: Hello\nSohum: How Are You Doing!\nOtherPerson: Im good thanks"``` as the method finds the user and the message from the url argument and append it to the String `chatInput`.

## Absolute Path to Private Key:
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-13%20at%203.36.28%20PM.png?raw=true)

## Absolute Path to Public Key:
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-30%20at%209.37.54%20PM.png?raw=true)

## Screenshot of logging into `ieng6` without password authentification:
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-30%20at%205.03.42%20PM.png?raw=true)

## Something I learned: 
* During week 3 lab, something I learned that I thought was super cool was how to build and run a web server using localhost using a port. I am still curious on more advanced techniques that can be employed to build more useful tools.  




