# Lab Report 4

## Set Up

If a fork already exists of the lab7 repository, delete the original fork, then fork it again. 
Also, have a Google document with the GitHub lab7 repository clone link and the JUnit compile and run commands in it. (If this is not allowed, then just have a GitHub lab7 repository tab ready, and have Week 3 of the CS15L Course Website tab (has the JUnit commands) ready)

> Note: I will be doing this challenge task on a fresh run, so it assumes that none of the commands are in the history. However, it is possible to do this challenge faster by having some of the commands done once to get them saved in the history, and then using the `<up>` key to get to the commands. (I will type the alternate version for the steps with this method as well) The order in which I would put the commands in history are this (Command at the very bottom would be the most recent command): 
> On the personal computer:
> * `ssh cs15lwi23ata@ieng6.ucsd.edu` the command for logging into the remote server
> On the remote server:
> * `nano ListExamples.java` the command for opening the editor for ListExamples
> * `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` the command for running the JUnit tests
> * `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` the command for compiling the JUnit tests
> * `cd lab7` the command for entering the repository
> * `git clone git@github.com:ucsd-cse15l-w23/lab7.git` the command for cloning the lab 7 repository

<br/>

## Start the Timer!

1. 
Type "ssh`<space>`cs15lwi23ata@ieng6.ucsd.edu`<enter>`" 
> Alternate: Type `<up><enter>`.

<br/>

2. 
Copy the GitHub lab7 repository clone link by clicking to the Google Doc tab, highlighting the link, `<ctrl+c>`, OR clicking to the GitHub lab7 repository tab, clicking on the green "Code" button, clicking on "SSH", clicking on the copy button.
<br/>
Then, click back to VSC and type "git`<space>`clone`<space><ctrl+v><enter>`"
> Alternate: Type `<up><enter>`.

<br/>

3. 
Type "cd`<space>`l`<tab><enter>`"
Copy the JUnit compile command by clicking to the Google Doc tab, highlighting the compile command, `<ctrl+c>`, OR clicking to Week 3 of the CS15L Course Website tab, highlighting the compile command, `<ctrl+c>`.
<br/>
Then, click back to VSC and type `<ctrl+v><enter>`.
<br/>
Copy the JUnit run command by clicking to the Google Doc tab, highlighting the run command, `<ctrl+c>`, OR clicking to Week 3 of the CS15L Course Website tab, highlighting the run command, `<ctrl+c>`.
<br/>
Then, click back to VSC and type `<ctrl+v><space>`Lis`<tab>`Tests.
> Alternate: Type `<up><up><enter><up><up><up><enter><up><up><up><up><enter>`.

<br/>

4. 
Type "nano`<space>`Lis`<tab>`.`<tab><enter>`".
<br/>
> Alternate (Only for the line above, the lines below will be needed for both methods): Type `<up><up><up><up><up><enter>`".
<br/>

Then, type "`<ctrl+/>`43`<enter>`. 12
<br/>
Type "`<right>`" 12 times in a row (or hold down the right key until you reach the end of "index1" on line 43).
<br/>
Type "`<backspace>`2".
<br/>
Type "`<ctrl+x>`y`<enter>`". 

<br/>

5.
Type "`<up><up><up><enter>`
<br/>
Type "`<up><up><up><enter>`
> Alternate: The exact same as the lines above.

6. 
Type "git`<space>`add`<space>`.`<enter>`".
<br/>
Type "git`<space>`commit`<space>`-m`<space>`";"`<enter>`".
<br/>
Type "git`<space>`push`<enter>`".
> Alternate: The exact same as the lines above.



