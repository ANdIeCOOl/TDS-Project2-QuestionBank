# TDS-Project2-QuestionBank
Question Bank for all TDS assignments

#Requested format
# Student Assignments Directory Structure

Each student has a folder named with their roll number. Inside each student's folder, there are multiple assignment folders (`Assignment_X`). Each assignment contains:
- A `.txt` file with the question statement.
- A corresponding `.py`, `.sh`, or `.js` file for the solution.

## Example Directory Structure
RollNo_12345/
├── Assignment_1/
│   ├── Q1.txt    # Question for Q1
│   ├── Q1.py     # Solution in Python
│   ├── Q2.txt    # Question for Q2
│   ├── Q2.sh     # Solution in Bash
│   ├── Q3.txt    # Question for Q3
│   ├── Q3.js     # Solution in JavaScript
├── Assignment_2/
│   ├── Q1.txt
│   ├── Q1.py
│   ├── Q2.txt
│   ├── Q2.sh
│   ├── Q3.txt
│   ├── Q3.js


## Command to Generate This Structure in Linux

Run the following script to create the directory structure:

```bash
for roll in 12345 12346 12347; do
  for assignment in {1..2}; do
    mkdir -p RollNo_${roll}/Assignment_${assignment}
    for q in {1..3}; do
      touch RollNo_${roll}/Assignment_${assignment}/Q${q}.txt
      touch RollNo_${roll}/Assignment_${assignment}/Q${q}.py
      touch RollNo_${roll}/Assignment_${assignment}/Q${q}.sh
      touch RollNo_${roll}/Assignment_${assignment}/Q${q}.js
    done
  done
done
