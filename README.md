# Structural-Profiles-in-Powerlifting-a-Statistical Analysis
A statistical analysis of IPF powerlifting data using K-Means clustering to identify distinct athlete profiles based on their lift percentages.

This project performs a statistical analysis on the official OpenPowerlifting dataset to identify distinct structural profiles among competitive powerlifters within the International Powerlifting Federation (IPF).

The core of the analysis uses **K-Means Clustering** to group athletes based on the percentage contribution of their squat, bench press, and deadlift to their total weight lifted. The goal is to move beyond absolute strength and understand the different "archetypes" of lifters that exist in the sport.

The final, compiled report can be viewed by opening the PDF file: [**Structural_Profiles_in_Powerlifting.pdf**](Structural_Profiles_in_Powerlifting.pdf).

------------------------------------------------------------------------

## Key Findings

The analysis revealed several key insights:

1.  **Three Distinct Athlete Profiles Exist:** The algorithm successfully identified three well-defined clusters:

    -   **Sq (Squatters):** Athletes whose squat is the dominant lift percentage-wise.
    -   **Bp (Benchers):** Athletes specializing in the bench press.
    -   **Dl (Deadlifters):** Athletes with a proportionally superior deadlift.

2.  **Geographical Specialization:** There is a statistically significant association between an athlete's profile and their nation. For example, Latin American countries showed a higher prevalence of "Deadlifters," while Central and Northern European nations had a stronger association with "Benchers."

3.  **The "Bencher" Performance Anomaly:** The "Benchers" cluster initially showed the highest average performance (GL Points). However, this was found to be almost entirely explained by a **strong gender gap**, as the cluster is composed of over 90% male athletes.

4.  **Performance After Controlling for Gender:** When analyzing the sexes separately, the performance gap between clusters narrows significantly. The "Deadlifter" profile consistently shows the lowest average performance for both males and females, while "Squatters" and "Benchers" become roughly equivalent.

------------------------------------------------------------------------

## Key Visualization: Athlete Distribution in Ternary Space

This ternary plot visualizes the three clusters. Each point is an athlete, positioned based on their lifting percentages. The three distinct "islands" of density clearly show the separation between the structural profiles.

[Ternary Plot of Athlete Clusters](Ternary%20Plot.png)

------------------------------------------------------------------------

## Methodology and Tools

-   **Language:** R
-   **Key Packages:** `dplyr`, `ggplot2`, `data.table`, `cluster`, `factoextra`, `ggtern`, `FactoMineR`.
-   **Statistical Techniques:** Data Cleaning & Preprocessing, K-Means Clustering, Elbow Method for K selection, Correspondence Analysis, ANOVA.

------------------------------------------------------------------------

## Repository Contents

-   `RMD_eng.Rmd`: The complete R Markdown source file containing all the code, commentary, and analysis.
-   `Structural_Profiles_in_Powerlifting.pdf`: The final, compiled PDF report of the analysis.
-   `README.md`: This file, providing an overview of the project.

------------------------------------------------------------------------

## How to Reproduce the Analysis

1.  **Data:** This analysis uses a snapshot of the official `openipf` dataset from OpenPowerlifting, updated to October 25, 2025. The original, live dataset is maintained by the OpenPowerlifting project.
2.  **Environment:** You will need R and RStudio, along with the packages listed under the "Methodology and Tools" section.
3.  **Run the Code:** Open the `RMD_eng.Rmd` file in RStudio and click the "Knit" button to reproduce the PDF report from scratch. All data preprocessing steps are included in the script.

------------------------------------------------------------------------

## Data Source and Acknowledgements

This analysis would not have been possible without the incredible work of the **OpenPowerlifting project**. The data is provided by them and is the foundation of this entire study.

A huge thank you to their team for maintaining such a vital resource for the powerlifting and data science communities.

For the most up-to-date data, please visit the official [OpenPowerlifting website](https://www.openpowerlifting.org/).
