## CD Command With No Arguments:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-10%20at%2010.02.10%20PM.png?raw=true)

* The working directory when `cd` was ran was `/home`.
* This command resulted in no output because the `cd` command is used to change the working directory when there is a path to another directory given after the command. However, in this case no path (argument) was given, so there was no output.
* As a result, NO output is what we expected we to see.   

## CD Command With a Path to a Directory as an Argument:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-10%20at%2011.01.01%20PM.png?raw=true)

* The working directory when `cd lecture1/` was ran was `/home`.
* This command did not produce an output but the `cd lecture1/` command changed the working directory to `/home/lecture1`. While there is not output, the command line reflects this change by changing `[user@sahara ~]$` to `[user@sahara ~ /lecture1]$`. 
* This output was not an error and what we expected we to see.

## CD Command With a Path to a File as an Argument:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-01-10%20at%2011.11.02%20PM.png?raw=true)

* The working directory when `cd Hello.java` and `cd Hello.class` was ran was `/home/lecture1`.
* The output of our command produces an error in the bash script: `bash: cd: Hello.java: Not a directory`. This is because the cd command must be followed by a path to a directory or folder and cannot change directory to a specific text or code file. 
* This output was an error and what we expected we to see since `cd Hello.java` and `cd Hello.class` are not directories. 




