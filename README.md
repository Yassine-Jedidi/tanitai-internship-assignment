# Academic Paper Analysis with BERT

A machine learning project for processing and analyzing academic papers in the medical/fertility domain using BERT-based models.

## Project Overview

This project implements a natural language processing pipeline to:

- Extract and process metadata from academic papers
- Analyze paper content using BERT models
- Generate structured insights from medical research papers

## Prerequisites

- Python 3.8 or higher
- CUDA-capable GPU (recommended for faster training)
- 8GB RAM minimum (16GB recommended)

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd <project-directory>
```

2. Create and activate a virtual environment:

```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# Linux/Mac
python -m venv venv
source venv/bin/activate
```

3. Install required packages:

```bash
pip install -r requirements.txt
```

## Project Structure

```
.
├── assignementdataset/     # Dataset directory containing JSON files
├── Tanit IA - Technical Test.ipynb # Jupyter notebooks for analysis
├── requirements.txt       # Project dependencies
└── README.md             # This file
```

## Setting Up the Dataset

1. Ensure all JSON files are placed in the `assignementdataset` directory
2. Files should be in the GROBID TEI format
3. Each file should contain paper metadata including:
   - Title
   - Abstract
   - Author information
   - Keywords

## Running the Analysis

1. Start Jupyter Notebook:

```bash
jupyter notebook
```

2. Open `Tanit IA - Technical Test.ipynb`

3. Run the cells in sequence to:
   - Process the JSON files
   - Extract paper metadata
   - Train and evaluate the BERT model

## Dependencies

Main libraries used:

- tensorflow>=2.0.0
- transformers
- pandas
- numpy
- scikit-learn
- jupyter

For a complete list of dependencies, see `requirements.txt`.

## Model Training

The project uses a BERT-based model with the following configuration:

- Base model: TFBertForSequenceClassification
- Optimizer: Adam
- Loss function: SparseCategoricalCrossentropy
- Early stopping and learning rate reduction implemented

## Output

The pipeline generates:

- Processed CSV file containing structured paper data
- Trained BERT model for paper analysis
- Performance metrics and evaluation results

## Troubleshooting

Common issues and solutions:

1. **CUDA/GPU Issues**:

   - Ensure CUDA toolkit is properly installed
   - Check TensorFlow GPU compatibility
   - Verify GPU drivers are up to date

2. **Memory Issues**:

   - Reduce batch size in model training
   - Process smaller chunks of data
   - Close other memory-intensive applications

3. **Encoding Errors**:
   - Ensure files are in UTF-8 format
   - Check for special characters in file names
   - Verify JSON file formatting

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request
