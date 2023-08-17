# Data Analysis for Mingar

This repository contains the code and documentation for a data analysis project conducted by CJYB Consulting Group Inc. for Mingar. The analysis focuses on two main questions: 

1. Who are the new customers that use the ‘Active’ and ‘Advanced’ products and how do they compare to traditional users in terms of median income?
2. Is there a correlation between skin tone and the number of flags during sleep sessions on Mingar's devices?

## Project Overview

Students acting as a consulting group received data as well as web scraping, accessing an API and retrieving licensed data, and then used these to merge, wrangle, visualize, summarize and model data on fitness tracker customers to meet a client brief, and reported on their methods and findings appropriately for a general executive audience and, separately, for a technical audience. 

The analysis is carried out in R and involves various data wrangling, visualization, and statistical modeling techniques. The project includes the following main components:

- Data collection: The data was collected from various sources, including customer data and sleep log data.
- Data wrangling: The collected data was cleaned, transformed, and combined to create suitable datasets for analysis.
- Exploratory data analysis: Various data visualizations were created to explore the relationships between different variables.
- Statistical modeling: Linear regression and generalized linear mixed models were used to answer the research questions.

## Course Information

This data analysis project serves as the final project for STA303 at the University of Toronto. As part of this course, our consulting group was tasked with conducting a comprehensive analysis of fitness tracker customer data. The project involved data collection, web scraping, API integration, and licensed data retrieval to meet the specific requirements of a client brief.

For detailed project requirements and guidelines, please refer to the [STA303 Final Project Description](https://sta303-bolton.github.io/sta303-w22-final-project/). This resource provides insight into the scope, objectives, and expectations of the project.

The collaborative effort within our consulting group showcases our ability to apply advanced analytical techniques and communicate findings effectively to diverse audiences, while delivering practical and data-driven recommendations.

We are grateful for the opportunity to undertake this project as part of our academic journey, and we look forward to sharing the insights and skills we have gained through this experience.

## Project Structure

The project directory is structured as follows:

- `data-raw/`: Contains the raw data provided by the client, as well as the licensed data for postcode conversion, census data, and web scraping results (not to be made publicly available).
- `code/`: Contains R scripts used for data wrangling, analysis, and visualization.
- `reports/`: Contains the final report in PDF format summarizing the analysis findings.
- `README.md`: The file you are currently reading, providing an overview of the project.

## Gitignore

The repository includes a `.gitignore` file that specifies which files and directories should be ignored by Git. This helps keep the repository clean and focused. Files and directories such as compiled code, temporary files, user-specific settings, and generated output are excluded from version control. For a complete list of ignored files and directories, please refer to the `.gitignore` file in the root directory.

## Folder and File Structure

### Folders

- `data-raw/`: Contains the raw data provided by the client, as well as the licensed data for postcode conversion, census data, and web scraping results (not to be made publicly available).

### Files

- `README.md`: This file you're reading! It provides an overview of the project's contents and setup.
- `data-prep.Rmd`: Write the code here to create the datasets you'll use in your main report. Read data from `raw-data` and the datasets you plan to use for the report into `data`. All other modeling, summaries, etc., should be done in the main Rmd.
- `sta303-final-project.Rmd`: Update this file to create your final report. It should only use data from the `data/` folder.
- `report.tex`: LaTeX template for the final report (no need to edit).

### Note on File Paths

All file paths should be relative to `sta303-final-project.Rmd` and in the form `raw-data/filename`.

## Guide to Raw Data

The `data-raw/` folder contains the following files:

- `cust_dev.Rds`: Matches each customer to their current device.
- `customer.Rds`: General information about each customer for use in the app and associated profile and chat features.
- `device.Rds`: Additional information about each device.
- `cust_sleep.Rds`: Sleep data for each customer.

## Guide to Data

### Table 1: Guide to client provided data

| Dataset      | Variables                  | Description                                          |
|--------------|----------------------------|------------------------------------------------------|
| cust_dev.Rds | cust_id, dev_id            | Matches each customer to their current device.      |
| customer.Rds | cust_id, dob, postcode, sex, pronouns, emoji_modifier | General information about each customer for use in the app and associated profile and chat features. |
| device.Rds   | dev_id, device_name, line, released | Additional information about each device in these data. May be useful for connecting with the industry dataset. |
| cust_sleep.Rds | cust_id, date, duration, flags | Sleep data for each customer.                        |

### Table 2: Client data variables

| Variable       | Description                                               |
|----------------|-----------------------------------------------------------|
| cust_id        | Unique ID for each customer.                             |
| dob            | Date of birth, as entered by the customer. Year, month, day format. |
| postcode       | Postal code of customer.                                 |
| sex            | Biological sex, used for calculations of health metrics, like body-mass index and base metabolic rate. |
| pronouns       | Pronouns for social profile.                            |
| emoji_modifier | Code for skin tone modifier for emojis when using the chat and react features of the social component of our app. These are the standard unicode modifiers, based on the Fitzpatrick scale. If not set, this means the default yellow colour used. |
| dev_id         | Unique ID for each device registered with our app.    |
| device_name    | Name of device type.                                    |
| line           | Line of products this device belongs to.               |
| released       | Release date for this particular device type. Year, month, day format. |
| date           | For sleep data, date sleep session started. Year, month, day format. |
| duration       | Duration, in minutes, of sleep session.                |
| flags          | Number of times there was a quality flag during the sleep session. Flags may occur due to missing data, or due to data being recorded but sufficiently unusual to suggest it may be a sensor error or other data quality issue. |

## License

This project is licensed under the [MIT License](LICENSE).

For any questions or feedback about this project, please feel free to contact us:

- Chun Ki Yip: [jackyyipchunki@gmail.com](mailto:jackyyipchunki@gmail.com)


We appreciate your interest in our project and hope you find the analysis informative and useful!
