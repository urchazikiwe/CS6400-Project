# CS6400-Project

Project Proposal for Data Mining of Online Retail Dataset Using Pentaho BI Suite

Follow the steps outlined here to be able to replicate this project

Here is a breakdown of the steps:

PREPARATION STEPS:
*********************************************************

1. Download sample data from: https://archive.ics.uci.edu/dataset/352/online+retail

2.Download and Install MYSQL 8.3
  i. Download MYSQL 8.3 from: https://downloads.mysql.com/archives/community/ #Select product version 8.3 and operating system Microsoft windows
      Run the windows installer to install MYSQL on your computer.
      Start MYSQL and make sure you can connect to the database server.

      Create a database called: online_retail and a table called: transactions using the script below:

                    CREATE DATABASE Online_retail;

                    CREATE TABLE Transactions (
                    InvoiceNo VARCHAR(250),
                    StockCode VARCHAR(250),
                    Description VARCHAR(250),
                    Quantity INTEGER,
                    InvoiceDate DATE,
                    UnitPrice DECIMAL(10,2),
                    CustomerID INTEGER,
                    Country VARCHAR(250),
                    TotalPrice DECIMAL(10,2),
                    PRIMARY KEY (InvoiceNo, StockCode, InvoiceDate);
      
  ii. Download MYSQL JDBC Driver 8.3 from: https://downloads.mysql.com/archives/c-j/ #Select product version 8.3 and platform independent operating system. Then download the Platform Independent (Architecture Independent), ZIP Archive.
      Unzip file and keep the copy the jar file: mysql-connector-j-8.3.0 to a known location to be used later.

3. Download and Install Pentaho BI products:
   i. Download Pentaho Community Edition version 9.3 from: https://www.hitachivantara.com/en-hk/products/pentaho-platform/data-integration-analytics/pentaho-community-edition.html
       Ensure that selected version is 9.3. you can do this by clicking on the select version dropdown and click on 9.3
   Download the following:
      a. pdi-ce-9.3.0.0-428.zip Pentaho Data Integration (Base Install)
      b. prd-ce-9.3.0.0-428.zip Pentaho Report Designer  (Base Install)
      c. pentaho-server-ce-9.3.0.0-428.zip Pentaho Server archive install assembly

   Install Pentaho BI products:
   1. Refer to the installation guides in this repo sequentiallly to install the Pentaho server:
      a. first, start with the pdf: Prepare your Windows environment for an archive install. Note: For Java, download and install JAVA 11 Windows x64 installer from here: https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html
      b. second, the pdf: Use MySQL as your repository database (Archive installation)

      NOTE: Remember the MYSQL JDBC Driver we downloaded earlier? ensure to copy it to the ...\pentaho_server\tomcat\lib folder.

   At this point your server should be up and running.

   2. Refer to the installation guide named: three-steps-to-install-pentaho-data-integration-ce in this repo to install PDI server. NOTE: Copy the MYSQL JDBC Driver to the ...\data-integration\lib folder
   3. Refer to the installation guide named: Install Pentaho Data Integration and Analytics in this repo to install Pentaho Report Designer. Copy the MYSQL JDBC Driver to the ...\design-tools\report-designer\lib\jdbc folder.




WORKING WITH THE DATA(ANALYTICS)
****************************************************************************

Download the CS6400Project.zip files which contains all the files needed for this part. unzip it.

1. Start with Extracting, transforming and loading the DATA using PDI.
   i. Start PDI(Spoon) using Spoon.bat located in \data-integration\lib folder.
   ii. Once spoon is started, open the transformation: transform_load_data.ktr.
   iii. Run this transformation this will load

      
  
  
