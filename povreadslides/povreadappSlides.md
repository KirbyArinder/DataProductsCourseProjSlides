An app to illustrate the separation of poverty effects from school district performance rank on a Mississippi third-grade reading test
========================================================
author: Kirby Arinder
date: 6/20/2015

What's going on here?
========================================================

- Mississippi recently administered a reading test to all public-school third graders.

- This test is very high-profile; its results will likely shape a lot of public policy.

- There is a strong relationship between district-level poverty and pass rates on this test.  

So where does this app come in?
========================================================

- Sometimes we're concerned with raw pass rate on this test.  

- But sometimes, we want to know which districts are doing well or poorly, *relative to poverty level*.

- This app shows us just that.  

How?
========================================================

- Data were collected from the U.S. Census and Mississippi Department of Education websites.

- Data processing, analysis, and model-building were done in a separate file, to save bandwith and speed up the app.

- The current app provides poverty and passrate information for all 144 school districts in the state, along with a measure of wealth-relativized performance.  It also ranks each district on each of these features. 

Under the hood
========================================================

- Here's a look at some of the underlying data:  


```r
povreaddata <- read.csv("data/povertyreadingranked.csv")
head(povreaddata)
```

```
  X                     distnames Passrate  Poverty      fit correctedpass
1 1      Aberdeen School District       88 37.22359 82.70583     1.0640120
2 2         Alcorn County Schools       91 25.10833 89.79520     1.0134172
3 3  Amite County School District       78 35.98805 83.42882     0.9349287
4 4         Amory School District       88 31.01380 86.33956     1.0192315
5 5 Attala County School District       88 33.57825 84.83894     1.0372595
6 6       Baldwyn School District       93 28.78636 87.64297     1.0611234
  passrank corpovrank povrank
1       67         33      90
2       47         71      29
3      111        117      83
4       67         63      59
5       67         47      70
6       25         34      44
```
