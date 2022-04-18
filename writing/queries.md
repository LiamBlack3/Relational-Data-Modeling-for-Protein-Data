### cs312F2022

Please add your responses to this file.

#### Lab 3 Assignment
#### Relational Data Modeling for Protein Data: four tables

#### Name
Liam Black

#### GitHub Account Name
LiamBlack3

#### Submission Date
28 March 2022


Please respond to the lab assignment sheet's questions-in-blue below.


#### 1)

 - Your response 1:

```
1. How many sars protID from the nprot database are there?
2. Count all distinct protID from nprot,saprot, and mprot.

```

 - Your response 2:

```
2. Count all distinct protID from nprot,saprot, and mprot.
```

---
#### 2)

 - Your response:

```
Each protein ID is different than the next, meaning there are no duplicates so saying distinct here won't make a difference.
```

```

---
#### 3)

 - Your query: List distinct orgranisms that are common to sara and nprot

```
select distinct(n.organism) from nprot n, sars sa where sa.protID == n.protID;

```

 - Result:

```
SARS coronavirus CUHK-AG02
SARS coronavirus civet010
SARS coronavirus Sino3-11
Bat coronavirus RacCS264
SARS coronavirus A022
Bat SARS coronavirus HKU3-8
Civet SARS CoV 007/2004
Cardioderma bat coronavirus/Kenya/KY43/2006
SARS coronavirus ShanghaiQXC2
Bat SARS-like coronavirus Rs3367
SARS coronavirus TW-GD4
SARS coronavirus BJ182a
Porcine transmissible gastroenteritis coronavirus (strain Purdue) (TGEV)
Bat coronavirus Rp3/2004 (BtCoV/Rp3/2004) (SARS-like coronavirus Rp3)
Murine coronavirus (strain A59) (MHV-A59) (Murine hepatitis virus)
Bat coronavirus 279/2005 (BtCoV) (BtCoV/279/2005)
SARS coronavirus TW-YM4
Bat SARS coronavirus HKU3-13
SARS coronavirus TW-HP3
Bat SARS coronavirus HKU3-7
Bat coronavirus Rp/Shaanxi2011
SARS coronavirus TW-HP2
Bat SARS coronavirus HKU3-2

```

---
#### 4)

 - Your query:

```
select count(distinct(n.organism)) from nprot n, sars sa, mprot m where sa.protID == n.protID AND sa.protID == m.protID;

```

 - Result:

```
124
```

---
#### 5)

 - Your query:

```
select count(distinct(protID)) from sars where organism == "Mus musculus (Mouse)";

```

 - Result:

```
24
```

---
#### 6)

 - Your query:

```
 select AVG(Length) from sars where organism == "Mus musculus (Mouse)"; 

```

 - Result:

```
445.583333333333
```

---
#### 7)

 - Your query:

```
 select MAX(Length) from sprot where organism == "Mus musculus (Mouse)";


```

 - Result:

```
892
```

---
#### 8)

 - Your query:

```
select protID, organism from sars where Length == 240;

```

 - Result:

```
J5KAT3|SAR86 cluster bacterium SAR86B
A0A7K6YNH5|Alca torda (Razorbill)
J4WQ88|SAR86 cluster bacterium SAR86A
J5KHS7|SAR86 cluster bacterium SAR86B
J4WVK4|SAR86 cluster bacterium SAR86B
J5KAD0|SAR86 cluster bacterium SAR86B
J4KSX0|SAR86 cluster bacterium SAR86B
J4KT08|SAR86 cluster bacterium SAR86B
J4KSJ5|SAR86 cluster bacterium SAR86B
```

---
#### 9)

 - Your query:

```
select protID, organism from nprot where Length == 220;


```

 - Result:

```
A0A6F8IJN5|Bat coronavirus HKU5 (BtCoV) (BtCoV/HKU5/2004)
A0A0U1WHM6|BtPa-BetaCoV/GD2013
A0A7L1IJZ4|Smutsornis africanus (Double-banded courser) (Rhinoptilus africanus)
A0A7L0H8L9|Arenaria interpres (Ruddy turnstone) (Tringa interpres)
E0ZN63|Bat coronavirus HKU9-10-2
A0A6B9KDE2|Pipistrellus abramus bat coronavirus HKU5-related
B9UYN4|Porcine epidemic diarrhea virus
A3EXF4|Bat coronavirus HKU5-3
A0A7K7BQA5|Aphelocoma coerulescens (Florida scrub-jay) (Corvus coerulescens)
A3EXE5|Bat coronavirus HKU5-2
A0A6N1WKV1|Severe acute respiratory syndrome coronavirus 2 (2019-nCoV) (SARS-CoV-2)
E0ZN55|Bat coronavirus HKU9-10-1
A3EXG3|Bat coronavirus HKU5-5
A3EXI5|Bat coronavirus HKU9-3
A3EXD6|Bat coronavirus HKU5 (BtCoV) (BtCoV/HKU5/2004)
E0ZN39|Bat coronavirus HKU9-5-1
A0A7T5Y1P2|Bat coronavirus

```

---
#### 10)

 - Your response:
 I noticed there was a trend of very similar named proteins, and organisms that had the desired length of 220 or 240 when plugged into the query.





---

#### 11)

 - Your response:

```
How many distinct protein names are there in total, including all four tables?

```


 - Your query:

```
select count(distinct(sa.ProteinName)) from nprot n, sars sa, mprot m where sa.protID == n.protID AND sa.protID == m.protID;


```

 - Result:

```
3
```


---
(Did you remember to add your name at the top of this document?)
