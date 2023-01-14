# CSE15L Login Tutorial

## Part 0: Accessing Your CSE15L Course-Specific Account

---------------------------------------------------------

1. Go to [this link](https://sdacs.ucsd.edu/~icc/index.php).

<br/>

2. Sign in with your school username and Student ID.

<br/>

3. Find your cse15L account and account username.
> Ex: For Winter 2023, the account username would be cs15lwi23___, where at the end is a personalized random sequence of characters

> You should see something similar to the screen below
> 
<img width="371" alt="cse15L-acc" src="https://user-images.githubusercontent.com/66851491/212466395-66094f19-d6ba-4c63-9b6d-ed500cc667ed.png">


<br/>

4. If you need to change your password, go to [this link](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit).

<br/>
<br/>

## Part 1: Installing VScode (Visual Studio Code)
Note: Skip this if you already have VScode installed

---------------------------------------------------------

1. Download and install [Visual Studio Code](https://code.visualstudio.com/Download) onto your computer.
> Make sure to select the correct version depending on your operating system (Windows, Linux, Mac)

<br/>

2. Open up VScode.
> You should see something similar to the screen below
> 
<img width="960" alt="vscode-start" src="https://user-images.githubusercontent.com/66851491/212463055-7fe0c44d-14a0-45c4-a0a3-b67911e6703c.png">

<br/>
<br/>

## Part 2: Remotely Connecting

---------------------------------------------------------

1. If you are on Windows, download and install [Git](https://gitforwindows.org/) onto your computer.

<br/>

2. Open the terminal in VScode (Under *Terminal* in the upper bar), then open the command palette (Under *View* in the upper bar). Search "Select
default profile" in the command palette, and then select Git Bash.
> You should see something similar to the screen below
> 
<img width="960" alt="vscode-gitbash" src="https://user-images.githubusercontent.com/66851491/212463058-46d82a24-aff6-4e58-9581-043bf9b0b942.png">


<br/>

3. Go the terminal and click on the plus sign in the upper right corner. This should open a drop down menu. Select Git Bash, and a new Git Bash terminal will
be created.

<br/>

4. Type the following template into the Git Bash terminal: `$ ssh ____________@ieng6.ucsd.edu` where the blank spaces should be filled with
your cse15L account username. 
> Ex: `$ ssh cs15lwi23zzz@ieng6.ucsd.edu`

> Note: You should see the that the terminal already has `$`, and you don't type it in yourself. 

<br/>

5. Because this is (likely) the first time you are connecting to this server, the terminal will then output a message about authenticity and ask you: `Are you sure you want to continue connecting (yes/no/[fingerprint])?`. Type in `yes`. 

<br/>

6. You will then have to enter your password to your cse15L account next to where it says `Password:`.
> Note: If you just changed the password, it may take a while (maybe even up to an hour) for the password change to take effect.

> Another Note: When you type in your password, nothing will show up on the screen, but the characters are still being registered (hidden due to privacy).

<br/>

7. You are now connected to the remote server, and should see a message like `Hello _________, you are currently logged into ieng6-203.ucsd.edu`, where the blank space is your cse15L account username. There should also be some other status and user information displayed.

<br/>
<br/>

## Part 3: Trying Some Commands 

---------------------------------------------------------


