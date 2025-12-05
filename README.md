# The Best Neighborhood in Pittsburgh (Group 33)
 
**Group Number:** 33  

## 1. Project Overview
This project determines the "Best Neighborhood" in Pittsburgh through a data-driven analysis combining three distinct metrics: **Safety** (arrest data), **Traffic Quietness** (traffic counts), and **Education Opportunity** (student enrollment).

## 2. Team Members & Responsibilities

| Name | Email | Role / Sub-metric | Assigned Notebook |
| :--- | :--- | :--- | :--- |
| **Haoyang Sun** | [has666@pitt.edu](mailto:has666@pitt.edu) | Traffic Quietness & Final Compilation | `Traffic.ipynb` |
| **Jiakai Dai** | [jid147@pitt.edu](mailto:jid147@pitt.edu) | Safety Analysis | `Safety Score.ipynb` |
| **Xiangyu Li** | [xil594@pitt.edu](mailto:xil594@pitt.edu) | Education Analysis | `Education_Metric.ipynb` |

## 3. File Structure
This repository is organized to showcase both individual work and the final group synthesis.

* **Root Directory:**
    * `Combined_Analysis.ipynb`: **The Main Report.** This notebook merges the individual datasets, applies the weighted formula (Safety 50%, Traffic 30%, Education 20%), and visualizes the final ranking.
    * `README.md`: Project documentation.
    * `final_weighted_ranking.csv`: The final output of our combined analysis.

* **Individual Workspaces (Folders):**
    * Each member has a dedicated folder containing their **Individual Notebook** and the **Raw/Processed Data** they used.
    * **Haoyang Sun:** Folder containing `Traffic.ipynb` and traffic count data.
    * **Jiakai Dai:** Folder containing `Safety Score.ipynb` and arrest data.
    * **Xiangyu Li:** Folder containing `Education_Metric.ipynb` and census enrollment data.

## 4. Datasets Used

### 1. Traffic Count Data (City of Pittsburgh)
* **Source:** [WPRDC - Traffic Count Data](https://data.wprdc.org/dataset/traffic-count-data-city-of-pittsburgh)
* **Description:** Data provided by the Department of Mobility and Infrastructure (DOMI) covering daily traffic volume and speeding counts across various Pittsburgh neighborhoods.
* **Analyst:** Haoyang Sun

### 2. Pittsburgh Police Arrest Data
* **Source:** [WPRDC - Pittsburgh Police Arrest Data](https://data.wprdc.org/dataset/arrest-data)
* **Description:** A dataset containing information on arrests made by the City of Pittsburgh Bureau of Police. It is used to calculate a "Safety Score" where fewer arrests indicate higher safety.
* **Analyst:** Jiakai Dai

### 3. SNAP Census Data (Education Enrollment)
* **Source:** [WPRDC - SNAP Census Data](https://data.wprdc.org/dataset/snap-census-data-populations)
* **Description:** 2010 Census and ACS data focusing on school enrollment figures by neighborhood. It is used to identify areas with high educational engagement and student density.
* **Analyst:** Xiangyu Li

## 5. Execution Instructions
1.  **Individual Metrics:** To see the raw data processing, run the individual notebooks located in the member folders. Each notebook exports a standardized `.csv` file.
2.  **Combined Analysis:** Run `Best_Neighborhood.ipynb` in the root directory. This notebook will:
    * Load the processed CSVs from the respective folders.
    * Merge the data using an inner join (ranking only neighborhoods with data for all 3 metrics).
    * Calculate the final weighted score.
    * Display the "Top 10" visualization and the Conclusion.