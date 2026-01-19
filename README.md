# ADA Score Elections Dataset

This repository downloads and processes ADA (Americans for Democratic Action) Score data from PDF files and creates a structured dataset for analysis.

## Overview

- `Downloading_PDFs.ipynb` - Downloads ADA Score PDF files from the official website
- `ADA_Score_new.ipynb` - Extracts data from PDFs and creates a CSV dataset
- `downloaded_pdfs/` - Directory containing the downloaded PDF files

## Setup

1. Install required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### Step 1: Download PDF Files

Run the `Downloading_PDFs.ipynb` notebook to download ADA Score PDFs:
- Downloads PDFs for years 2010-2022
- Skips already downloaded files
- Shows download progress and summary

### Step 2: Extract Data

Run the `ADA_Score_new.ipynb` notebook to extract and process the data:
- Reads all PDF files from `downloaded_pdfs/` directory
- Extracts legislator names, states, seats, and ADA scores
- Combines data from all years into a single DataFrame
- Exports to CSV file

## Output

The final dataset includes:
- **Seat**: Congressional seat number
- **State**: US State name
- **Name**: Legislator name
- **LQ Score**: ADA Liberal Quotient score (0-100)
- **Year**: Year of the score

## Requirements

- Python 3.7+
- requests
- pdfplumber
- pandas
- jupyter

See `requirements.txt` for specific versions.
