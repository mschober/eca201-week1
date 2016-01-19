# Week 1 - Lecture


### MAC - install specific steps
1. [install tkinter - ActiveTcl 8.5.18.0](http://www.activestate.com/activetcl/downloads/thank-you?dl=http://downloads.activestate.com/ActiveTcl/releases/8.6.4.1/ActiveTcl8.6.4.1.299124-macosx10.5-i386-x86_64-threaded.dmg)
2. [install pip system wide](https://pip.pypa.io/en/stable/installing/)

### WINDOWS - install specific steps
1. [Windows X86-64 MSI Installer (2.7)](https://www.python.org/ftp/python/2.7/python-2.7.amd64.msi) - Python 2.7
    * Need to check the install for all users box
3. Set the environment variable
    1. win key -> <search 'thispc'> right click -> properties -> advanced system settings -> Environment Variables
    2. Create a new user variable 'PYTHON27_HOME' value: C:\Python27
    3. Create a new user variable 'PATH' value: %PYTHON27_HOME%;%PYTHON27_HOME%\Scripts
    4. win key -> cmd -> python -V
4. Set the tkinter env variables in Fixes section at the bottom

### GENERAL
-------
1. install virtualenv system wide
    ```
    pip install virtualenv
    ```
    
2. create a class directory
3. create a virtualenv 'venv' in class directory
    ```
    virtualenv venv
    ```
    
4. source venv
  * MAC
    ```
    source venv/bin/activate
    ```
    
  * WINDOWS
    ```
    venv\Scripts\activate
    ```

5. pip install openpyxl
    ```
    pip install openpyxl
    ```
    
6. create start_idle.py
    * Code Snippet
    ```
    from idlelib.PyShell import main
    if __name__ == '__main__':
      main()
    ```
    
    * WINDOWS 
       ```
       notepad start_idle.py
       ```
       
        * paste code snippet
        * save and close
        
    * MAC
       ```
       cat > start_idl.py
       <paste code snippet here>
       ^c
       ```


7. python start_idle.py
8. [Copy the example code from openpyxl](https://openpyxl.readthedocs.org/en/2.4/)
9. In idle, File -> new file 'example.py'
10. Paste the example code
11. File -> Save
12. In the idle shell
    ```
    import example
    ```
    
14. Quit idle. Close the example.py file
15. Open the 'sample.xlsx' file
You should see data in the default worksheet generated by the example

### Homework
* [Census](https://www.census.gov/econ/cbp/download/) - Complete County File
* [Consumer Complaints](https://data.consumerfinance.gov/api/views/s6ew-h6mp/rows.csv?accessType=DOWNLOAD)
* [College Score Card](https://s3.amazonaws.com/ed-college-choice-public/CollegeScorecard_Raw_Data.zip)
* [Population by Country](http://en.openei.org/doe-opendata/dataset/a7fea769-691d-4536-8ed3-471e993a2445/resource/86c50aa8-e40f-4859-b52e-29bb10166456/download/populationbycountry19802010millions.csv)

1. Create a new working directory.
2. Create a new virtualenv. **Don't forget to source the env!**
3. Pip install openpyxl.
4. Download the 'Consumer Complaints' as a local csv.
5. Create a python file containing the csv to xlsx converting in this [stackoverflow](http://stackoverflow.com/questions/12976378/openpyxl-convert-csv-to-excel).
6. Modify the code to convert the 'Consumer Complaints'.
7. Convert the csv to xlsx and email to mschober@expedia.com.
   * subject: [eca201] - week1 homework 

### Fixes
* [Fix tkinter windows](https://github.com/pypa/virtualenv/issues/93)
   ```
   set "TCL_LIBRARY=C:\Python27\tcl\tcl8.5"
   set "TK_LIBRARY=C:\Python27\tcl\tk8.5"
   ```
   
   * set these as environment variables

### Supplemental
* [Convert csv to xlsx](http://stackoverflow.com/questions/12976378/openpyxl-convert-csv-to-excel)
