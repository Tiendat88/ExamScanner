Multiple Choice Answer Sheet Grading System
Overview
This Python application automates the grading of multiple-choice answer sheets by processing scanned images. It uses OpenCV for image processing, Tkinter for the GUI, and other libraries to detect marked answers, extract test and student IDs, calculate scores, and save results to a CSV file. The system supports multiple answer keys for different test versions and displays the graded answer sheet with marked answers.
Features

Image Processing: Detects marked bubbles on answer sheets using OpenCV.
Answer Grading: Compares student answers against predefined answer keys (ANSWER_KEY_1 to ANSWER_KEY_4) to compute scores.
ID Extraction: Extracts test ID and student ID from specific regions of the answer sheet.
Result Storage: Saves scores, test IDs, and student IDs to a CSV file (exam_results.csv).
GUI: Provides a Tkinter-based interface to open and process image files.
Visualization: Displays the original and graded answer sheets with marked answers highlighted (correct in green, incorrect in red).

Prerequisites
Ensure you have the following installed:

Python 3.6 or higher
Libraries listed in requirements.txt

Installation

Clone or download the repository.
Install the required dependencies by running:pip install -r requirements.txt


Ensure the script A39948.py is in the project directory.

Usage

Run the script:python A39948.py


A Tkinter window will open with a "Mở ảnh" (Open Image) button.
Click the button to select a scanned answer sheet image (.jpg or .png).
The application will:
Process the image to detect marked answers.
Extract test and student IDs.
Calculate the score based on the appropriate answer key.
Save results to exam_results.csv.
Display the original image and a merged view of graded sections.


Results, including the score, test ID, and student ID, will be shown in the GUI.

File Structure

A39948.py: Main script containing the grading logic and GUI.
exam_results.csv: Output file where results are saved.
requirements.txt: Lists required Python libraries.
README.md: This documentation file.

Answer Sheet Requirements

The answer sheet must be a scanned image (.jpg or .png).
The image should be clear, with marked bubbles filled in darkly.
The answer sheet layout must match the expected format (specific coordinates for answer sections, test ID, and student ID).
The image will be resized to 1830x2560 pixels for processing.

Dependencies
See requirements.txt for the list of required Python libraries.
Notes

The script assumes four answer keys (ANSWER_KEY_1 to ANSWER_KEY_4) for different test versions, each with 30 questions used in the grading process.
The application processes four sections of the answer sheet, each corresponding to a different answer key.
The score is calculated as a percentage of correct answers out of 120 questions, scaled to a 10-point scale.
The test and student IDs are extracted from specific regions, assuming a grid of bubbles representing digits 0-9.

Troubleshooting

Image not processing correctly: Ensure the image is clear and matches the expected layout. Check for proper lighting and contrast.
Dependencies not found: Verify that all libraries in requirements.txt are installed.
CSV file issues: Ensure write permissions for the directory where exam_results.csv is saved.

License
This project is for educational purposes and provided as-is without any warranty.
