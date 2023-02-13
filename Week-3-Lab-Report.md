# Week 3 Lab Report

## Investigating the command `find`

## Part 1: Using `find` with `-name` and `-type`

---------------------------------------------------------

You can use both `-name` and `-type` to narrow down the item that you are looking for!

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

Example 2: 

```
$ find skill-demo1-data/written_2/travel_guides/ -name "History*" -or -name "*-History*" -type f

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
