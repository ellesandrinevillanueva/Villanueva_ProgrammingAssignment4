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
The DataFrame was displayed along with the `.shape` of the table.

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
