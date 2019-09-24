# Intro to SQL for Querying Databases

**This workshop is under development. It should be complete before Nov. 6, 2019.**  The goal is to write a workshop that teaches the basics of (non-spatial) SQL using DB Browsesr and SQLite.

This workshop provides an overview of the utility and base SQL commands for working with data in a relational database. We’ll focus on querying data to get to know a database and answer questions, and combining data from separate tables. 

## Goals
After this workshop learners should be able to:
 * Perform common SQL commands including sorting, filtering, calculating values, aggregating, combining data, and basic data cleaning (i.e. replace missing values).
 * Combine commands to construct a query to answer a specific question.
 * Identify the benefits of working with SQL.
 * Access additional resources for using SQL in other software like R.

## Prereqs
No prior programming experience is necessary. Bring your laptop with SQLite installed (http://www.sqlitetutorial.net/download-install-sqlite/) and running. 



# Concepts

## What is a Relational Database?

A database is a set of data in tables that are related to each other in some way. That's it. It's just a collection of tables.

Ideally each table can be connected to another table by a column that both tables have that store the information to match up the rows. This column is called a **key**. A key commonly used on campus is your student or employee ID number.

Let's look at an example dataset of student data with data about courses, grades, and employment.  Can we say anything about the relationship between course grades and employment based on this data?

**Table: Student**

|ID|Name|
|--|--|
|123|Jane Smith|
|456|Maria Martinez|
|789|Paul Jones|

**Table: Courses**

|ID|Course|Grade|
|--|--|--|
|123|Calculus|A-|
|456|Calculus|A|
|789|Calculus|C+|
|123|Data Science|A-|
|456|Data Science|B|
|789|Data Science|B-|

**Table: Employment**

|ID|Position|Employer|HoursPerWeek|
|--|--|--|--|
|123|Student Assistant|University Research Lab|5|
|456|Customer Service|Alumni Center|5|
|456|Research Assistant|University Research Lab|15|
|789|Student Assistant|University Research Lab|10|
|789|Stock Room|Medical Supplier|20|
|789|Customer Service|Alumi Center|15|

## What is Spatial SQL?
SQL stands for "structured query language" and it's a language that allows you to ask questions of a database. 

In the above example, it would be much easier to understand the relationships if we build a table aggregating and reshaping our data.  SQL allows us to do that.

### You're Already Doing This!

Researchers typically are already thinking about querying data.  

Imagine you have a table about air quality data.  It contains columns with measurements about various environmental properties such as the temperature, the level of ozone, and perhaps measurements of various particulates.

If you've ever subsetted data in R, for example, you've already done something similar to writing an SQL query! The R code `subset(airquality, Temp > 80, select = c(Ozone, Temp))` becomes `SELECT Ozone, Temp FROM airquality WHERE Temp > 80` in SQL.

In Excel, you might sort your whole spreadsheet on the Temp column, then copy all of the rows that are greater than 80, and paste them into another tab.  You might remove all the other columns except for the Ozone and Temp columns.  You might have also used the cell highlighting tools to change the color of the cells based on the Temp column just to see which cells meet your criteria.

### Why do you want to learn to work with databases and SQL?
 * Efficient
    + Write a few lines of code rather than lots of manual data manipulation
    + SQL is meant for data manipulation
 * Reproducibility 
    + save queries as a record of your workflow
    + re-run code with updates
 * Work with large amounts of data
    + Typically faster to run a process in a database than in a spreadsheet
    + Store lots of data (compare with Excel's row limits)
 * Data management
    + One database file stores many, many tables
    + Write a query instead of making a new files or tabs

### What makes this challenging?
If you currently work in a graphical user interface (GUI), you might be used to being able to see your data, have tools with guided interfaces, and seeing the results of your processing immediately. These aren't things you get with a typical database manager tool, however, you will get used to the typical workflow and seeing everything won't be so necessary.




# Getting Setup

## Install the Software

We'll be using [DB Browser](https://sqlitebrowser.org/), a free, open source, graphical interface for working with SQL databases that works on all major computing operating systems. Installers are available on their [Downloads Page](https://sqlitebrowser.org/dl/).  If you do not have install permissions on your computer, the Portable App version may work without administrator permissions.

## Download the Workshop Data



# Hands On



# Resources
[Sofware Carpentry's SQL Novice Workshop](http://swcarpentry.github.io/sql-novice-survey/)
[Clark Fitzgeralds & Nick Ulle's SQL Workshop](https://github.com/clarkfitzg/SQLworkshop)
[Michele Tobias' Spatial SQL Workshop](https://github.com/MicheleTobias/Spatial_SQL)