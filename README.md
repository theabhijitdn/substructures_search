# Cheminformatics Substructure Analysis

This project provides tools for loading molecular data from various file formats, performing substructure searches, and analyzing chemical structures using RDKit. The project is designed to be flexible, allowing users to input molecular data from SDF, SMILES, or CSV files and perform substructure analysis using a customizable set of SMARTS patterns.

## Features

- Load molecular data from SDF, SMILES, or CSV files.
- Perform substructure searches using a predefined set of SMARTS patterns.
- Export substructure patterns to a CSV file for easy sharing and modification.
- Analyze and visualize common substructures in a dataset.

## Setup

### Prerequisites

- Python 3.x
- RDKit
- Pandas


## Usage

1. **Load Molecules:**

   Use the `load_molecules` function to load molecules from a specified file. Supported formats include `.sdf`, `.smi`, and `.csv`.

python
from your_module import load_molecules

file_name = 'molecules.csv'  # Replace with your file path
molecules = load_molecules(file_name)


2. **Substructure Analysis:**

   Load substructure patterns from `substructures.csv` and perform analysis.

python
import pandas as pd

substruct_df = pd.read_csv('substructures.csv')
substructure_smarts = dict(zip(substruct_df['Name of Substructure'], substruct_df['SMILES']))

for name, smarts in substructure_smarts.items():
print(f"{name}: {smarts}")


3. **Export Substructures:**

   Export the substructure patterns to a CSV file for easy modification.

python
substruct_df.to_csv('substructures.csv', index=False)


## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an Issue for any bugs or feature requests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [RDKit](https://www.rdkit.org/) for providing a comprehensive cheminformatics toolkit.
- [Pandas](https://pandas.pydata.org/) for data manipulation and analysis.
