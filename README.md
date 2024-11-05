# Sri Lanka Cricket Data Analysis

This project focuses on extracting, transforming, and visualizing cricket data related to Sri Lanka. The final dataset will be visualized in Tableau to provide insights into Sri Lankan cricket performance, including player stats, match outcomes, and detailed ball-by-ball analysis.

This project aims to analyze Sri Lankan cricket data by downloading, processing, and visualizing the data using AWS services. 

## Project Overview

This project collects and processes cricket data specifically related to Sri Lanka. Data is downloaded as JSON files and transformed into a CSV format for analysis and visualization. The AWS Lambda service is used to automate the data collection and storage in S3.

## Data Collection

### Data Sources
- **Cricsheet**: [Cricsheet Downloads](https://cricsheet.org/downloads/)
- **Direct Link**: [Sri Lanka Male JSON ZIP](https://cricsheet.org/downloads/sri_lanka_male_json.zip)

### AWS Resources
- **S3 Bucket**: Created an S3 bucket named `sl-cricket-data` to store downloaded files and processed data.

### Data Download Process
The data download process is automated with an AWS Lambda function:
- **Lambda Function**: A function downloads the ZIP file from the Cricsheet link and uploads it to the `sl-cricket-data` S3 bucket.
- **Dependencies**: The `requests` package is used in the Lambda function to handle the HTTP download from the URL. A Lambda Layer with the `requests` library is included in the function to manage dependencies.

### Folder Structure