# Part 1 
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    int numObjects = 1;
    String contents = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return contents;
        }
        else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    contents = contents + String.valueOf(numObjects) + ". " + parameters[1] + "\n";
                    numObjects++;
                    return contents;
                }
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
![Image](firstAdd.png)  
- The method handleRequest is called, with the url of the page being passed in as an URI argument. In this screenshot, the value for URI url being passed in to handleRequest is `http://localhost:4029/add-message?s=Hi`. Within the method, the value of `int` numObjects is 1 initially, and `String` contents is empty. The value of `String[]` parameters is set to the query of the url split at =, so this becomes `[s, Hi]`. After this specific request is run, `int` numObjects is incremented by 1, so it becomes equal to 2, and `String` contents is now equal to `"1. Hi\n"`. 


![Image](secondAdd.png)  
- The method handleRequest is called, with the url of the page being passed in as an URI argument. In this screenshot, the value for URI url being passed in to handleRequest is `http://localhost:4029/add-message?s=How%20are%20you`. Within the method initially, the value of `int` numObjects is 2, and `String` contents is equal to `"1. Hi\n"`. The value of `String[]` parameters is set to the query of the url split at =, so this becomes `[s, How are you]`. After this specific request is run, `int` numObjects is incremented by 1, so it becomes equal to 3, and `String` contents is now equal to `"1. Hi\n2. How are you\n"`. 

# Part 2
![Image](privatePath.png)  
- The path to the private key for your SSH key for logging into `ieng6` (on your computer or on the home directory of the lab computer)
  
Running `ls id_rsa` (with the home directory as my working directory) returned the path to the private key for my SSH key, which is `/Users/katyechen/.ssh/id_rsa`.

![Image](publicKey.png)  this screenshot needs to get fixed
- The path to the public key for your SSH key for logging into ieng6 (within your account on ieng6)
  
After logging into my account on `ieng6` and changing directory to the `.ssh` directory, running `ls authorized_keys` returned the path to the private key for my SSH key, which is `/.ssh/authorized_keys`. This was created during lab when we ran `scp` to copy the file from our personal computer to our account on `ieng6`, and saved the copy under the name `authorized-keys`.


![Image](login.png)  
- A terminal interaction where you log into ieng6 with your course-specific account without being asked for a password.
  
I was able to log into `ieng6` without being prompted to enter my password, as after I entered the `ssh cs15lfa23la@ieng6.ucsd.edu` command, it immediately began the login steps without any additional input.

  

# Part 3 
In week 2 of lab, I learned how to connect to a remote server from my computer, which I had never done before. This week (week 3) in lab, I also was able to connect to a remote server 

