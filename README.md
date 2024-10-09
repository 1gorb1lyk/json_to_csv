# JSON to CSV Converter using Python

This is a simple yet powerful Python application that allows you to convert JSON files to CSV format. It's a lightweight tool that can be incredibly helpful for data processing and analysis tasks.

## Features
- Converts JSON files to CSV format
- Handles nested JSON structures
- Preserves UTF-8 encoding
- Command-line interface for easy usage

## Installation

1. Clone this repository or download the `json_to_csv.py` file.
2. Ensure you have Python ^3.9 installed on your system.

## Usage
To use the converter, follow these steps:

1. Open a terminal or command prompt.
2. Navigate to the directory containing `json_to_csv.py`.
3. Run the following command:
```
python json_to_csv.py <prefix> <input_json_file> <output_csv_file>
```
Where:

- prefix is the root node of your JSON data (use an empty string if your JSON is an array at the root level)
- <input_json_file> is the path to your input JSON file
- <output_csv_file> is the desired path for the output CSV file

Example:
```
python json_to_csv.py data input.json output.csv
```
## How it works
The script performs the following operations:

1. Read the JSON file
2. Flattens nested JSON structures
3. Extracts all unique keys to form the CSV header
4. Write the data to a CSV file, ensuring all fields are properly quoted

## Limitations
- The script assumes that all objects in the JSON array have a similar structure. Inconsistent structures may lead to missing data in some rows.
- Huge JSON files might require significant memory and processing time.