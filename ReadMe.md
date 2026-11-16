# Module 2 Assignment: Salary Function

## 1. Project Overview

This project focuses on working with the San Francisco employee salary dataset using Python and R. I developed a Python notebook that allows users to search for employee information, organise salary records using a dictionary, and export the selected employee's details into a CSV file. I also included error handling to make the program more reliable when unexpected issues occur.

The final part of the assignment uses R to extract the exported ZIP archive and display the employee information.

## 2. Files Included

The submission contains the following files:

- **`Module_2_Salary_Function_Assignment.ipynb`** – Contains the Python code for importing the salary data, processing employee records, searching for employees, handling errors, and exporting the results.
- **`unzip_employee_profile.R`** – Used to extract the ZIP archive, read the exported CSV file, and display the employee details in RStudio.
- **`README.md`** – Provides an overview of the project and explains how to set up and run both programs.

## 3. Dataset Information

The project uses the San Francisco employee salary dataset referenced in the original `sf-salary.ipynb` notebook. The dataset file is named **`Total.csv`**.

The CSV file is not bundled with this submission, so it needs to be placed in the same folder as the Python notebook before running the program.

The dataset should include an `EmployeeName` column, along with salary-related fields such as `BasePay`, `OvertimePay`, `OtherPay`, `Benefits`, `TotalPay`, and `TotalPayBenefits`.

One thing worth noting is that some employees appear more than once because the dataset covers several years. The lookup function accounts for this by returning all records associated with the entered employee name.

## 4. Requirements and Setup

The following tools are needed to run the project:

- Python 3
- Jupyter Notebook or JupyterLab
- pandas
- R or RStudio

The Python program uses `pandas` for reading and processing the salary data. The `pathlib` and `zipfile` modules are already included in Python, so they do not require separate installation.

To install pandas, run:

```bash
python -m pip install pandas
```

## 5. Running the Python Notebook

Follow these steps to run the Python part of the assignment:

1. Extract the submission ZIP file into a folder on your computer.
2. Download the `Total.csv` dataset and place it in the same folder as the notebook.
3. Open `Module_2_Salary_Function_Assignment.ipynb` using Jupyter Notebook, JupyterLab, or VS Code.
4. Run the notebook cells in order, starting from the first section.
5. When the program asks for an employee's name, enter the full name as it appears in the `EmployeeName` column. The search is not case-sensitive.
6. Review the employee information returned by the program. Where an employee has records from multiple years, all matching records will be displayed.
7. After the lookup, the program saves the selected information and creates the following outputs:

   - `Employee Profile/Employee_Details.csv`
   - `Employee Profile.zip`

The CSV file is saved inside the `Employee Profile` folder. The ZIP archive contains the folder and the CSV file, keeping the folder structure intact for use in R.

## 6. Running the R Script

Once the Python program has created `Employee Profile.zip`, the R script can be used to retrieve the exported information.

1. Open `unzip_employee_profile.R` in RStudio.
2. Make sure the Python export step has been completed and the ZIP archive is available.
3. Click **Source** to run the script.
4. When prompted, locate and select `Employee Profile.zip` if it is not already in the R working directory.
5. The script extracts the archive into a folder named `Employee Profile_R_Extracted`.
6. It then reads `Employee_Details.csv` and displays the employee information in the R console and, when running interactively, the RStudio Data Viewer.

## 7. Error Handling

I included error checks in both programs to make it easier to identify and manage problems during execution.

In Python, these checks cover situations such as a missing dataset, an unreadable CSV file, missing required columns, an empty employee name, an employee name that cannot be found, and file access or permission issues.

The R script also checks whether the ZIP archive and extracted CSV file are available. It reports any problems encountered during extraction or when reading the CSV file.

## 8. Final Checks Before Submission

Before submitting the assignment, I recommend running both the Python notebook and the R script using the actual `Total.csv` dataset.

The executed notebook should be saved with its outputs, and the generated `Employee Profile.zip` should be included as evidence of the Python export process.

The original salary dataset is not included in this submission ZIP. It should be kept separately and supplied alongside the notebook when the program needs to be run again.

