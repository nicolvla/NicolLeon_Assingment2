# Analysis of 'American Community Survey' - 2022

This repository contains data, analytic code, and findings about foreign-born population in the United States.

## Data

This analysis uses one spreadsheets containing information colected by the Census Bureau, through the American Community Survey, in 2022, about foreign-born population. Specifically about how many are heads of household, female heads of household, foreign-born women over the age of 16 are employed, and the poverty levels among foreign-born female heads of household who care for children under the age of 18 and under the age of 5.

The spreadsheet come from the following sources:

- Name of source:
  - `Raw_Data_Cleaning.csv`: Raw data of 'American Community Survey'
  - `FB22.csv` : Cleaned data 'American Community Survey'

Each of the spreadsheets contain, among others, the following columns relevant to the analysis:

- `Poverty rates for families and people for whom poverty status is determined All families` — Of the total population in poverty, the percentage of foreign families in poverty.
- `Withrelatedchildrenofthehouseholderunder18years` — Of the total number of people in poverty, the percentage of foreign women in poverty who care for children under 18.


## Methodology

The notebook [`Assingment_2_NicolLeon.ipynb`](notebooks/Assingment_2_NicolLeon.ipynb) performs the following analyses:

##### Part 1: Obtaining and cleaning the data

- I used the "American Community Survey-2022" database from the Census Bureau. I used advanced search and focused only on the foreign-born population. I downloaded the database in .csv format and uploaded it to Spreadsheets. I created a new sheet to apply the "Transpose" function and display the states as rows and the variables as columns. Then, I performed a special paste into a new sheet. In another sheet, I applied "=SUBSTITUTE(A1, ",", "")" to remove all commas "," from the numbers, and "=LEFT(A1, LEN(A1)-1)" to remove the "%" symbol. In a new Spreadsheets file called "FB22," I did a special paste and downloaded it.


##### Part 2: Analizing the data

- In Jupyter, I imported this "FB22" database. Then, I selected the columns I was interested in and used "dtypes" to specify the format in which I wanted them interpreted by Python. I created new columns to calculate the number of foreign women households, the number of foreign women households caring for children under 18, the percentage of foreign women over 16 working, and the percentage of foreign heads of household. Finally, I filtered each variable from highest to lowest to identify the key states.


## Outputs

The notebooks output this spreadsheet which contains TKTK: [`fb22_filtered_v1.csv`](fb22_filtered_v1.csv).

## Running the analysis yourself

You can run the analysis yourself. To do so, you'll need the following installed on your computer:

- Python 3
- The Python libraries specified in [`requirements.txt`](requirements.txt)

## Licensing

All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). The data file in the output/ directory is available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

## Feedback / Questions?

Contact YOUR NAME HERE at nicol.leonarge36@journalism.cuny.edu.
