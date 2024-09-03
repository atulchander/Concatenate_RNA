# FASTQ File Management and Concatenation Script

This repository contains a Python script designed to manage and process FASTQ files. The script performs two primary tasks:
1. **Removing duplicate FASTQ files**: Identifies and removes duplicate FASTQ files based on their name and size.
2. **Concatenating RNA-seq reads**: Combines RNA-seq reads (R1 and R2) from different lanes into a single file, while maintaining a checkpoint to avoid reprocessing already concatenated files.

## Features

- **Duplicate Removal**: The script checks for duplicate FASTQ files in the specified directory and removes them.
- **File Concatenation**: Groups FASTQ files by sample ID and read direction (R1 or R2) and concatenates them into a single file for each group.
- **Checkpointing**: Keeps track of concatenated files using a checkpoint file to ensure the process can be resumed without redoing work.

## Requirements

- Python 3.x
- Standard Python libraries: `os`, `glob`

## Usage

1. **Set Up Your Folder Path**:
    - Update the `folder_path` variable in the script to the directory where your FASTQ files are located.

    ```python
    folder_path = '/content/drive/MyDrive/Google colab/xyz'
    ```

2. **Run the Script**:
    - Execute the script in your Python environment (e.g., Google Colab or Jupyter Notebook).

3. **Output**:
    - The script will print the status of the processed files, including any duplicates removed and the details of concatenated files.
    - Concatenated files will be saved in a subfolder named `concatenated_files` within your specified directory.
