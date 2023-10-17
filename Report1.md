# Lab Report 1
## **cd**  

* No arguments:  
![Image](cdNoDir.png)  
The working directory was /home when the command was run. Since there was no argument given, the directory is changed to /home. Because the working directory was /home already when the command was run, there is no output and the terminal still displays [user@sahara ~], or /home, in the next line. Running `cd` with no arguments changes the directory to the root directory, which is /home. The lack of output is not an error since you wouldn't expect there to be any changes to the working directory.  

* Path to a directory:  
![Image](cdDir.png)  
The working directory was /home when this command was run. The output was that the working directory was changed to /lecture1, which was indicated by the display showing [user@sahara ~/lecture1] in the next line. Nothing else was printed since the directory was changed successfully to a folder within the working directory, /home. The output is not an error because the working directory was successfully changed to the input, which was /lecture1, so the `cd` command worked as intended.  


* Path to a file:  
![Image](cd file.png)  
The working directory was /lecture1 when the command was run. The output message reflects that the terminal tried to change the directory to the given argument, which was the path to a file, and that it was unsuccessful, since nothing should be printed when the directory is correctly changed. The directory cannot be set to a file, so passing in a path to a file caused a message to be output that tells you that the path led to a file, not a directory as expected. This output is an error because the directory cannot be set to a file, so the command could not be executed.  


## **ls**  


* No arguments:  
![Image](ls.png)  
The working directory was /lecture1 when the command was run. The output printed out the contents of the /lecture1 folder, since that was the working directory and no input was given. This output was not an error, since all the files in the working directory were printed successfully, and the command was executed as expected. 

   
* Path to a directory:  
![Image](lsDir.png)  
The working directory was /lecture1 when the command was run. The output printed out the contents of the input directory, which was the /messages folder. Since the working directory was /lecture1, the input path corresponded to /home/lecture1/messages, and the contents of the /messages directory could be printed successfully. This output is not an error, since every file in the /messages folder was correctly printed as expected when the `ls` command was run.
  
 
* Path to a file:  
![Image](lsFile.png) 
The working directory was /lecture1 when the command was run. The output printed out the relative path of the argument, so this looked the same as what was input. Since the en-us.txt file is within the /messages folder, and the /messages folder is within the working directory, /lecture1, the program was able to successfully output the name of the given file. The output is not an error, since the command returned what was expected.  


## **cat**  


* No arguments:  
![Image](cat.png)  
The working directory was /lecture1 when the command was run.  The output looked blank because the terminal was waiting for user input. After you typed something and pressed enter, it would print what you typed, and you had to exit using `Ctrl c`.  The output is not an error since entering `cat` with no arguments does not give the terminal a directory or file to refer to, and thus nothing can be output without further input from the user.  

   
* Path to a directory:  
![Image](catDir.png)   
The working directory was /lecture1 when the command was run. The output tells you that /messages is a directory, as /messages is a folder within the /lecture1 directory. This output is an error, since `cat` expects an argument to be a path to a file, but the argument was a path to a directory. `cat` is unable to print the contents of a directory, so `cat` outputs a message to tell the user that the argument was a directory, which `cat` cannot handle properly.   

   
* Path to a file:  
![Image](catFile.png) 
The working directory was /lecture1 when the command was run. The output is the contents of the en-us.txt file, which tells you that the `cat` command successfully found the en-us.txt file within the /messages folder, which was in the working directory. The output is not an error, since the program successfully used located the en-us.txt file and printed its contents, given the path that was input.  
