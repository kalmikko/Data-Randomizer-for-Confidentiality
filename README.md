# Randomize Data for Confidentiality

## Overview
This script randomizes numerical and boolean values in a dataset while preserving the original data structure and format. It supports CSV, XLSX, and JSON file formats, ensuring that the randomized output file retains the same format as the input file. The primary motivation for this script is to modify the data for confidentiality reasons.

## Features
- **Data Randomization**: Randomizes integer, float, and boolean data types while keeping strings and unsupported types unchanged.
- **File Format Preservation**: Maintains the original file format and structure, including the layout of Excel sheets, CSV columns, and JSON records.

## Usage
1. Place the script in a directory with the data file to be processed.
2. Specify the path to the input data file in the `input_file` variable.
3. Run the script to generate a randomized data file with a prefix `randomized_` added to the original file name.

Example usage:
```python
input_file = "/path/to/your/data_file.xlsx"  # Replace with your file path
randomize_data(input_file)

