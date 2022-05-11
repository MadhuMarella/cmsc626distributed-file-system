# cmsc626distributed-file-system
cmsc626distributed-file-system_Group7

Download the following external softwares noted in the "requirements.txt"

install the the following libraries:
pyaes,pbkdf2
using pip install.

once the mysql is downloaded, proceed with the table creation as shown in "database.txt"
it will create 2 tables with names as register and access.
register is used to store the user credentials and access table is used to store the file access rights.

After the completion of tables creation, start the "Server.py" file which is in the "DistributedServer" Folder.
it can be started using command "python Server.py" once you navigated the terminal into "DistributedServer" Folder.

similarly start the "Server2.py" file which is in the "DistributedServer2" Folder.

After successfully starting the Server, open a new terminal and navigate to The Client folder.

Before running the Client.py, Change the mysql details in the code part where replace the root password with the password that you set up at the time of setting the mysql.

once these changes are done, run the Client.py file using the command "python Client.py"

Once it will start it has login and signup page.

Signup if the user is new and login if the user is already present in the database.

After the successful completion of login a new UI will appear where you can perform differnt different file CRUD Operations.


The above procedure will work if you are running the clients and servers in the same machine.

If we want to run the code in different machines then take the ip address of the machine which has server running on it and replace the localhost part in server and Client.py file.


