# Lab Report 4

## Set Up

If a fork already exists of the lab7 repository, delete the original fork, then fork it again. 
Also, have a Google document with your forked GitHub lab7 repository link, and the JUnit compile and run commands in it. (If this is not allowed, then just have your GitHub lab7 repository tab ready and have Week 3 of the CS15L Course Website tab (has the JUnit commands) ready).

> Note: I will be doing this challenge task on a fresh run, so it assumes that none of the commands are in the history. However, it is possible to do this challenge faster by having some of the commands done once to get them saved in the history, and then using the `<up>` key to get to the commands. (I will type the alternate version for the steps with this method as well) The order in which I would put the commands in history are this (Command at the very bottom would be the most recent command): 
<br/>

> On the personal computer: <br/>
> * `ssh cs15lwi23ata@ieng6.ucsd.edu` the command for logging into the remote server <br/> <br/>
> 
> On the remote server: <br/>
> * `nano ListExamples.java` the command for opening the editor for ListExamples
> * `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` the command for running the JUnit tests
> * `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` the command for compiling the JUnit tests
> * `cd lab7` the command for entering the repository
> * `git clone git@github.com:ucsd-cse15l-w23/lab7.git` the command for cloning the lab 7 repository

<br/>

## Start the Timer!

**(1)** <br/>
Type "ssh`<space>`cs15lwi23ata@ieng6.ucsd.edu`<enter>`". 
- This logs me into the remote server

> Alternate: Type "`<up><enter>`".
> - The command was 1 up in the search history, so typing `<up>` once should access it 

<img width="960" alt="step1" src="https://user-images.githubusercontent.com/66851491/221411789-33e8df0b-e3a3-47f6-859d-2d8cfdc5135d.png">

<br/>

**(2)** <br/>
Copy your GitHub lab7 repository link by clicking to the Google Doc tab, highlighting the link, "`<ctrl + c>`", 
<br/>
**OR** clicking to your GitHub lab7 repository tab, clicking on the green "Code" button, clicking on "SSH", clicking on the copy button.
<br/>
Then, click back to VSC and type "git`<space>`clone`<space><ctrl + v><enter>`".
- This clones my forked lab7 repository, I copy and pasted the repository's SSH key

> Alternate: Type "`<up><enter>`".
> - The command was 1 up in the search history, so typing `<up>` once should access it 

<img width="960" alt="step2" src="https://user-images.githubusercontent.com/66851491/221411830-ef5e0b95-b2e6-4cee-9022-769f8fa16a9e.png">

<br/>

**(3)** <br/>
Type "cd`<space>`l`<tab><enter>`".
- This changes the directory to the GitHub repository lab7, I used `<tab>` to autofill "lab7/" from just "l"
> Note: That is a lower case "L", not an upper case "I".

Copy the JUnit compile command by clicking to the Google Doc tab, highlighting the compile command, "`<ctrl + c>`", 
<br/>
**OR** clicking to Week 3 of the CS15L Course Website tab, highlighting the compile command, "`<ctrl + c>`".
<br/>
Then, click back to VSC and type "`<ctrl + v><enter>`". 
- This compiles the JUnit tester, I copy and pasted the entire command

Copy the JUnit run command by clicking to the Google Doc tab, highlighting the run command, "`<ctrl + c>`", 
<br/>
**OR** clicking to Week 3 of the CS15L Course Website tab, highlighting the run command, "`<ctrl + c>`".
<br/>
Then, click back to VSC and type "`<ctrl + v><enter>`" (if copied from the Google Doc), 
<br/>
**OR** "`<ctrl + v><space>`L`<tab>`T`<tab><backspace><enter>`" (if copied from the Course Website).
- This runs the JUnit tester, I copy and pasted the entire command (if copied from the Google Goc), 
- **OR** copy and pasted the command without specifying the file name (if copied from the website), in which I then used `<tab>` to autofill "ListExamples" from typing "l", then used `<tab>` to autofill "ListExamplesTests." from typing "T", then used `<backspace>` on the period to delete it

