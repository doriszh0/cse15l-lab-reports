# Lab Report 3

## Investigating the command `find`
> Note: For all commands, I am starting in the `skill-demo1-server` directory, and the `skill-demo1-data` directory is inside of the `skill-demo1-server` directory, and then the `written_2` directory is inside of the `skill-demo1-data` directory.

<br/> <br/>

## Part 1: Using `find` with `-name` and `-type`

---------------------------------------------------------

You can use both `-name` and `-type` to narrow down the data item that you are looking for!

<br/>

Example 1:

```
$ find skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ -name "*.txt" -type f
skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch1.txt
skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch14.txt
skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch15.txt
skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch2.txt
skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch3.txt
skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch6.txt
skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch7.txt
skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch8.txt
skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch9.txt
```
In the code block above, I am finding anything that has `.txt` at the end of the name AND is also a file. The `f` refers to type file, but there are other options as well, the other more-likely-to-be-used choice being `d` for type directory. Also, to be clear, if there is only a space separating two tests (tests refer to specifications for `find` such as `-name` and `-type`), then it is assumed that there is an operator `-and` in between the two tests, meaning both tests have to be fulfilled. Overall, because you can use patterns to specify certain data items (in this case I am only looking for `.txt` files), as well specify exactly what data type you want (usually either a file or directory), I can easily look through directories to find what I want. 

> Although it may seem redundant to specify the data item to be type file when I am already looking for names that end in `.txt`, which is a file format, you never know if someone ever decides to name a folder  `{insert-name-here}.txt` for some weird reason.

<br/>

Example 2: 

```
$ find skill-demo1-data/written_2/travel_guides/ -name "History*" -or -name "*History*" -type f
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryDublin.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryEdinburgh.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryEgypt.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryFrance.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryFWI.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryGreek.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryHawaii.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryHongKong.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryIbiza.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryIndia.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryIsrael.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryIstanbul.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryItaly.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryJamaica.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryJapan.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryJerusalem.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryLasVegas.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryMadeira.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryMadrid.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryMalaysia.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HistoryMallorca.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Algarve-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Amsterdam-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Athens-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Bali-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Barcelona-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Beijing-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Berlin-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Budapest-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/California-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Canada-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/CanaryIslands-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Cancun-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/China-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Costa-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/CostaBlanca-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Crete-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Cuba-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Nepal-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/NewOrleans-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Poland-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Portugal-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Vallarta-History.txt
```
In the code block above, I am finding anything that has a name in the format of `History{insert-name-here}` OR `{insert-name-here}History` AND is also a file. In this case, I used the operator `-or` in between the two name tests, so that I would get data items in either format. After a data item fulfills one of the name specifications, it is then checked whether or not it is a file (the precedence of the evaluation of the operations is just left to right). Overall, because you can use patterns to specify certain data items (in this case I am looking for a specific formatting for the name), as well specify exactly what data type you want (usually either a file or directory), I can easily look through directories to find what I want. 

<br/> <br/>

## Part 2: Using `find` with access/change times such as `-atime` and `-ctime`

---------------------------------------------------------

You can use `-atime` and `-ctime` to narrow down the data item that you are looking for!

<br/>

Example 1:

```
$ find skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ -atime -1
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch1.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch10.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch3.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch4.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch5.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch6.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch7.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch8.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch9.txt

$ find skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ -atime +1

```
In the first code block above, I am looking for files in the `Kauffman` directory that I have accessed less than 1 day ago. I currently have my VSCode open for all these files, so it makes sense that all the files in `Kauffman` would appear, as I am accessing them right now. In the second code block above, I am looking for files in the `Kauffman` directory that I have accessed more than 1 day ago (see note below for clarification on actual time). Again, because I am currently accessing the files in VSCode, it makes sense that no files would appear, which is exactly what happened. Also, to explain exactly how the format of `-atime` works, it uses `n` * 24 hours to determine the numerical value for the time, as well as the `+`, or `-`, or lack of any sign to determine the time to be more than, or less than, or equal to, respectively, with the time value specified. Overall, with `-atime` you can easily find files you have recently accessed, or perhaps even remove files you have not accessed in a long itme and don't need anymore.

> An important note about how the time-based tests work is that fractions/decimals are rounded down to a whole number, which means, for example, if you put `-atime +1`, it means that you actually need to have accessed the file at least **2** days ago (even 1.999 days would round down to 1 day). 

<br/>

Example 2:

