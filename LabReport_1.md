## `cd` Command With No Arguments:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-04-02%20at%2012.16.04%20PM.png?raw=true)

* The working directory when `cd` was ran was `/home/lecture1`.
* This command resulted in no output because the `cd` command is used to change the working directory when there is a path to another directory given after the command. However, in this case no path (argument) was given, so there was no output. However, it is important to note that performing `cd` without no argument and from a directory that isn't `home` will simply take us back to `/home`. This change would be represented by `(base) sohum@Sohums-MacBook-Pro-280 lecture1` being changed to `(base) sohum@Sohums-MacBook-Pro-280 ~ %`. 
* As a result, the ouptut was not an error and NO output is what we expected we to see.

## `cd` Command With a Path to a Directory as an Argument:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-10%20at%2011.01.01%20PM.png?raw=true)

* The working directory when `cd lecture1/` was ran was `/home`.
* This command did not produce an output but the `cd lecture1/` command changed the working directory to `/home/lecture1`. While there is not output, the command line reflects this change by changing `[user@sahara ~]$` to `[user@sahara ~ /lecture1]$`. 
* This output was not an error and what we expected we to see.

## `cd` Command With a Path to a File as an Argument:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-10%20at%2011.11.02%20PM.png?raw=true)

* The working directory when `cd Hello.java` and `cd Hello.class` was ran was `/home/lecture1`.
* The output of our command produces an error in the bash script: `bash: cd: Hello.java: Not a directory`. This is because the cd command must be followed by a path to a directory or folder and cannot change directory to a specific text or code file. 
* This output was an error and what we expected we to see since `cd Hello.java` and `cd Hello.class` are not directories.

## `ls` Command With No Arguments:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-10%20at%2011.27.14%20PM.png?raw=true)

* The working directory when `ls` was ran was `/home`.
* This command resulted in the output `lecture1` because the `ls` command is used to output/list all the files within the current directory. 
* The output was not an error. The working directory was /home, so we expected to see only `lecture1` as our output. 

## `ls` Command With a Path to a Directory as an Argument:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-12%20at%201.38.35%20PM.png?raw=true)

* The working directory when `ls lecture1/` was ran was `/home`.
* This command resulted in the output `Hello.class`, `Hello.java`, `messages`, and `README`. Here, we applied the `ls` command with the argument `lecture1/` to indicate that we want the list of all the files within the `/lecture1` directory. 
* The output was not an error and was what we expected we to see.

## `ls` Command With a Path to a File as an Argument:
  
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-12%20at%201.44.29%20PM.png?raw=true)

* The working directory when `ls Hello.java`, `ls Hello.class`, and `ls README` was `/home/lecture1`.
* When the `ls` command was given with a path to a file as an argument, it simply resulted in the output of the name of the file given as an argument: `Hello.class`, `Hello.java`, `messages`, and `README`. 
* The output was not an error and was what we expected we to see. If the file is not in the current working directory, we can also provide the relative/absolute path of the file after `ls` to avoid performing multiple commands. 

## `cat` Command With No Arguments:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-13%20at%207.01.16%20PM.png?raw=true)

* The working directory when `cat` was ran was `/home`.
* This command resulted in no output because the `cat` command is used to print out the content of one or more files given by the paths as arguments. Here we used no arguments so the command did not have a path to print out the contents of any files.  
* The output did not display an error message, there was simply no output.

## `cat` Command With a Path to a Directory as an Argument:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-13%20at%207.05.31%20PM.png?raw=true)

* The working directory when `cat lecture1/` was ran was `/home`.
* This command resulted in the following error message: `cat: lecture1/: Is a directory`. Here, we applied the `cat` command with the argument `lecture1/`, but the `cat` command can only take paths to a file as an argument and does not work when a path to a directory is given as an argument.  
* The output was an error message because as mentioned, the `cat` command can only take paths to a file as an argument and does not work when a path to a directory is given as an argument.

## `cat` Command With a Path to a File as an Argument:
  
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-13%20at%207.19.20%20PM.png?raw=true)

* The working directory when `cat lecture1/Hello.java` was ran was `/home`.
* When the `cat` command was given a path to a file as an argument, it resulted in the output being the entirety of that file's content being porinted. The output I received when giving a path to the `Hello.java` file was
  
```
{
 `import java.io.IOException;
 
 import java.nio.charset.StandardCharsets;
 
 import java.nio.file.Files;
 
 import java.nio.file.Path;

 public class Hello {
   public static void main(String[] args) throws IOException {
     String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
     System.out.println(content);
   }
}
```

* The output was not an error and was what we expected we to see. The output was the entire file content of the `Hello.java` file.  







