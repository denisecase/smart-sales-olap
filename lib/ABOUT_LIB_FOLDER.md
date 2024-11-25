# About the lib Folder

The project lib folder contains external libraries required for proper functioning of the BI analytics workflow. 
It includes the SQLite JDBC driver, which allows PySpark to connect to the SQLite database in our data warehouse.

## Purpose

- SQLite JDBC Driver - essential for enabling Spark to read and write data to/from SQLite database using the JDBC (Java Database Connectivity) interface.

## Adding External Libraries

To add external libraries like the SQLite JDBC driver:
1. Download the JAR file from a trusted source, such as Maven Central.
   - [Download SQLite JDBC from Sonatype Central Repository](https://central.sonatype.com/artifact/org.xerial/sqlite-jdbc)
2. Place the downloaded .jar file into the lib folder of the project.

## Current Libraries

As of now, the following library is present in the lib folder:

- sqlite-jdbc-3.41.2.jar: The JDBC driver for SQLite, required for Spark to communicate with SQLite databases.

## Usage in Project

When initializing the Spark session in your Python scripts, the path to the JAR file is provided to Spark so it can load the necessary drivers. 
This is handled programmatically within the script like so:

