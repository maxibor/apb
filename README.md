# APB : **A** **P**roject **B**alloter
*A specific [multi-objective optimization](https://en.wikipedia.org/wiki/Multi-objective_optimization) short program.*  
Given a specially formatted `.csv` file, APB selects for each student the best project according to the voted rank, while trying to be fair with every other student.


## Requirements
- Python 3
- Pandas
- Numpy

## Installation

```c
git clone https://github.com/maxibor/apb
cd apb
chmod +x apb
```

## Example

```c
apb ./data/example.csv
```

## Get Help

```
usage: APB: A Project Balloter [-h] [-maxRank MAXRANK] [-maxStud MAXSTUD] file

Choose a project for each student given a ranked project list.

positional arguments:
  file              .csv entry file of ranked project list per student

optional arguments:
  -h, --help        show this help message and exit
  -maxRank MAXRANK  Worst Rank acceptable for all student. Default = 3
  -maxStud MAXSTUD  Maximum number of students per project. Default = 2
```

## CSV file formatting Example
Column names contain student names.  
Row names contain project names.  
Cells contains ranking of each project by each student.

|            | student_1 | student_2 | student_3 | student_4 | student_5 | student_6 | student_7 | student_8 | student_9 | student_10 | student_11 | student_12 | student_13 | student_14 | student_15 | student_16 |
|------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|------------|------------|------------|------------|------------|------------|------------|
| project_1  | 8         | 1         | 10        | 6         | 10        | 4         | 8         | 2         | 1         | 1          | 10         | 8          | 7          | 2          | 6          | 10         |
| project_2  | 3         | 2         | 1         | 7         | 3         | 2         | 2         | 6         | 10        | 2          | 4          | 6          | 8          | 10         | 7          | 4          |
| project_3  | 7         | 3         | 9         | 1         | 9         | 9         | 3         | 1         | 4         | 9          | 7          | 1          | 4          | 6          | 1          | 1          |
| project_4  | 2         | 5         | 8         | 4         | 1         | 10        | 1         | 9         | 3         | 7          | 1          | 10         | 2          | 8          | 10         | 9          |
| project_5  | 10        | 4         | 6         | 8         | 2         | 1         | 10        | 5         | 7         | 3          | 2          | 4          | 9          | 4          | 4          | 5          |
| project_6  | 1         | 8         | 5         | 10        | 4         | 6         | 4         | 4         | 5         | 5          | 6          | 2          | 5          | 7          | 3          | 7          |
| project_7  | 9         | 6         | 4         | 5         | 8         | 5         | 5         | 8         | 2         | 4          | 5          | 7          | 10         | 3          | 2          | 3          |
| project_8  | 6         | 10        | 2         | 9         | 6         | 8         | 6         | 3         | 9         | 8          | 8          | 3          | 1          | 5          | 8          | 2          |
| project_9  | 4         | 7         | 3         | 3         | 7         | 7         | 9         | 7         | 8         | 10         | 9          | 9          | 3          | 9          | 9          | 8          |
| project_10 | 5         | 9         | 7         | 2         | 5         | 3         | 7         | 10        | 6         | 6          | 3          | 5          | 6          | 1          | 5          | 6          |

## Example Output

```
student_1 : project_6  - Choice n° 1
student_10 : project_1  - Choice n° 1
student_11 : project_4  - Choice n° 1
student_12 : project_6  - Choice n° 2
student_13 : project_8  - Choice n° 1
student_14 : project_10  - Choice n° 1
student_15 : project_7  - Choice n° 2
student_16 : project_8  - Choice n° 2
student_2 : project_3  - Choice n° 3
student_3 : project_2  - Choice n° 1
student_4 : project_10  - Choice n° 2
student_5 : project_5  - Choice n° 2
student_6 : project_5  - Choice n° 1
student_7 : project_2  - Choice n° 2
student_8 : project_3  - Choice n° 1
student_9 : project_4  - Choice n° 3
```
