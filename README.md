# SC1003: Team Allocation Algorithm

## Project Title
Student Team Allocation Using Fairness Constraints

## Introduction
This project was developed as part of the SC1003 coursework requirement. The aim of the assignment was to design an algorithm that groups students into balanced project teams based on fairness and diversity rules.

The main challenge was to allocate students into teams of 5 while ensuring that no team was unfairly dominated by a single school, gender, or academic performance category. The algorithm reads a dataset of students, performs preprocessing, applies balancing rules, and produces the final grouped output.

## Objective
The objective of this project is to:

- read student data from a CSV file
- group students by tutorial section
- assign students into project teams of 5
- ensure fairness across gender, school, and CGPA distribution
- generate a final output file containing team allocations

## Problem Statement
In a large class, it is important for project teams to be formed fairly so that each team has a balanced mix of students. A team should not be dominated by one gender, one school, or one academic level.

The project therefore applies the following fairness constraints:

1. Gender balance: teams should ideally be in a 2:3 or 3:2 male-to-female ratio.
2. School diversity: no more than 2 students from the same school in a team.
3. Academic balance: no more than 2 students from the same CGPA range in a team.

## Dataset
The repository contains the following files:

- `records.csv` — original student data
- `grouped_students (1).csv` — generated team allocation output
- `Mini Project.ipynb` — notebook containing the full implementation
- `Mini Project Requirements - Student (2).pdf` — assignment requirements

## Methodology
The solution is implemented in Python and follows a structured workflow:

1. Import necessary libraries
2. Read the student records from CSV
3. Categorize CGPA into academic ranges
4. Group students by tutorial section
5. Check whether a candidate student can be added to a team without violating constraints
6. Form teams using rule-based selection
7. Attempt swaps to improve team balance if violations are found
8. Export the final grouped results as a CSV file

## Computational Thinking Concepts Applied
This project demonstrates several core computational thinking principles:

- Decomposition: The problem was broken into smaller tasks such as reading data, grouping students, validating constraints, and exporting output.
- Abstraction: Each student was represented using essential attributes such as school, gender, tutorial group, and CGPA.
- Pattern Recognition: Similarities in gender, school, and academic level were identified to build fair teams.
- Algorithmic Thinking: The team-building process used structured decision rules and iterative checks.

## Key Functions
The notebook includes functions such as:

- `cgpa_range()` — classifies CGPA into ranges
- `readstudents()` — loads student records from CSV
- `grp_with_tut()` — groups students by tutorial section
- `checkconstraints()` — validates whether a team satisfies fairness constraints
- `canadd()` — checks whether a student can be added to a partial team
- `pick_student()` — selects a suitable student for the team
- `formgrps()` — creates the student groups
- `try_swap_fix()` — attempts to resolve team violations
- `savegrps()` — saves the final team allocation to CSV

## Output
The final output file, `grouped_students (1).csv`, contains each student's assigned tutorial group and team number, along with their personal information such as:

- Student ID
- Name
- School
- Gender
- CGPA

## Results and Discussion
The algorithm successfully generates teams based on predefined fairness conditions. Although some groups may still require additional adjustment in certain edge cases, the project demonstrates a practical approach to balancing team formation using constraint-based logical checks.

This project is useful for understanding how computational problems can be translated into rule-based algorithmic solutions in real-world scenarios.

## Conclusion
This project shows how Python can be used to solve a real allocation problem by combining data processing, logic design, and optimization. It highlights the importance of fairness in team assignment and demonstrates how computational thinking can be applied to create balanced and efficient groupings.

## References
- Project requirements document provided in the repository
- Coursework materials for SC1003

## Notes
This repository is intended for academic submission and learning purposes.
