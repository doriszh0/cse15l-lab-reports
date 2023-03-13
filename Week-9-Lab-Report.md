# Lab Report 5

## Week 6: Grading Script

<img width="326" alt="gradescript" src="images/gradescript.png">

> This is the grading script my partner and I wrote during Week 6!

## How the Grading Script Works

```
CPATH='.;../lib/hamcrest-core-1.3.jar;../lib/junit-4.13.2.jar'
```
> This line just stores the JUnit path in a variable so that the code is cleaner to look at

<br/>

```
rm -rf student-submission
mkdir student-submission
git clone $1 student-submission
echo 'Finished cloning'
```
> We probably need to run the grading script multiple times, but we only want one student submission at a time, which is why, if it exists, we delete the previous `student-submission` directory first, then create a new `student-submission` directory right after. 
> We then want to get the actual student submission from GitHub by using `git clone` along with the file name specified in the terminal when running the grading script (stored in the variable `$1`). To show that the process was completed, we print `Finished cloning` in the terminal. 

<br/>

```
cp TestListExamples.java student-submission
cd student-submission
if [[ -f ListExamples.java ]]
then 
    echo "ListExamples.java found"
else 
    echo "need file ListExamples.java"
    exit 1
fi
```
> Using the `cp` command on `TestListExamples.java`, we first copy the file that is used to test the student submission into `student-submission`, the same directory as the student submission, to make access simpler. Then, we change the directory to `student-submission` using `cd`.
> Now we need to check whether or not the student submission contains the file we need, and to do this, we use an if statement. We ask if, specifically the file (`-f`), `ListExamples.java` exists in the directory, and if it does, we print `ListExamples.java found` in the terminal. If it does not exist, then we print `need file ListExamples.java`, and then we terminate the script with exit code 1 due to the missing file. 

<br/>

```
javac -cp $CPATH *.java 
if [[ $? -eq 0 ]];
then 
    echo "ListExamples.java successfully compiled"
else 
    echo "ListExamples.java did not compile correctly"
    exit 1
fi
```
> Now, with the first line, we run the command of compiling the JUnit tester, which checks for errors in both the JUnit tester and the files that the JUnit is testing (this is why we do not need to compile `ListExamples.java` before we compile the JUnit tester). If there are any compile issues, they would also be printed in the terminal. 
> If the command is successful, it will return an exit code of 0, but if it fails it will return an exit code of 1. Therefore, we can check if we successfully compiled the file or not by checking the returned exit code. The exit code of the most recent command that was run is always stored in the variable `$?`, so we check if the exit code is equal to (`-eq`) 0. If the exit code is equal to 0 that means the compile was successful and there was no error, and we print `ListExamples.java successfully compiled` in the terminal. If the exit code is not equal to 0, that means the compile was not successful, and we print `ListExamples.java did not compile correctly` in the terminal. Then, we terminate the script with exit code 1 due to the unsuccessful compile. 

<br/>

```
java -cp $CPATH org.junit.runner.JUnitCore TestListExamples > score.txt
```
> Now we actually run the JUnit tester `TestListExamples` and save the output in a text file called `score.txt`.

<br/>

```
grep -C 0 "Tests run:" score.txt > grep-score.txt
if [[ -s grep-score.txt ]]
then
    grep -o "[0-9]*" grep-score.txt > numbers.txt
    TESTS=`head -n 1 numbers.txt`
    FAILS=`tail -n 1 numbers.txt`
    DIFFERENCE=`expr $TESTS - $FAILS`
    GRADE=`expr $DIFFERENCE / $TESTS \* 100`
    echo "You failed $FAILS out of $TESTS tests"
    echo "Your grade is $GRADE%"
else 
    grep -C 0 "OK" score.txt > grep-score.txt
    grep -o "[0-9]*" grep-score.txt > numbers.txt
    TESTS=`head -n 1 numbers.txt`
    echo "You failed 0 tests out of $TESTS tests"
    echo "Your grade is 100%!"
fi
```
> First, we need to get the line that shows how many tests have failed. If there was a failed test, then the output would have the line `Tests run: __,  Failures: __`, where there would be numbers in place of the `__`. Therefore, we use grep to search for the `Tests run:` line and then save the output in a text file called `grep-score.txt`. The part `-C 0` means context 0, in which context refers to the lines before and after the matching line. Context 0 ensures that we get only the line that has the matching text. 
> Next, we check use `-s` to check whether or not `grep-score.txt` is empty,  which determines whether or not the student passed all their tests or not. 

