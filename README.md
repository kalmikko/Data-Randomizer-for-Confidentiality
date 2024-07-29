# Randomize Data for Confidentiality
This script randomizes numerical and boolean values in a dataset while preserving the original data structure and format. It supports CSV, XLSX, and JSON file formats, ensuring that the randomized output file retains the same format as the input file. Can be used on sensitive data you want to perform data analysis on using not locally run AI tools.

## Features
- **Data Randomization**: Randomizes integer, float, and boolean data types while keeping strings and unsupported types unchanged.
- **File Format Preservation**: Maintains the original file format and structure, including the layout of Excel sheets, CSV columns, and JSON records.

## Usage
1. Place the script in a directory with the data file to be processed.
2. Specify the path to the input data file in the `input_file` variable.
3. Run the script to generate a randomized data file with a prefix `randomized_` added to the original file name.
4. Generate a data analysis script using AI tools on the randomized data.
5. Use the generated script on your local computer on the original data, maintaining data confidentiality.

![Image](https://github.com/user-attachments/assets/5d77a998-ee3b-40be-a587-7a5bae013b4a)

## Example Usage (Python)
```
input_file = "/path/to/your/data_file.xlsx"  # Replace with your file path
randomize_data(input_file)
```
## Known Issues
1. Floating Point Inaccuracy:
The randomization of float values may result in excess decimal places due to floating-point precision limits. This can lead to inaccuracies and an unintended increase in the number of decimal places in the output data.

2. Empty Header Names in Excel:
In Excel files, any empty header names are replaced with default placeholders like "Unnamed: x". This behavior is inherent to how Pandas handles Excel data with missing header names.

3. Limited Testing with Different Data Structures:
The script has not been comprehensively tested across all possible data structures and file formats. There may be unforeseen issues when processing complex datasets or unique file configurations.

## Requirements
Python 3.x

Pandas library (pip install pandas)