> Alternate: Type "`<up><up><enter><up><up><up><enter><up><up><up><up><enter>`".
> - The command for changing the directory to the GitHub repository lab7 is 2 up in the search history, so typing `<up>` twice should access it 
> - The command for running the JUnit tester is 3 up in the search history, so typing `<up>` three times should access it 
> - The command for compiling the JUnit tester is 4 up in the search history, so typing `<up>` four times should access it 

<img width="960" alt="step3" src="https://user-images.githubusercontent.com/66851491/221411845-1c7b8a59-0e53-4855-8e50-47db5132d461.png">

<br/>

**(4)** <br/>
Type "nano`<space>`L`<tab>`.j`<tab><enter>`".
<br/>
- This opens up nano to edit the file "ListExamples.java", I used `<tab>` to autofill "ListExamples" from typing "L", then used `<tab>` to autofill "ListExamples.java" from typing ".j"

> Alternate: (Only for the line above, the lines below will be needed for both methods): Type "`<up><up><up><up><up><enter>`".
> - The command for opening nano is 5 up in the search history, so typing `<up>`  times five should access it 

Then, type "`<ctrl + />`43`<enter>`".
- This takes me to line 43 of the file in nano

<img width="960" alt="step4-part1" src="https://user-images.githubusercontent.com/66851491/221411861-6e234162-184f-4d97-b4a7-c41714e6a3be.png">

<br/>
Type "`<right>`" 12 times in a row (or hold down the right key until you reach the end of "index1" on line 43). <br/>
Type "`<backspace>`2".
- This fixes the mistake in the file

Type "`<ctrl + x>`y`<enter>`". 
- This saves the changes made in the file using `<ctrl + x>`, and "y" confirms that I want to save the changes made in the file 

<img width="960" alt="step4-part25" src="https://user-images.githubusercontent.com/66851491/221411887-3e5066dc-2fb3-43f1-b509-97f9887a3dbb.png">

<br/>

**(5)** <br/>
Type "`<up><up><up><enter>`".
<br/>
Type "`<up><up><up><enter>`".
- The command for compiling the JUnit tester is 3 up in the search history, so typing `<up>` three times should access it 
- The command for running the JUnit tester is 3 up in the search history, so typing `<up>` three times should access it 

> Alternate: The exact same as the lines above.

<img width="960" alt="step5" src="https://user-images.githubusercontent.com/66851491/221411932-70754638-3422-4378-824c-9885b55b04f5.png">

<br/>

**(6)** <br/>
Type "git`<space>`add`<space>`.`<enter>`".
- This adds the changed working directory "." to the staging area

Type "git`<space>`commit`<space>`-m`<space>`";"`<enter>`".
- This commits the changes in the staging area with the message ";" (the semi-colon is close to the quotation mark, so it makes the command faster and easier to type)

Type "git`<space>`push`<enter>`".
- This pushes the committed changes to the remote GitHub lab7 repository on my account

> Alternate: The exact same as the lines above.

<img width="960" alt="step6" src="https://user-images.githubusercontent.com/66851491/221411943-aeec470d-9456-4d4d-af1b-06491eef994f.png">

<br/>

## Done!
<img width="930" alt="step6-part2" src="https://user-images.githubusercontent.com/66851491/221411954-941ca798-f7af-4e84-b2b8-a77a853ba9fd.png">
- This screenshot shows the changes I made from the steps!
<br/>

## Before:
<img width="686" alt="lab7-before" src="https://user-images.githubusercontent.com/66851491/221411977-8f757437-58c4-44bf-829c-27b125385a3f.png">
- This is how the repository looked *before* the changes
<br/>

## After: 
<img width="689" alt="lab7-after" src="https://user-images.githubusercontent.com/66851491/221411984-7aeba523-f733-4377-b1a7-5325e070f50c.png">
- This is how the repository looked *after* the changes
<br/>

