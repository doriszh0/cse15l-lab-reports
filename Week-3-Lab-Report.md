# Week 3 Lab Report

## Investigating the command `find`
> Note: For all commands, I am starting in the `skill-demo1-server` directory, and the `skill-demo1-data` directory is inside of the `skill-demo1-server` directory, and then the `written_2` directory is inside of the `skill-demo1-data` directory.

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
In the code block above, I am finding anything that has ".txt" at the end of the name AND is also a file. The `f` refers to type file, but there are other options as well, the other more-likely-to-be-used choice being `d` for type directory. Also, to be clear, if there is only a space separating two tests (tests refer to specifications for `find` such as `-name` and `-type`), then it is assumed that there is an operator `-and` in between the two tests, meaning both tests have to be fulfilled. Overall, because you can use patterns to specify certain data items (in this case I am only looking for ".txt" files), as well specify exactly what data type you want (usually either a file or directory), I can easily look through directories to find what I want. 

> (Although it may seem redundant to specify the data item to be type file when I am already looking for names that end in ".txt", which is a file format, you never know if someone ever decides to name a folder "{insert name here}.txt" for some weird reason.)

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
In the code block above, I am finding anything that has a name in the format of "History{Insert name here}" OR "{Insert name here}History" AND is also a file. In this case, I used the operator `-or` in between the two name tests, so that I would get data items in either format. After a data item fulfills one of the name specifications, it is then checked whether or not is a file (The precedence of the evaluation of the operations is just left to right). Overall, because you can use patterns to specify certain data items (in this case I am looking for a specific formatting for the name), as well specify exactly what data type you want (usually either a file or directory), I can easily look through directories to find what I want. 

<br/> <br/>

## Part 2: Using `find` with access/change times such as `-atime` and `-ctime`

---------------------------------------------------------

You can use `-atime` and `-ctime` to narrow down the item that you are looking for!

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
```

```
$ find skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ -atime +1

```

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
```

```
$ find skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ -ctime -1

```

<br/>

> Note: there is also `amin` and `cmin`, which is based on minutes, rather than days.


<br/> <br/>

## Part 3: Using `find` with `-delete`

---------------------------------------------------------

You can use `-delete` to delete the item that you are looking for!

<br/>

Example 1:

```
$ cd written_2/non-fiction/OUP/

$ mkdir RybczynskiCopy

$ cp Rybczynski/ch1.txt RybczynskiCopy

$ find RybczynskiCopy -name "*.txt" -delete
```

Example 2:

```
$ find RybczynskiCopy -delete
```

<br/> <br/>

## Part 4: Using `find` with `exec`

---------------------------------------------------------

You can use `-exec` to ___ the item that you are looking for!

<br/>

Example 1:

```
$ find skill-demo1-data/ -type f -exec grep -l "Lucayans" {} \;

skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt
```

Example 2:

```
$ find skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ -name "ch1.txt" -exec touch -m {} \;

$ find skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ -ctime -1
skill-demo1-data/written_2/non-fiction/OUP/Kauffman/ch1.txt
```