```
$ find skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ -ctime +1
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch1.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch10.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch3.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch4.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch5.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch6.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch7.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch8.txt
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch9.txt

$ find skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ -ctime -1

```
In the first code block above, I am looking for files in the `Kauffman` directory that I have changed more than 1 day ago (see note above for clarification on actual time). I have never changed the files before, except for when I cloned the files from GitHub, which was definitely more than 2 days ago, so it makes sense that all the files in `Kauffman` would appear. In the second code block above, I am looking for files in the `Kauffman `directory that I have changed less than 1 day ago. Again, because I have never changed the files in VSCode, it makes sense that no files would appear, which is exactly what happened. Also, `-ctime` works basically the exact same way as `-atime`, except it checks for the change/modify time instead of the access time. Overall, with `-ctime`, similar to `-atime`, you can easily find files you have recently changed, or remove files you have not changed in a long itme and don't need anymore.


<br/>

> Some Extra Information: There is also `amin` and `cmin`, which are based on minutes, rather than days. So typing `-amin +30` will give files last accessed more than 30 minutes ago. 


<br/> <br/>

## Part 3: Using `find` with `-delete`

---------------------------------------------------------

You can use `-delete` to delete the data item that you are looking for!

<br/>

Example 1:

```
$ cd skill-demo1-data/written_2/non-fiction/OUP/

$ mkdir RybczynskiCopy

$ cp Rybczynski/ch1.txt RybczynskiCopy

$ find RybczynskiCopy -name "*.txt"
RybczynskiCopy/ch1.txt

$ find RybczynskiCopy -name "*.txt" -delete

$ find RybczynskiCopy -name "*.txt"
```
> I didn't want to actually delete any of the actual files in `written_2`, so I created a new directory called `RybczynskiCopy`, and copied the file `ch1.txt` that was in the original `Rybczynski` directory to `RybczynskiCopy`. 

In the code block above, after making a copy to delete safely, and using `find` with `-name` to check that the copy worked (`ch1.txt` is outputted as expected), I then used `find` with `-name` to specify I wanted to delete all the `.txt` files in the directory with `-delete`, which in this case, would just be `ch1.txt`. I then use `find` with `-name` again to check that the deletion worked, and because there is no output, that means `ch1.txt` was successfully deleted. Overall, `-delete` just makes it easy to delete the files that you are looking for.  

<br/>

Example 2:

```
$ find RybczynskiCopy
RybczynskiCopy

$ find RybczynskiCopy -delete

$ find RybczynskiCopy
find: ‘RybczynskiCopy’: No such file or directory
```

In the code block above, after executing `-delete` in Example 1, I am left with just the empty directory `RybczynskiCopy`. I first prove that the directory still exists with just `find`, and then I delete it using `find` with `-delete`. After deleting it, I use `find` again to check that the deletion worked, and the output of `No such file or directory` means that `RybczynskiCopy` was successfully deleted. Overall, you can also use `-delete` to delete specified directories and all of the files inside of it all at once too.  

<br/> <br/>

## Part 4: Using `find` with `exec`

---------------------------------------------------------

You can use `-exec` to execute command line arguments on the data item that you are looking for!

<br/>

Example 1:

```
$ find skill-demo1-data/written_2/ -type f -exec grep -l "Lucayans" {} \;
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt
```
In the code block above, I first look for all the files in `written_2`, and then I use `exec` to pass each file as a command line argument for the command `grep`. With `grep -l`, I list the file name(s) that have the word "Lucayans" in it. How `-exec` works is that you write the command(s) right after the `-exec`, where `{}` is the "placeholder" for where the file name will be passed to, and `;` (which needs to be escaped with a `\` backslash) stops `exec` from taking command arguments. Overall, `exec` provides an alternate way to take the output from `find` and use them as command line arguments for other commands, such as `grep`.

<br/>

Example 2:

```
$ find skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ -name "ch1.txt" -exec touch -m {} \;

$ find skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ -ctime -1
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch1.txt
```
In the code block above, I first look for the file in the directory `Kauffman` with the name `ch1.txt`, and then I use `exec` to pass the file as a command line argument for the command `touch`. With `touch -m`, I updated the time I last changed `ch1.txt` to right now. I then check that the change time has been updated by using `-ctime -1`, which looks for all the files in the `Kauffman` directory that have been changed less than 1 day ago. As shown in Part 2, originally, when I used  `-ctime -1` in the `Kauffman` directory, nothing appeared because I had never changed the files other than when I created them. However, after I touched `ch.1.txt` to update the change time to now, `ch1.txt` becomes the only file that is outputted when `-ctime -1` is used. Overall, `exec` provides an alternate way to take the output from `find` and use it as command line arguments for other commands, such as `touch`.

