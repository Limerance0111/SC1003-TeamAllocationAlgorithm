# Team Allocation Algorithm Project

This repository contains a Python-based project that automatically allocates students into fair and balanced teams based on a set of team-formation constraints.

## Project Overview

The goal of the project is to assign students into project groups of 5 while maintaining fairness across:

- School diversity
- Gender balance
- Academic balance (CGPA range)

The solution reads student records from a CSV file, groups students by tutorial section, applies allocation rules, and exports the final team assignments.

## Files in this Repository

- `Mini Project.ipynb` — main notebook containing the project implementation and explanation
- `records.csv` — raw student data used for allocation
- `grouped_students (1).csv` — generated grouped output file
- `Mini Project Requirements - Student (2).pdf` — project specification and requirements

## What the Algorithm Does

The workflow includes:

1. Reading and preprocessing student records
2. Categorizing CGPA values into ranges
3. Grouping students by tutorial group
4. Checking fairness constraints for each team
5. Forming project teams using rule-based selection and fallback logic
6. Trying swaps to improve balance when violations occur
7. Exporting final results to CSV

## Constraints Applied

Each team is designed to satisfy the following rules:

- Gender composition should follow a balanced pattern such as 2 males + 3 females or 3 males + 2 females
- No more than 2 students from the same school in one team
- No more than 2 students in the same CGPA category in one team

## How to Use

Open the notebook in Jupyter and run the cells in sequence:

```bash
jupyter notebook "Mini Project.ipynb"
```

If you are using the same project structure, ensure the CSV files are in the same directory as the notebook before running the allocation code.

## Expected Output

The program generates a grouped output CSV containing each student's:

- tutorial group
- assigned team number
- student ID
- name
- school
- gender
- CGPA

## Notes

This project is a practical implementation of computational thinking principles, including:

- decomposition
- abstraction
- pattern recognition
- algorithmic thinking

## License

This project does not currently include a license file. If you plan to share or distribute it publicly, you may want to add an open-source license such as MIT.
