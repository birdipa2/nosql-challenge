# nosql-challenge
## Eat Safe, Love - A Food Hygiene Data Analysis

This repository includes two Python MongoDB scripts: **NoSQL_setup_starter.ipynb** and **NoSQL_analysis_starter.ipynb**, one **ReadMe** file and a **Resources** folder containing the ratings data of various establishments: **establishments.json**

The **NoSQL_setup_starter.ipynb** script has been used to perform Part 1 and Part 2 of the challenge. The script:

>sets up a MongoDB database named uk_food with a collection named establishments populated with data from an establishments.json file.

>Performs various updates on the database, including:

>Adding a new restaurant to the collection.

>Updating specific fields in the collection.

>Deleting all documents related to a specific local authority.

>Converting string fields to number fields where applicable.

### Getting Started

Before running the script, make sure to import the establishments.json data file to your MongoDB instance. Use the following command in your terminal:

mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json

This command creates a new database named uk_food and a new collection named establishments, and imports the data from establishments.json.

### Prerequisites

The script requires MongoDB to be running on your system. You also need Python, with the pymongo package installed. You can install it via pip:

pip install pymongo

### How to Run the Script

Clone the repository to your local machine.

Navigate to the repository's root directory in your terminal.

Run python script_name.py in your terminal, replacing script_name.py with the actual script's name.

The script will connect to your MongoDB instance, perform the operations, and print the results to the terminal.

### Description of Operations

#### Part 1: Database and Jupyter Notebook Set Up

The script begins by importing the necessary Python libraries and establishing a connection with the MongoDB instance. 

It assigns the uk_food database and establishments collection to variables for ease of use.

#### Part 2: Update the Database

The script then performs several updates on the database, such as:

Adding a new restaurant "Penang Flavours" to the database.

Finding the BusinessTypeID for "Restaurant/Cafe/Canteen" and updating the new restaurant with this BusinessTypeID.

Removing all establishments associated with the Dover Local Authority.

Converting latitude, longitude, and RatingValue to appropriate number data types.

#### Part 3: Exploratory Analysis

The **NoSQL_analysis_starter.ipynb** script performs exploratory data analysis on the food establishment data.

The exploratory analysis is divided into four parts:

##### 1. Finding Establishments with a Hygiene Score of 20

The code finds establishments with a hygiene score of 20, counts the number of such documents, prints the first such document, and then converts the result into a Pandas DataFrame.

##### 2. Finding Establishments in London with a RatingValue Greater Than or Equal to 4

The code finds establishments with LocalAuthorityName containing "London" and RatingValue greater than or equal to 4. 

It then follows the same steps as the first part to count, print, and convert to a DataFrame.

##### 3. Top 5 Establishments with a RatingValue of 5, Sorted by Lowest Hygiene Score, Nearest to "Penang Flavours"

The code finds the top five establishments with a RatingValue of 5, sorted by the lowest hygiene score, which are nearest to the newly added restaurant "Penang Flavours". 

The result is converted into a DataFrame.

##### 4. Number of Establishments in Each Local Authority Area with a Hygiene Score of 0

The code counts the number of establishments in each local authority area with a hygiene score of 0, and then sorts them from highest to lowest. 

The result is converted into a DataFrame.

#### Contact

If you have any questions or feedback about this script, please feel free to contact me at param.birdi@utoronto.ca.

#### Acknowledgments

This code was written by Paramdeep Singh Birdi as part of a project for a data analysis course. 

Most of the data used in this project was provided by the course instructors.
