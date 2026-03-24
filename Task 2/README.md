# Task 2 – Equality Analysis (Excel)

## Goal
A dataset with information on employee compensation was supplied by Daikibo Industrials from their four global factories. Every row had an Equality Score between -100 and +100, with 0 denoting perfect equality.
To assist, each score was to be categorized into one of three groups. Determine which areas of the company may be experiencing pay discrimination.

---

## Tools Used
- Microsoft Excel

---

## Classification Criteria

| Equality Score Range | Classification |
|---|---|
| -10 to +10 | Fair |
| -20 to -11 and +11 to +20 | Unfair |
| Below -20 and above +20 | Highly Discriminative |

---

## Steps Taken

### 1. Opened the Dataset
- Opened `Equality Table.xlsx` containing 3 columns:
  - Factory
  - Job Role
  - Equality Score

### 2. Created the Equality Class Column
- Identify the 4th column with the header **Equality Class**
- Applied the following formula to classify each score:
=IF(OR(C2<-20,C2>20),"Highly Discriminative",IF(OR(C2<-10,C2>10),"Unfair","Fair"))

- Dragged the formula down to cover all rows in the dataset

### 3. Saved and Submitted
- Saved the updated file and uploaded it as the task deliverable

---

## Output
The completed Excel file is availablein this folder.
