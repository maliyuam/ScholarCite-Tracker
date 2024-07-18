
# ScholarCite Tracker

## Overview

**ScholarCite Tracker** is a Python tool designed to fetch and analyze the top 20 most cited scholarly articles from Google Scholar based on a user-specified query. It focuses on papers published in the last five years, sorting them by the number of citations. The results are stored in an Excel file, making it easy to access and analyze the data.


## Installation

### Prerequisites

Ensure you have Python 3.6 or newer installed on your system. The following Python libraries are required:

- `requests`
- `beautifulsoup4`
- `pandas`
- `openpyxl`

### Installing Dependencies

To install the required libraries, run the following command in your terminal:

```bash
!pip install -q requests 
!pip install -q beautifulsoup4
!pip install -q pandas
!pip install openpyxl
```

## Usage

### Fetching and Saving Data

Run the following command to fetch data:

```python
query = "machine learning"
result_df = get_top_cited_papers(query)
print(result_df)
```

This function will save the top 20 most cited papers into an Excel file named 'top_cited_papers.xlsx'.

### Reading Data from Excel

To read back the data from the Excel file, use:

```python
papers_from_excel = read_papers_from_excel('top_cited_papers.xlsx')
print(papers_from_excel)
```

## Functions

### `get_top_cited_papers(query)`

- **Parameters**:
  - `query`: A string representing the search term used to query Google Scholar.
- **Returns**: A pandas DataFrame containing the top 20 cited papers, sorted by citation count.
- **Description**: Fetches, sorts, and saves scholarly papers based on the query.

### `read_papers_from_excel(filepath)`

- **Parameters**:
  - `filepath`: Path to the Excel file containing the top cited papers.
- **Returns**: A pandas DataFrame of the papers.
- **Description**: Reads the Excel file and returns the data.

### Maintaining the Script

- Regular updates to the parsing logic may be necessary to accommodate changes in the Google Scholar website structure.
- Keep all dependencies updated and monitor for security patches.
