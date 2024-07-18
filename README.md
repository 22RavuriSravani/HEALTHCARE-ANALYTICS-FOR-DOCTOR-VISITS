# HEALTHCARE-ANALYTICS-FOR-DOCTOR-VISITS
TO ANALYZE HEALTHCARE DATA AND DERIVE MEANINGFUL INSIGHTS

This project involves analyzing healthcare data to gain insights into doctor visits, patient segmentation, and the impact of socioeconomic factors on healthcare utilization.

**Files in this Repository**
1. **HealthCare_Analysis.ipynb**: Jupyter Notebook containing the data analysis and visualizations.
2. **DoctorVisits - DA.csv**: CSV file with the raw data used in the analysis.
3. **HEALTHCARE_ANALYSIS_POWERBI.pptx**: Power BI presentation summarizing the findings and insights.
4. **HealthCare_Analysis.html**: HTML version of the Jupyter Notebook for easy viewing.

**Project Overview**

The main objective of this project is to analyze healthcare data related to doctor visits. 
The analysis focuses on:

1. **Patient Segmentation**: Dividing patients into subgroups based on characteristics such as age, gender, and income.
2. **Impact of Socioeconomic Factors**: Examining how variables like income influence healthcare access and outcomes.
3. **Correlation Analysis**: Understanding relationships between different healthcare metrics and patient demographics.

**Python Script To Convert The Notebook To HTML**
```python
import nbconvert

# Path to your notebook
notebook_path = "/mnt/data/HealthCare_Analysis.ipynb"

# Initialize the notebook converter
html_exporter = nbconvert.HTMLExporter()

# Read the notebook file
with open(notebook_path) as f:
    notebook_content = f.read()

# Convert the notebook to HTML
html_body, _ = html_exporter.from_notebook_node(nbconvert.reads(notebook_content, as_version=4))

# Save the HTML output to a file
html_file_path = notebook_path.replace(".ipynb", ".html")
with open(html_file_path, "w") as f:
    f.write(html_body)
