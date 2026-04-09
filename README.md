openalex-bibliometric-reports

A reproducible Python workflow for generating bibliometric research reports from OpenAlex data.

This project harvests scholarly metadata from the OpenAlex API and transforms it into concise, visually oriented research reports that support library outreach, research visibility analysis, and local assessment. The workflow is discipline-agnostic and can be adapted for departments, schools, or entire institutions.

Overview

Given a vetted list of researchers and their OpenAlex author identifiers, this workflow:

Collects author- and work-level metadata from OpenAlex
Builds structured datasets for analysis
Generates bibliometric tables and visualizations
Produces department-level HTML reports
Exports print-ready PDF reports
Report Contents

Each report typically includes:

Publication outlet frequencies
Most-cited referenced journals or sources
Open access summary
Funding distribution
Keyword frequency analysis (word cloud)
Co-authorship network visualization
Collaboration summary tables
Workflow Summary
Compile a researcher roster
Match researchers to OpenAlex author IDs
Query the OpenAlex API
Build publication datasets
De-duplicate records for unit-level reporting
Generate bibliometric indicators
Render HTML reports
Export PDF reports
Repository Structure

openalex-bibliometric-reports/
├── data/
├── imgs/
├── html/
├── templates/
├── *.ipynb
├── .env
└── README.md

Requirements
Python 3.12+
pandas
requests
matplotlib
networkx
numpy
wordcloud
jinja2
weasyprint
python-dotenv
Installation

conda create -n openalex-reports python=3.12
conda activate openalex-reports
pip install pandas requests matplotlib networkx numpy wordcloud jinja2 weasyprint python-dotenv

OpenAlex API Setup

Create a .env file in the project root:

OPENALEX_API_KEY=your_api_key_here

Running the Workflow
Add your author_ids.csv file to the data/ directory
Open the Jupyter notebook
Update configuration variables (department, year range, etc.)
Run all cells
Review outputs in data/, imgs/, html/, and exported PDFs
Important Notes
Author matching is critical — validate OpenAlex IDs carefully
De-duplication is required for accurate unit-level metrics
API calls may be time-intensive for large datasets
This is a framework, not a turnkey application — local adaptation is expected
Use Cases
Library outreach and liaison engagement
Departmental research overviews
Bibliometric exploration and analysis
Research visibility reporting
Institutional assessment pilots
License

MIT License
