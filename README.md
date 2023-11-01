# NCUA_5300
R script that combines as many separate 5300 Call Report files into one master file set and GeoCodes data.

# GitHub README for NCUA 5300 Call Report Data Integration

This repository contains a script designed to process multiple separate files of NCUA 5300 Call Report data and combine them into one master file. The primary functionality of the script includes dynamically handling changes in the structure of the input files and making the column names more user-friendly.

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [Step-by-Step Guide](#step-by-step-guide)
  - [Step 1: Set the Working Directory](#step-1-set-the-working-directory)
  - [Step 2: Combine Data Files](#step-2-combine-data-files)
  - [Step 3: Remove Duplicate Rows](#step-3-remove-duplicate-rows)
  - [Step 4: Write Combined Files](#step-4-write-combined-files)
  - [Step 5: Rename Columns](#step-5-rename-columns)
  - [Step 6: Move Files Back (Optional)](#step-6-move-files-back-optional)
- [License](#license)

## Introduction

The NCUA 5300 Call Report is a critical financial reporting tool for credit unions in the United States. It provides valuable data on a credit union's financial performance. This script is specifically designed to combine multiple NCUA 5300 Call Report data files, which may have varying structures, into a single master file for analysis.

## Prerequisites

Before using this script, you need to ensure you have the following prerequisites:

- R programming environment installed on your system.
- A directory containing the NCUA 5300 Call Report data files you want to process.
- A separate script for geocoding branch and ATM data (not included in this repository).

## Usage

To utilize this script, follow the step-by-step guide provided below.

## Step-by-Step Guide

### Step 1: Set the Working Directory

1. Set the working directory to the location where the NCUA 5300 Call Report data files are located. You can do this by uncommenting and modifying the following line in the script:

   ```R
   setwd("/path/to/root/directory")
   ```

   Replace `/path/to/root/directory` with the actual path to your data files.

### Step 2: Combine Data Files

1. This step loops through each unique filename in the directory and combines the data files with the same name.
2. It identifies the file with the most columns and adds data from other files with fewer columns to it.
   
### Step 3: Remove Duplicate Rows

1. After combining the data, duplicate rows are removed to ensure the integrity of the dataset.
   
### Step 4: Write Combined Files

1. The combined data is written to a new sub-directory with modified names.

### Step 5: Rename Columns

1. Set the working directory to the location where the combined data files are located by uncommenting and modifying the following line in the script:

   ```R
   setwd("/path/to/directory/with/combined/data/files")
   ```

   Replace `/path/to/directory/with/combined/data/files` with the actual path.

2. The script renames columns based on an "AcctDesc.csv" file, which provides user-friendly column names.

### Step 6: Move Files Back (Optional)

1. If needed, you can uncomment and modify this step to move the modified files back to the original directory.

## License

This script is released under the [MIT License](LICENSE), which means you are free to use and modify it as you see fit.
