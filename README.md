# Distributed-EHR-Tool-with-MIMIC3-Data
A Distributed Electronic Health Record System and Web-Application Based on MIMIC-3 Data


## Implementation Steps:

The existing MySQL URI assumes a username “root”, and a password “Dsci-551”. Please set up your MySQL with these credentials or replace the relevant parts of the URI’s found in the code files with your credentials.

Host ="localhost",
user="root",
password="Dsci-551"

### Import Data:

Project was built using local MySQL, please utilize local MySQL. 
All files should be executed within the directory they were downloaded from. Please do not remove files from their directories.

1)	Download ‘ImportData’ directory from Google Drive. This file contains our CSV files and python scripts
-	The file path defined in the importcsv.py file that imports data works on the fact that the CSV files are in the same directory as the scripts “ImportData” (which they are)
2)	This directory contains a file “sqlscript.py” which contains our table definitions as well as database creation functions. 
3)	If applicable, replace the URI structure with your MySQL username and password in the files “sqlscript.py” and “importcsv.py”
a)	Existing MySQL URI assumes a username “root”, and a password “Dsci-551”
4)	Execute the python file “sqlscript.py” within the ImportData directory to create the databases and tables
5)	Execute the python file (importcsv.py) within the ImportData directory such that it is able to read the CSV files in this directory 
-	This python script will process each CSV file in chunks and insert the data based on the last digit of the ‘subject_id’ (0-9 resulting in 10 databases) within each CSV file
6)	The data has now been successfully hashed to the correct database


### Database Manager:

1)	Download ‘DBManager’ directory from Drive 
2)	If applicable, replace the URI structure with your MySQL username and password in the dbmanager.py file.
a)	Existing MySQL URI assumes a username “root”, and a password “Dsci-551”
3)	Execute the dbmanager.py within the ‘DBManager’ directory where it is located
4)	DB Manager will be implemented and ready to use




### Front End Application:

1)	Download ‘FrontEndApplication’ directory from Drive 
2)	If applicable, replace the Username and Password structure with your MySQL username and password in the IC_Tool.py file.
a)	 Existing MySQL URI assumes a username “root”, and a password “Dsci-551”
3)	Install all required packages using pip install requirements or other commands suitable for your Python environment. 
4)	Run the python file within the ‘FrontEndApplication’ directory using Streamlit command -
streamlit run IC_Tool.py
The application will open on the default browser. It is recommended to use Anaconda Prompt with Jupyter Notebook installed. Or have the streamlit package installed and added in the Python path.


