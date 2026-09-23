# Credential Breach Detector & Benchmark

A Python-based credential auditing system designed to detect compromised passwords and compare the performance of different search and hashing algorithms.

The project performs a benchmarking experiment using three different approaches:

* **Hash Table — Separate Chaining:** `O(1)` average-case lookup
* **Hash Table — Linear Probing:** `O(1)` average-case lookup
* **Linear Search:** `O(n)` lookup

The system identifies compromised credentials and measures the execution time of each approach, allowing their performance to be compared using the same dataset.

> **Note:** This project does not use any external Python libraries. It relies exclusively on Python's standard library, including the libraries used for the graphical interface.

## Requirements

* Python 3.x

## Example Files

For testing purposes, the repository includes an `archivos_ejemplo` directory containing datasets ready to use with the program.

* `[BD] 100k-most-used-passwords-NCSC.txt` — Dataset containing a large list of compromised passwords.
* `[PWD] Pwdb_top-10000.txt` — Dataset containing passwords to be checked against the compromised-password database.

## How to Run

1. Open a terminal in the project's root directory.

2. Run the main program:

   ```bash
   python main.py
   ```

3. A file selection window will open (**Step 1**). Navigate to the `archivos_ejemplo` directory and select the database file, for example:

   ```text
   [BD] 100k-most-used-passwords-NCSC.txt
   ```

4. A second file selection window will open (**Step 2**). Select the password dataset to be analyzed, for example:

   ```text
   [PWD] Pwdb_top-10000.txt
   ```

5. The system will load the datasets, execute the three search implementations, and display the detected compromised credentials along with their respective execution times.

6. Once the process is complete, the program will automatically generate a `REPORTE_FINAL.txt` file in the project's root directory containing:

   * Detected compromised passwords
   * Execution times for each implementation
   * Performance comparison results

## Academic Context

This project was developed as part of the **Data Structures and Algorithms II** course at **Universidad de Lima**.
The project focuses on applying data structures and algorithm analysis to a practical cybersecurity-related problem, specifically credential auditing and compromised password detection.

