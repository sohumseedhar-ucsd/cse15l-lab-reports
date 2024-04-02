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
