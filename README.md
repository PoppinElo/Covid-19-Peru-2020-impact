# COVID-19 Impact Analysis in Peru

- Name: Kevin Juan Román Rafaele
- LinkedIn: https://www.linkedin.com/in/kevin-juan-r-997530117/
- Email: mrredsky.2095@gmail.com
- GitHub: https://github.com/PoppinElo
- License: MIT License

## Motivation
The COVID-19 pandemic has had a profound impact globally, and understanding its effects at a regional level can help improve public health responses. This project aims to analyze the relationship between healthcare infrastructure (specifically health centers and posts) and the number of COVID-19 positive cases and deaths in Peru during 2020.

## Hypothesis
Our initial hypothesis is that regions with more health centers and health posts would have lower numbers of COVID-19 positive cases and deaths due to better healthcare accessibility.

## Data
We used three datasets for this analysis, all sourced from the [Kaggle Peru Covid-19 dataset](https://www.kaggle.com/datasets/martinclark/peru-covid19-august-2020), [Open Data National Platform from Peru](https://www.datosabiertos.gob.pe/) and from the [INEI platform](https://m.inei.gob.pe/estadisticas/indice-tematico/health-sector-establishments/)
1. **Health Centers and Posts**: Contains the number of health centers (`NUM_CENTROS_SALUD`) and health posts (`NUM_PUESTOS_SALUD`) per department.
2. **Positive Cases**: Contains the total number of positive COVID-19 cases (`total_positive_cases`) per department.
3. **Deceased Cases**: Contains the total number of deceased COVID-19 cases (`total_deceased_cases`) per department.

### Data Curation
The datasets were curated manually before being loaded into the analysis notebook. This include reformating the tables and removing headers from the original files.

## Analysis
The analysis was conducted in two parts:
1. **Including all departments**.
2. **Excluding the 'LIMA' department** to see if the results differ significantly.

### Data Cleaning
We standardized the `DEPARTAMENTO` column by converting all values to uppercase and removing accents to ensure consistency across datasets. This enabled us to merge the datasets accurately.

### Correlation Analysis
We calculated the correlation matrix to understand the relationships between the variables.

### Scatter Plots
We generated scatter plots to visualize the relationships between:
1. Number of Health Centers and Positive Cases.
2. Number of Health Posts and Positive Cases.
3. Number of Health Centers and Deceased Cases.
4. Number of Health Posts and Deceased Cases.

## Results

### Correlation Matrix (Excluding LIMA)

![Correlation Matrix](results/correlation_matrix.png)

### Scatter Plots

**Health Centers vs Positive Cases**:
![Health Centers vs Positive Cases](results/scatter_health_centers_positive_cases.png)

**Health Posts vs Positive Cases**:
![Health Posts vs Positive Cases](results/scatter_health_posts_positive_cases.png)

**Health Centers vs Deceased Cases**:
![Health Centers vs Deceased Cases](results/scatter_health_centers_deceased_cases.png)

## Interpretation

The analysis shows weak correlations between the number of health centers/posts and the total positive and deceased cases. This suggests that other factors, such as population density, healthcare quality, and public health policies, might play more significant roles.

### With LIMA Department

Weak but notable correlations are observed. The strong correlation between positive and deceased cases are notable. The Lima department relations can be identified as a outlier.

### Without LIMA Department

Excluding the 'LIMA' department change for a little the weak correlations observed. The strong correlation between positive and deceased cases persisted.

## Suggestions

- **Further Analysis**: Incorporate additional variables such as population density, socio-economic factors, and healthcare quality indices.
- **Geospatial Analysis**: Visualize the data geographically to identify regional patterns.
- **Time Series Analysis**: Study the temporal trends to understand the evolution of the pandemic and the impact of healthcare infrastructure over time.

## Conclusion

This analysis provides initial insights into the relationship between healthcare infrastructure and COVID-19 impact in Peru. While the number of health centers and posts alone do not strongly correlate with the number of positive and deceased cases, a more comprehensive analysis incorporating additional factors is needed to draw more definitive conclusions.

## How to Run the Analysis

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/Covid-19-Peru-2020-impact.git
    cd Covid-19-Peru-2020-impact
    ```

2. **Run the notebook**:
   ```
    jupyter covid-peru-impact.ipynb
   ```

