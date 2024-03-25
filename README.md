# 1. DB Planning

Database planning is the first stage of the database application life cycle. In this stage, we plan to collect requirements, analyze, design, implement, and test a database. We may find many errors while making the database.

## 1.1 Reason behind doing this project

There are so many troubles we might face while collecting the donation, keeping the donor details in the memory of all the data, and writing them out. There is also the chance of losing the data.

## 1.2 The plan we made which will remove the problem

The idea of our project is to collect and keep the data on what donors donate and give them a receipt. We will collect all the details of volunteers donations in a database as a record, and in which campaign is held. In our system, a campaign will be arranged, and there will be some volunteers. In that campaign, the donor will donate the money. All the donor information will be recorded. Then, we will give the donor some information with a receipt. All the information on the donor and receipt will be stored at the donation.

# 2. Requirement Analysis

Requirement collection is the process of collecting and analyzing the requirements 
of the database by understanding the scope and boundaries of the database
application and major user views. User views refer to the perspective of 
particular user usage, and analysis involves finding what and how. 
In this part, we need to go through three steps. i) conceptual design, ii) logical 
design, and iii) physical design. After determining conceptual design and logical 
design, we decided to implement it in MySQL. 

## 2.1 Reason behind choosing MySQL

MySQL is a multithreaded, multi-user SQL 
database management System (DBMS). The basic program runs as a server, providing multi-user access to a number of databases. The project’s source code is 
available under terms of the GNU General Public License, as well as under a 
variety of property arguments. MySQL is a database. The data in MySQL is 
stored in Database objects called tables. A table is a collection of related data 
entries that consist of columns and rows. Databases are useful when
categorically storing information.
We need some software to implement the project. Firstly, we 
must install MySQL libraries with MySQL Workbench on our PC. Then, we used
www.draw.io to make the ER diagram for our first design. Later, we need MySQL 
Workbench will make the schema tables, write all queries, and implement them. 
Finally, we need reverse engineering to get the automated ER diagram.

## 2.2 Software specification

 MySQL Libraries 
 MySQL Workbench 8.0 CE 
 draw.io
 Operating system: Windows10

# 3. Database Design
The database design process of creating a design for a database that will support the 
enterprise operations and objectives.
To design our database, we need to select the attribute first, then we will 
determine the relation between them.
Following the DB Planning part, we will have five attributes, i.e., i) campaign, ii) 
volunteer, iii) donor, iv) donation, v) receipt.
We talked about the process in the DB planning part. Now, let’s talk about their
relationship. There are five Primary key (PK) for the Attributes 
uniquely identified by the IDs. I.e. i) campaign_ID, ii) donor_ID, iii) 
volunteer_ID, iv) donation_ID, v) receipt_ID.
Many volunteers will be at one campaign so this is a many-to-one relationship.
Many donors will be involved in the campaign, which is a many-to-one relationship.
Each donor donates, so there is a one-to-one relationship.
Each donor gets a receipt, so that again, is a one-to-one relationship.
There is a separate relationship between Donation and Receipt, so that’s a one-to-one
relationship. 
There is a primary key called Campaign_ID, which can be accessed as a Foreign key 
in the Donor and Volunteer tables. Donor_ID primary key can be accessed as a Foreign 
key in the Donation and Receipt tables. The Donation_ID primary key can be 
accessed as a Foreign key in the Receipt table.


