<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Visualize data with QuickSight

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-analytics-quicksight)

**Author:** Kindson Nathan  
**Email:** kindsonegbule15@gmail.com

---

![Image](http://learn.nextwork.org/restful_orange_loyal_cumin/uploads/aws-analytics-quicksight_6c7f7ef0)

---

## Introducing Today's Project!

In this project, I will demonstrate how to use Amazon QuickSight to visualize data by connecting a dataset, creating interactive dashboards, and generating insights from the information.

I’m doing this project to learn how to analyze and present data effectively using AWS tools, understand how QuickSight integrates with other AWS services like S3 and Athena, and gain hands-on experience in building data visualizations that support decision-making.

### Tools and concepts

The services I used were Amazon S3, and Amazon QuickSight. S3 for data storage and QuickSight for creating interactive visualizations and dashboards.

Key concepts I learned include how to connect datasets from S3 to QuickSight, apply filters and parameters, and how to design and publish dashboards for sharing and reporting.

### Project reflection

This project took me approximately two hours to complete. The most challenging part was connecting my dataset and ensuring that all visuals updated correctly after each refresh. However, it was most rewarding to see the final interactive dashboard come together.

After this project, I plan to work on the 7 days dev0ps challenge. I will start this project on 27th October 2025.

---

## Upload project files into S3

S3 is used in this project to store two files, which are the CSV dataset file and the manifest.json file. The CSV file contains the actual data that will be analyzed and visualized in Amazon QuickSight, while the manifest.json file provides metadata and location details that tell QuickSight how to locate and interpret the CSV file within the S3 bucket.

I edited the manifest.json file by updating the file path (URI) to point to the exact location of my CSV dataset in the S3 bucket and ensuring that the format and structure matched QuickSight’s requirements.

It’s important to edit this file because QuickSight relies on the manifest.json to locate, read, and correctly interpret the dataset. Without the correct file path or structure, QuickSight would not be able to connect to the data source or import the data properly for visualization.

![Image](http://learn.nextwork.org/restful_orange_loyal_cumin/uploads/aws-analytics-quicksight_3c3cd85a)

---

## Create QuickSight account

Creating a QuickSight account costs nothing initially, as Amazon offers a free trial that lets you explore the service with limited usage. After the trial period, pricing depends on the edition you choose:

QuickSight Standard Edition starts at around $9 per user per month.

QuickSight Enterprise Edition starts at about $18 per user per month and includes advanced features like encryption, Active Directory integration, and sharing dashboards at scale.

During the free trial, you can analyze data, create dashboards, and explore most features without being charged.

Creating an account took me 4 minutes. I can do it lesser than that.

![Image](http://learn.nextwork.org/restful_orange_loyal_cumin/uploads/aws-analytics-quicksight_f4ab4214)

---

## Download the Dataset

I connected the S3 bucket to QuickSight by visiting the Amazon QuickSight console, navigating to the Datasets section, and selecting “New Dataset”. Then I chose Amazon S3 as my data source, entered a name for the dataset which is 'kaggle-netflix-data', and provided the S3 manifest.json file path  's3://nextwork-quicksight-project-kindson/manifest.json' (the URI pointing to the file in my S3 bucket). After that, I clicked “Connect” and QuickSight successfully established a connection to my S3 bucket, allowing me to import and prepare my data for visualization.

The manifest.json file was important in this step because it tells Amazon QuickSight exactly where to find the dataset in my S3 bucket and how the data is structured. It defines details such as the file location (S3 URI), format, and delimiters used in the CSV file. Without the manifest.json file, QuickSight wouldn’t know how to properly locate, read, or interpret the dataset, making it a crucial link between S3 storage and QuickSight’s data visualization tools.

![Image](http://learn.nextwork.org/restful_orange_loyal_cumin/uploads/aws-analytics-quicksight_6f874996)

---

## My first visualization

To create visualizations on QuickSight, I opened my dataset in the QuickSight analysis workspace, selected “New Analysis,” and then chose my prepared dataset from S3. From there, I dragged and dropped different fields (such as numerical and categorical data) into the visualization pane. I then selected various chart types like bar charts, pie charts, and line graphs from the visualization menu, and customized them by adjusting filters, colors, and labels. Finally, I combined multiple visuals into a single dashboard to present a clear, interactive summary of my data insights.

The chart/graph shown here is a breakdown of the Netflix titles dataset, showing insights such as the distribution of movies and TV shows by country, release year, genre, or rating. It helps visualize trends in Netflix’s content library, like which countries produce the most titles or how content types have changed over time.

I created this graph by dragging and dropping the relevant dataset fields from the Fields list in Amazon QuickSight onto the visualization pane. For example, I dragged the “release_year” field to the Y-axis and the “type” field to the Group/Color section to show the distribution of Netflix content types (Movies and TV Shows) across different years. This helps visualize how Netflix’s content library has evolved over time, highlighting which years had the most releases and whether Movies or TV Shows dominated in particular periods.

![Image](http://learn.nextwork.org/restful_orange_loyal_cumin/uploads/aws-analytics-quicksight_aff3aad7)

---

## Using filters

Filters are useful for narrowing down large datasets to focus on specific information or patterns. In Amazon QuickSight, they allow you to analyze subsets of data — for example, filtering by country, year, genre, or content type to answer targeted questions. Filters help make visualizations more interactive, precise, and meaningful by letting you control what data is displayed and compare different segments without altering the original dataset.

This visualization is a breakdown of Netflix titles by genre category (listed_in) and type, showing how content is distributed across different genres such as Action & Adventure, TV Comedies, and Thrillers. The charts display the count of shows and movies that fall under each genre, helping to identify which categories dominate the Netflix library.

Here, I added a filter by release year to focus on titles from specific time periods, allowing me to analyze how Netflix’s genre distribution has evolved over the years and which genres were most popular during certain eras.

![Image](http://learn.nextwork.org/restful_orange_loyal_cumin/uploads/aws-analytics-quicksight_c32248c5)

---

## Setting up a dashboard

As a finishing touch, I edited the title of each visualizations and reviewed my entire dashboard to ensure all visualizations were clear, accurate, and well-labeled, making the data story easy to follow. Finally, I shared or exported the completed dashboard to showcase my findings and demonstrate my ability to analyze and visualize data effectively using Amazon QuickSight.

Did you know you could export your dashboard as PDFs too? I did this by going to the Share menu in Amazon QuickSight, selecting Export, and then choosing Export to PDF. This allowed me to download a high-quality version of my dashboard, which I can easily share with others or include in reports and presentations.

![Image](http://learn.nextwork.org/restful_orange_loyal_cumin/uploads/aws-analytics-quicksight_6c7f7ef0)

---

## Refreshing source data

In this project’s extension, I downloaded fresh data that’s different from my original dataset because it allows me to capture more recent and accurate information, ensuring that my analysis reflects current trends and patterns. Using updated data also helps validate whether the insights from the initial dataset still hold true or if there have been significant changes over time.

Analyzing incomplete data brings the risk of drawing misleading or inaccurate conclusions. Missing or outdated information can distort trends, reduce the reliability of visualizations, and lead to poor decision-making based on partial evidence.

Once I downloaded new data, I had to update my S3 bucket because the old dataset no longer reflected the most current information, and I wanted my cloud storage to contain the latest version for accurate analysis and automation. Updating the S3 bucket ensures that any connected services or workflows (like AWS Athena, QuickSight, or data pipelines) reference the most recent data.

I also uploaded a new manifest.json file that defines the structure, location, and format of the updated dataset. This file helps AWS services understand how to read the new data, specifying details such as file paths and data types ensuring seamless integration and accurate querying of the refreshed dataset.

I initially couldn’t see my updated data in QuickSight, so I had to refresh the dataset to ensure it pulled the latest version from my S3 bucket. This involved navigating to the dataset settings in QuickSight and selecting the “Refresh now” or “Edit and save” option to reload the data source. After doing this, the new data appeared in my analysis, allowing me to visualize the most recent information accurately.

![Image](http://learn.nextwork.org/restful_orange_loyal_cumin/uploads/aws-analytics-quicksight_86415f4e3)

---

---
