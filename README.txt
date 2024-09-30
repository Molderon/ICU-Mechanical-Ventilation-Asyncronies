The following python3 scripts serve to extract and format a given data query into 
a .csv file saved inside a local directory named "Datasets", the directory will be
created upon execution of the script.



[File Structure]
1. Driving code is within: DataExtraction.py
2. ICU_DataQueries - Loads the SQL queries from the .yaml file
3. MySQL_config.yaml contains all configuration settings!


!!! Must configure .yaml file for your local Database !!!
1. Open 'MySQL_config.yaml'
2. At the beginning of the file configure:
    * Address of Database
    * Database Name
    * Profile name
    * Password

3. Save the File! 


-----------[Optional Python imports] -----------------------------------------------*
                                                                                    |
if the following Python3 imports are missing.                                       |
    -> PyYmal  // interface for .yaml files                                         |
    -> Default Python MySQL interface                                               |
    -> Pandas // Common Data Science formater                                       |
                                                                                    |
- They can be installed via "Optional_Setup_Script"                                 |
  to run the script open a terminal.                                                |
                                                                                    |
  [STEP 1]                                                                          |
                                                                                    |
    Windows: Open Start, search for:                                                |
       cmd // command prompt                                                        |
    Linux: ALT + T or Start: seach for "ter" for terminal :)                        |
                                                                                    |
    MAC: a)Applications > Utilities; b) open terminal                               |
                                                                                    |
  [STEP 2]                                                                          |
    -Use "dir" for Windows to list local files/folders                              |
    -Use "ls" for Linux/Mac to list local files/foledrs                             |
                                                                                    |
    -Navigate to Folder of the script with -> cd + "name of the directory"          |
    -> Run: python3 Optional_Setup_Script.py                                        |
------------------------------------------------------------------------------------*



[Running the Script]
 1. Open a terminal.
 2. Navigate to 'DataExtraction.py' directory
 3. Run -> python3 DataExtraction.py -i

 [MISC]
    The flags -i and -r associate with the current written SQL queries in the .yaml

    1. -i stands for Ivein's dataset representing Asynchronies premature triggering 
    and Double triggering found in Mechanical Ventilation

    2. -r stands for Ralica's dataset representing data for Pressure prediction model
        for Mechanical ventilation
    
    3. Feel free to append new SQL queries, but do not forget to represent them with
       a dedicated tag inside 'ICU_DataQueries.py' and 'MySQL_config.yaml'.