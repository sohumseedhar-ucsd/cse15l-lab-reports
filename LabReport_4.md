## Log in to ```ieng6```:
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-05-22%20at%208.36.48%20PM.png?raw=true)
* I used ```ssh sseedhar@ieng6-202.ucsd.edu``` followed by the ```<enter>``` key to log in. 

## Git Clone Using ```SSH``` URL:
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-26%20at%206.09.14%20PM.png?raw=true)
* I used ```git clone git@github.com:sohumseedhar-ucsd/lab7.git``` followed by ```<enter>``` to clone the fork of my repository using the ```SSH``` URL on the Github Account. 

## Running Tests:
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-26%20at%206.08.27%20PM.png?raw=true)
* I used the ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` command followed by the ```<enter>``` key to compile the java files, and then used the ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests``` command followed by the ```<enter>``` key run my tests. 

## Using ```Vim``` to Edit File:
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-26%20at%206.31.16%20PM.png?raw=true)
* I used ```vim ListExamples.java``` followed by the ```<enter>``` key to edit the file.
  
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-26%20at%206.34.05%20PM.png?raw=true)
* The keys I pressed were the ```<down>``` key 43 times and the ```<right>``` key 12 times to get my cursor to the ```1``` of ```index1```.
  
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-26%20at%206.34.54%20PM.png?raw=true)
* I then used the ```<x>``` key to delete the ```1``` at that position. 

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-26%20at%206.35.29%20PM.png?raw=true)
* I then used the ```<i>``` key to enter insert mode so that I could insert my edit to the file. 

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-26%20at%206.36.06%20PM.png?raw=true)
* I then pressed the ```2``` key to make the change ```index1``` to ```index2``` in my file. 

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-26%20at%206.36.36%20PM.png?raw=true)
* I then pressed the following keys: ```<escape><:><w><q><enter>``` to save my changes and exit ```vim```. ```<escape>``` switches to command mode and then when followed by ```<:><w><q>```, it writes the changes we made to the file and then exits ```vim```. 

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-26%20at%206.37.33%20PM.png?raw=true)
* I then used the ```bash test.sh``` command followed by the ```<enter>``` key to re run my tests and confirm that the new output shows that the previously failing tests are now passing. 

## Committing and pushing changes:
![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-26%20at%206.48.55%20PM.png?raw=true)
* I first used the ```git init``` followed by ```<enter>``` to reinitialize my existing Git repository. I then ran the ```git add ListExamples.java``` command followed by ```<enter>``` to add my modified file to the staging. I then ran ```git commit -m "Fixed Merge"``` followed by ```<enter>``` to commit my changes to the file in the staging area, while also adding a brief message regarding my modification. I finally ran ```git push origin main``` followed by ```<enter>``` to push and commit my changes to the main branch of the remote repository. 


