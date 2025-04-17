# TourismLethbridgeSite
Requirements:
<br>Python 3.10.11: https://www.python.org/downloads/release/python-31011/
<br>A working XAMPP Server
<br>Add file into htdocs folder after installing files
# Install Guide
To make the Python code to work in your system you need to do the following
<br>Go into your windows powershell or your PC's cmd prompt
<br>Change the directory to your xampp/htdocs server "cd C:\xampp\htdocs" for example
<br>Make sure pip is installed with this command pip --version
<br>If no install is detected do these steps based on your OS
# Windows

<br>run this line to install the dependencies needed to run the python script: 
<br>pip install pandas mysql-connector-python dateparser spacy validators python-dateutil
<br>When running the software you need to setup certain variables in the code for it to actually run on your computer
# MACOS/LINUX
# Connecting to the database
There are lines of code you have to change due to how your database may be set up
<br>In apptest.py in lines 21-24, you should change the connection to the database to the MySQL server IP, and change the login to the database that holds the information from the CSVs
<br>In db.php in lines 2-5, You should do the same as before and connect to the database that holds all the logins and other event information
# Creating the Database
# Running the Python Script
<br>Your python script may NOT work depending on what command you need to run python
<br>On line 12 of the displayTable.php change this line of code to the command you use to call python programs
<br>$command = "py apptest.py " . escapeshellarg($filePath) . " 2>&1"; // Capture errors
<br>$output = shell_exec($command);
<br>Change "py apptest.py" to the comman your computer uses to call this script
<br>If you have a command prompt or powershell inside the directory where "apptest.py" is located you can try commands to see which one executes the program
<br>Common commands are (py, python, python3)
