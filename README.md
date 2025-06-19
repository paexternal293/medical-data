## Overview

This repository provides a single, denormalized table for storing comprehensive patient medical information in a flat format. It includes fields for patient identifiers, personal details, medical conditions, symptoms, diagnosed diseases, contact information, and address data. This simple structure is ideal for small-scale deployments, rapid prototyping, or data analysis tasks where a single-table approach suffices.

## Table Structure

| Column Name         | Description                                                |
| ------------------- | ---------------------------------------------------------- |
| `PatientID`         | Unique identifier for each patient (e.g., `P001`).         |
| `PatientName`       | Full name of the patient (e.g., `John Doe`).               |
| `MedicalCondition`  | Primary medical condition or focus (e.g., `Hypertension`). |
| `Symptoms`          | Semicolon-separated list of reported symptoms.             |
| `DiagnosedDiseases` | Formal disease diagnoses (can include ICD-10 code).        |
| `Address`           | Full mailing address (street, city, country).              |
| `PhoneNumber`       | Contact phone number (with country code).                  |

## Getting Started

### Prerequisites

* Python 3.6+ (for any data manipulation scripts)
* A relational database (MySQL, PostgreSQL, SQLite) if loading into SQL
* CSV reader (e.g., Excel, pandas) for direct analysis

### Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/your-org/medical-info-db.git
   cd medical-info-db
   ```

2. Review the data file:

   * `data/patients.csv` contains the flat table with example rows.

3. (Optional) Load into a database:

   ```sql
   -- Example for SQLite
   .mode csv
   .import data/patients.csv Patients
   ```

## Usage

* **Analysis:** Use pandas or your preferred tool to read `data/patients.csv`:

  ```python
  import pandas as pd
  df = pd.read_csv('data/patients.csv')
  ```

* **Database querying:** Run standard SQL queries against the `Patients` table.

## Example Data

A snippet of the CSV:

| PatientID | PatientName | MedicalCondition | Symptoms                     | DiagnosedDiseases        | Address                            | PhoneNumber     |
| --------- | ----------- | ---------------- | ---------------------------- | ------------------------ | ---------------------------------- | --------------- |
| P001      | John Doe    | Hypertension     | Headache; Dizziness; Fatigue | Essential hypertension   | 123 Elm St., Addis Ababa, Ethiopia | +251 911 123456 |
| P002      | Jane Smith  | Type 2 Diabetes  | Polyuria; Excessive thirst   | Type 2 diabetes mellitus | 456 Oak Rd., Addis Ababa, Ethiopia | +251 911 654321 |

## Contributing

Contributions are welcome! Please submit issues or pull requests for:

* Additional sample data rows
* Scripts for data validation or import
* Enhancements to documentation

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Contact

For questions or support, please open an issue or contact the maintainer at `maintainer@example.com`. 🎉
# medical-data
