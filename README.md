# Encrypted Distibuted File System 

## Introduction
We have designed multi-threaded concurrent server which can access by N users to create and access their file systems. Replicated server also used for high availability, backup and disaster recovery.
- All the directories,file name and file content are encrypted.
- AES encryption algorithm is used in the project.
- Created a UI for better usage of the features.

### To operate the application user has to perform below steps:
  1) **User Signup** : using this module user can register with the application and server will provide one directory space for that user
  2) **User Login**  : using this module user can login to application
  3) **File System Modules** : after login user can create their own directories and can create file in those directories and can delete, rename, write                                    data to those files
  4) **Share Access System** : using this module user can share READ and WRITE access with other user by selecting a desired file

## Requirements :
- Python 3.7+
- MySQl database 5.5+
- Python Libraries:
    - pyaes <br />
      ``` pip install pyaes ```
    - pbkdf2 <br />
      ``` pip install pbkdf2 ```
    - PyMySql <br />
      ``` pip install PyMySQL==0.9.3 ```

## Running the system

### Building the database
  - create a database and use <br />
    ``` 
        create database distributed; 
        use distributed;
     ```
  - create table register and access <br />
    ```
      create table register(username varchar(30) primary key,
      password varchar(30),
      contact varchar(12));
      
      create table access(owner varchar(30),
      user varchar(30),
      filename varchar(30) primary key,
      access_mode varchar(30));
    ```
  
### Building the servers
  - Run the server from "DistributedServer" Folder.
    ```
      python Server.py
    ```
  - Run the replica server from "DistributedServer2" Folder.
    ```
      python Server2.py
    ```

### Client usage:
  - In Client.py modify the mysql details with the details used when setting up mysql in system.
  - Run the Client.py program
    ```
      python Client.py
    ```
  - In the popup screen regester using new user sighup
  - Login to the page 
  - create/delete/rename/update file transactions are allowed.
  - All the data in the backend are encrypted.

### **NOTE** 
In order to run servers and client in multiple machines use ip-address of the machine instead of localhost and update it in client.py,Server.py and Server2.py.
