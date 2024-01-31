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

## Screenshot 2 of using `/add-message`:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-30%20at%203.41.59%20PM.png?raw=true)

* Which methods in your code are called?
* What are the relevant arguments to those methods, and the values of any relevant fields of the class?
* How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.






