# ECE-2112-PA-4
#### Villanueva, Elle Sandrine P. | 2ECE-C
## Description
This repository contains Programming Assignment 4 for the course Advanced Computer Programming, S.Y. 2026-2027, for the objectives to: 

1. Filter data using several categorical and numerical conditions;
2. Construct DataFrames by selecting relevant features;
3. Summarize the relationship between categorical features and a numerical variable; and
4. Present data comparisons using labeled plots.

## Part A: Visayas Communication DataFrame

```
df = pd.read_excel('board2.xlsx')
df
```
A DataFrame named `VisComm` was created containing students whose Hometown is Visayas and whose Track is Communication with the retained columns of Name, Gender, Math, Electronics, and Average.
The DataFrame was displayed along with the `.shape` of the table, which is (30, 8), or 30 rows and 8 columns.

```
df = df.copy()
df['Average'] = df[['Math','Electronics','GEAS','Communication']].mean(axis=1)

df
```
As the given DataFrame was missing the Average column, ``.mean(axis=1)`` was used to calculate the mean of each row. The resulting DataFrame is:
|  # | Name | Gender | Track            | Hometown | Math | Electronics | GEAS | Communication | Average |
| -: | ---- | ------ | ---------------- | -------- | ---: | ----------: | ---: | ------------: | ------: |
|  0 | S1   | Male   | Instrumentation  | Luzon    |   58 |          89 |   75 |            78 |   75.00 |
|  1 | S2   | Female | Communication    | Mindanao |   52 |          75 |   90 |            52 |   67.25 |
|  2 | S3   | Female | Instrumentation  | Mindanao |   83 |          74 |   77 |            57 |   72.75 |
|  3 | S4   | Male   | Instrumentation  | Visayas  |   65 |          58 |   91 |            68 |   70.50 |
|  4 | S5   | Male   | Communication    | Luzon    |   59 |          86 |   43 |            88 |   69.00 |
|  5 | S6   | Female | Microelectronics | Visayas  |   88 |          45 |   86 |            83 |   75.50 |
|  6 | S7   | Female | Instrumentation  | Luzon    |   66 |          60 |   60 |            48 |   58.50 |
|  7 | S8   | Male   | Instrumentation  | Luzon    |   49 |          81 |   64 |            53 |   61.75 |
|  8 | S9   | Male   | Instrumentation  | Luzon    |   50 |          36 |   63 |            42 |   47.75 |
|  9 | S10  | Male   | Microelectronics | Mindanao |   80 |          84 |   61 |            44 |   67.25 |
| 10 | S11  | Female | Communication    | Visayas  |   48 |          56 |   48 |            67 |   54.75 |
| 11 | S12  | Male   | Communication    | Visayas  |   89 |          67 |   84 |            64 |   76.00 |
| 12 | S13  | Female | Microelectronics | Luzon    |   88 |          35 |   83 |            43 |   62.25 |
| 13 | S14  | Female | Microelectronics | Luzon    |   83 |          77 |   89 |            73 |   80.50 |
| 14 | S15  | Female | Microelectronics | Mindanao |   69 |          41 |   40 |            86 |   59.00 |
| 15 | S16  | Female | Communication    | Luzon    |   71 |          70 |   87 |            81 |   77.25 |
| 16 | S17  | Female | Microelectronics | Mindanao |   81 |          79 |   77 |            45 |   70.50 |
| 17 | S18  | Male   | Communication    | Visayas  |   81 |          40 |   81 |            52 |   63.50 |
| 18 | S19  | Male   | Microelectronics | Luzon    |   79 |          63 |   79 |            71 |   73.00 |
| 19 | S20  | Female | Communication    | Mindanao |   59 |          60 |   62 |            85 |   66.50 |
| 20 | S21  | Female | Microelectronics | Visayas  |   83 |          51 |   68 |            72 |   68.50 |
| 21 | S22  | Female | Communication    | Visayas  |   64 |          39 |   89 |            58 |   62.50 |
| 22 | S23  | Male   | Instrumentation  | Luzon    |   84 |          70 |   74 |            47 |   68.75 |
| 23 | S24  | Female | Microelectronics | Visayas  |   85 |          45 |   60 |            41 |   57.75 |
| 24 | S25  | Male   | Communication    | Luzon    |   74 |          91 |   94 |            42 |   75.25 |
| 25 | S26  | Female | Instrumentation  | Visayas  |   71 |          47 |   83 |            62 |   65.75 |
| 26 | S27  | Male   | Microelectronics | Visayas  |   70 |          47 |   40 |            86 |   60.75 |
| 27 | S28  | Male   | Communication    | Visayas  |   85 |          53 |   80 |            53 |   67.75 |
| 28 | S29  | Male   | Instrumentation  | Mindanao |   73 |          48 |   71 |            62 |   63.50 |
| 29 | S30  | Male   | Instrumentation  | Luzon    |   78 |          81 |   57 |            56 |   68.00 |
*Add Vis filter*
*Add shape*

## Part B: Visayas Female DataFrame

A DataFrame named `VisFemale` is created by selecting female students from the Visayas. The selected columns are Name, Track, GEAS, Electronics, and Average.

The data is then filtered to show students whose Average is at least 60.
```
VisFemale = df.loc[(df['Hometown'] == 'Visayas') &
            (df['Gender'] == 'Female'),
            ['Name','Track','GEAS','Electronics','Average']]
VisFemale[VisFemale['Average'] >= 60]
VisFemale
```
`VisFemale` shows female students from Visayas, with the columns Name, Track, GEAS, Electronics, and Average. This also filters to show whose averages are at least 60. The resulting table is:
|  # | Name | Track            | GEAS | Electronics | Average |
| -: | ---- | ---------------- | ---: | ----------: | ------: |
|  5 | S6   | Microelectronics |   86 |          45 |   75.50 |
| 10 | S11  | Communication    |   48 |          56 |   54.75 |
| 20 | S21  | Microelectronics |   68 |          51 |   68.50 |
| 21 | S22  | Communication    |   89 |          39 |   62.50 |
| 23 | S24  | Microelectronics |   60 |          45 |   57.75 |
| 25 | S26  | Instrumentation  |   83 |          47 |   65.75 |

## Part C: Category-Average Visualization

a. For each feature, compute the mean of Average for every category using Pandas.
The mean of Average for every category was computed with Pandas. ``.groupby()`` ensured that the calculations were organized by the columns Track, Gender, and Hometown.
```
track_ave = df.groupby('Track')[['Average']].mean()
track_ave
```
| **Track**        | **Average** |
| ---------------- | ----------: |
| Communication    |      67.975 |
| Instrumentation  |      65.225 |
| Microelectronics |      67.500 |

**README File Version History**

September 17, 2026 - Initial submission

September 26, 2026 - Edited README file

August 28, 2026 - Added description
