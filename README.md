# **Average Airline Delay Analysis with nycflights13 Dataset**

## **Description**

This project analyzes flight data from the `nycflights13` dataset to calculate the average delay times for each airline. The goal is to identify which airlines are the most and least reliable in terms of punctuality. The project uses two approaches, Tidyverse and data.table, to clean and manipulate the data, compare performance, and present the results in a table.

---

## **Tools and Libraries Used**

The following tools and libraries were used:

- **R**: Programming language used for the analysis.
- **Tidyverse**: A suite of R packages for data manipulation and visualization.
  - **`dplyr`**: For data cleaning, grouping, and summarizing.
  - **`ggplot2`**: For data visualization.
- **data.table**: A high-performance R package for fast data manipulation.
- **nycflights13**: Provides flight data, including airline codes and delay times.

---

## **Main Functions Used**

### **Tidyverse Approach**
1. **Data Manipulation**:
   - `select()`: To select specific columns from the dataset.
   - `left_join()`: To merge airline names into the flights dataset.
   - `group_by()`: To group data by airline name.
   - `summarize()`: To calculate average delays.
   - `arrange()`: To sort results by average delay.

2. **Timing Execution**:
   - `system.time()`: To measure the time taken for data cleaning and summarization.

### **data.table Approach**
1. **Data Manipulation**:
   - `merge()`: To join flights and airlines data.
   - `[, .()]`: To calculate average delays by airline.
   - `[order()]`: To sort results by average delay.

2. **Timing Execution**:
   - `system.time()`: To measure execution time for data.table operations.

---

## **Tasks Completed**

1. **Data Loading**:
   - Loaded the `nycflights13` dataset, including `flights` and `airlines`.
   - Inspected the structure of the datasets to identify relevant columns.

2. **Data Cleaning**:
   - Selected relevant columns (`carrier`, `dep_delay`, `arr_delay`) from `flights`.
   - Merged the `airlines` dataset to include airline names.

3. **Data Manipulation**:
   - Calculated average departure and arrival delays for each airline.
   - Sorted the results to display airlines with the least delays first.

4. **Performance Comparison**:
   - Compared the execution times of Tidyverse and data.table approaches.

5. **Output Generation**:
   - Produced a clean table showing each airline's average departure and arrival delays.

---

## **Output**

### **Key Observations**:
1. **Airlines with Low or Negative Delays**:
   - Airlines like **Hawaiian Airlines Inc.**, **Alaska Airlines Inc.**, and **US Airways Inc.** have low average delays. Hawaiian Airlines even has a negative average arrival delay, indicating early arrivals.
   
2. **Airlines with High Delays**:
   - Airlines like **ExpressJet Airlines Inc.** and **Frontier Airlines Inc.** have significantly higher average delays.

3. **Performance Comparison**:
   - Tidyverse: **0.07 seconds (elapsed time)**.
   - data.table: **0.06 seconds (elapsed time)**.
   - **data.table** was slightly faster, though both approaches performed similarly for this dataset.

---




