# Crowdfunding_ETL
This is the second project in the UC Berkeley Data Analytics Bootcamp.
Crowdfunding_ETL, involved extracting, transforming, and loading data from Excel files into a PostgreSQL database.


## Subsection 1: Category and Subcategory DataFrames
In the first subsection, the Category and Subcategory DataFrames were created. The crowdfunding.xlsx Excel data was extracted and transformed to create a category DataFrame with columns for "category_id" and "category." The "category_id" column contained sequential entries from "cat1" to "catn," representing the unique categories, and the "category" column contained the corresponding category titles. 
### Category DataFrame

![Screenshot 2023-05-25 at 8 07 22 PM](https://github.com/estellesantini/Crowdfunding_ETL/assets/47437697/f1b6c09a-4fc2-4d69-baf2-4ce1a7453720)

### Subcategory DataFrame
A similar process was followed to create a subcategory DataFrame with columns for "subcategory_id" and "subcategory." The "subcategory_id" column had entries from "subcat1" to "subcatn," representing unique subcategories, and the "subcategory" column contained the corresponding subcategory titles. Both the category and subcategory DataFrames were exported as CSV files.

![Screenshot 2023-05-26 at 11 02 09 AM](https://github.com/estellesantini/Crowdfunding_ETL/assets/47437697/ee46ca91-89f6-4a86-9c03-289f1f3e70d4)

## Subsection 2: Campaign DataFrame
Next, the Campaign DataFrame was created. The crowdfunding.xlsx Excel data was extracted and transformed to create a campaign DataFrame with several columns including "cf_id," "contact_id," "company_name," "description," "goal," "pledged," "outcome," "backers_count," "country," "currency," "launch_date," "end_date," "category_id," and "subcategory_id." The data types of certain columns were converted, and the "blurb" column was renamed to "description." The "launch_date" and "end_date" columns were converted to datetime format. The "category_id" and "subcategory_id" columns were matched with the unique identification numbers from the category and subcategory DataFrames. The campaign DataFrame was exported as a CSV file and saved to the GitHub repository.

![Screenshot 2023-05-26 at 11 02 57 AM](https://github.com/estellesantini/Crowdfunding_ETL/assets/47437697/e8b248f3-4967-4535-a86a-c482d743d1c5)

![Screenshot 2023-05-26 at 11 04 22 AM](https://github.com/estellesantini/Crowdfunding_ETL/assets/47437697/3c2efa71-c375-41ce-b8af-ef9033b1a3ea)

## Subsection 3: Contacts DataFrame
In this subsection, the Contacts DataFrame was created. There were two options provided for extracting and transforming the data from the contacts.xlsx Excel file. Option 1 involved using Python dictionary methods, while Option 2 utilized regular expressions. The chosen option was implemented to import the contacts.xlsx file into a DataFrame and convert each row into a dictionary. The dictionary values were extracted and added to a new list. A new DataFrame was created using the extracted data, and the "name" column was split into separate columns for first and last names. The resulting Contacts DataFrame was cleaned and exported as a CSV file, which was saved to the GitHub repository.

![Screenshot 2023-05-25 at 8 13 00 PM](https://github.com/estellesantini/Crowdfunding_ETL/assets/47437697/fd54c824-a1d4-43d1-9470-f8be5bfd134a)

## Subsection 4: Crowdfunding Database
The final subsection focused on creating the Crowdfunding Database. The CSV files and the ERD (Entity-Relationship Diagram) were inspected. The table schema for each CSV file was sketched based on the ERD using QuickDBD. The database schema, specifying data types, primary keys, foreign keys, and other constraints, was saved as a PostgreSQL file named crowdfunding_db_schema.sql and stored in the GitHub repository. A new PostgreSQL database named "crowdfunding_db" was created, and the tables were created in the order according to the database schema foreign key relationships. The table creation was verified by running SELECT statements for each table. Finally, the CSV files were imported into their corresponding SQL tables, and SELECT statements were used to ensure the correct data was present in each table.

<img width="758" alt="Screenshot 2023-05-25 at 8 14 39 PM" src="https://github.com/estellesantini/Crowdfunding_ETL/assets/47437697/2f6e2038-5474-4a91-a8e0-7a368a379039">

## Conclusion:
Overall, the project successfully completed the extraction, transformation, and loading of data from Excel files into a PostgreSQL database utilizing appropriate data structures and tools.
