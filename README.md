# ECE-2112-PA-4
#### Villanueva, Elle Sandrine P. | 2ECE-C
## Description
This repository contains Programming Assignment 4 for the course Advanced Computer Programming, S.Y. 2026-2027, for the objectives to: 

1. Filter data using several categorical and numerical conditions;
2. Construct DataFrames by selecting relevant features;
3. Summarize the relationship between categorical features and a numerical variable; and
4. Present data comparisons using labeled plots.

## Part A: Visayas Communication DataFrame

A DataFrame named `VisComm` was created containing students whose Hometown is Visayas and whose Track is Communication with the retained columns of Name, Gender, Math, Electronics, and Average.
The DataFrame was displayed along with the `.shape` of the table, which is (5, 5,), or 5 rows and 5 columns.

|  # | Name | Gender | Track            | Hometown | Math | Electronics | GEAS | Communication |
| -: | ---- | ------ | ---------------- | -------- | ---: | ----------: | ---: | ------------: |
|  0 | S1   | Male   | Instrumentation  | Luzon    |   58 |          89 |   75 |            78 |
|  1 | S2   | Female | Communication    | Mindanao |   52 |          75 |   90 |            52 |
|  2 | S3   | Female | Instrumentation  | Mindanao |   83 |          74 |   77 |            57 |
|  3 | S4   | Male   | Instrumentation  | Visayas  |   65 |          58 |   91 |            68 |
|  4 | S5   | Male   | Communication    | Luzon    |   59 |          86 |   43 |            88 |
|  5 | S6   | Female | Microelectronics | Visayas  |   88 |          45 |   86 |            83 |
|  6 | S7   | Female | Instrumentation  | Luzon    |   66 |          60 |   60 |            48 |
|  7 | S8   | Male   | Instrumentation  | Luzon    |   49 |          81 |   64 |            53 |
|  8 | S9   | Male   | Instrumentation  | Luzon    |   50 |          36 |   63 |            42 |
|  9 | S10  | Male   | Microelectronics | Mindanao |   80 |          84 |   61 |            44 |
| 10 | S11  | Female | Communication    | Visayas  |   48 |          56 |   48 |            67 |
| 11 | S12  | Male   | Communication    | Visayas  |   89 |          67 |   84 |            64 |
| 12 | S13  | Female | Microelectronics | Luzon    |   88 |          35 |   83 |            43 |
| 13 | S14  | Female | Microelectronics | Luzon    |   83 |          77 |   89 |            73 |
| 14 | S15  | Female | Microelectronics | Mindanao |   69 |          41 |   40 |            86 |
| 15 | S16  | Female | Communication    | Luzon    |   71 |          70 |   87 |            81 |
| 16 | S17  | Female | Microelectronics | Mindanao |   81 |          79 |   77 |            45 |
| 17 | S18  | Male   | Communication    | Visayas  |   81 |          40 |   81 |            52 |
| 18 | S19  | Male   | Microelectronics | Luzon    |   79 |          63 |   79 |            71 |
| 19 | S20  | Female | Communication    | Mindanao |   59 |          60 |   62 |            85 |
| 20 | S21  | Female | Microelectronics | Visayas  |   83 |          51 |   68 |            72 |
| 21 | S22  | Female | Communication    | Visayas  |   64 |          39 |   89 |            58 |
| 22 | S23  | Male   | Instrumentation  | Luzon    |   84 |          70 |   74 |            47 |
| 23 | S24  | Female | Microelectronics | Visayas  |   85 |          45 |   60 |            41 |
| 24 | S25  | Male   | Communication    | Luzon    |   74 |          91 |   94 |            42 |
| 25 | S26  | Female | Instrumentation  | Visayas  |   71 |          47 |   83 |            62 |
| 26 | S27  | Male   | Microelectronics | Visayas  |   70 |          47 |   40 |            86 |
| 27 | S28  | Male   | Communication    | Visayas  |   85 |          53 |   80 |            53 |
| 28 | S29  | Male   | Instrumentation  | Mindanao |   73 |          48 |   71 |            62 |
| 29 | S30  | Male   | Instrumentation  | Luzon    |   78 |          81 |   57 |            56 |

## Part B: Visayas Female DataFrame

A DataFrame named `VisFemale` is created by selecting female students from the Visayas. The selected columns are Name, Track, GEAS, Electronics, and Average.

The data is then filtered to show students whose Average is at least 60.

## Part C: Category-Average Visualization

The mean Average is calculated for three categories:

* **Track**
* **Gender**
* **Hometown**

The results are then visualized using bar charts.

The calculated category means are:

| Category | Group            | Mean Average |
| -------- | ---------------- | -----------: |
| Track    | Communication    |       67.975 |
| Track    | Instrumentation  |       65.225 |
| Track    | Microelectronics |       67.500 |
| Gender   | Female           |       66.617 |
| Gender   | Male             |       67.183 |
| Hometown | Luzon            |       68.083 |
| Hometown | Mindanao         |       66.679 |
| Hometown | Visayas          |       65.750 |

The notebook identifies the highest sample mean within each grouping as Communication for Track, Male for Gender, and Luzon for Hometown.


**README File Version History**

September 17, 2026 - Initial submission

September 26, 2026 - Edited README file

August 28, 2026 - Added description
