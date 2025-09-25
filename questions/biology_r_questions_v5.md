# R Programming Assessment Questions for Biology Students
Group 1 2 3 = q1_dataset
Group 4 5 6 = q2_dataset
Group 7 8 9 = q3_dataset
Group 10 11 12 = q4_dataset

## Dataset 1: Plant Photosynthesis Experiment Questions

**Dataset Description:** 60 plants across three species (Arabidopsis, Tobacco, Spinach) with measurements of chlorophyll levels, photosynthesis rates, and environmental conditions.

### Question 1.1 - Data Exploration
Load the plant photosynthesis dataset and use appropriate R functions to display the first 8 rows, examine the structure of the data frame, and generate summary statistics for all variables. What data types are present in each column?

### Question 1.2 - Vector Operations and Statistics
Extract the photosynthesis rate measurements into a separate vector. Calculate the mean, median, standard deviation, minimum, maximum, and total number of observations. Which plant achieved the highest photosynthesis rate?

### Question 1.3 - Categorical Data Analysis
Convert the Light_Intensity variable to a factor and determine how many plants were tested under each light condition. Create a frequency table showing the distribution of plants across different light intensity levels.

### Question 1.4 - Data Filtering with Base R
Using base R indexing methods, create a subset containing only Arabidopsis plants that achieved photosynthesis rates greater than 15.0. How many plants meet these criteria, and what are their average initial and final chlorophyll levels?

### Question 1.5 - Data Manipulation with dplyr
Using dplyr functions, filter the dataset to include only plants grown under High light intensity conditions, select the columns for Species, CO2_Level, and Photosynthesis_Rate, and arrange the results in descending order by photosynthesis rate.

---

## Dataset 2: Animal Behavioral Study Questions

**Dataset Description:** 75 animals across three species (Rat, Mouse, Hamster) with different dietary treatments and behavioral measurements.

### Question 2.1 - Data Structure Examination
Load the animal behavioral dataset and examine its structure using str(), head(), and summary() functions. Identify which variables are numeric, which are categorical, and determine the total number of observations per species.

### Question 2.2 - Weight Gain Analysis
Calculate the weight gain for each animal and add this as a new column to the data frame. Determine which animal achieved the maximum weight gain and provide its complete information including species and diet type.

### Question 2.3 - Factor Conversion and Analysis
Convert the Diet_Type variable to a factor and create a frequency table showing how many animals received each dietary treatment. Which diet type was most commonly administered in this study?

### Question 2.4 - Age-Based Filtering
Using base R methods, create a subset containing only animals that are between 90 and 150 days old. Calculate the average initial weight, final weight, and activity score for this age group.

### Question 2.5 - Species Comparison with dplyr
Use dplyr functions to group the data by Species and calculate the mean initial weight, mean final weight, and mean activity score for each species. Which species has the highest average activity score?

---

## Dataset 3: Microbial Growth Experiment Questions

**Dataset Description:** 48 bacterial cultures from four strains with antibiotic treatments and growth measurements.

### Question 3.1 - Dataset Overview
Load the microbial growth dataset and provide a comprehensive overview including the number of observations, variable types, and summary statistics. How many different bacterial strains were tested in this experiment?

### Question 3.2 - Growth Rate Calculation Verification
Verify the growth rate calculations by manually computing growth rates for the first five cultures using the formula: (Final_OD600 - Initial_OD600) / Growth_Time_Hours. Do your calculations match the provided Growth_Rate values?

### Question 3.3 - Antibiotic Treatment Analysis
Create a frequency table showing the distribution of cultures across different antibiotic treatments. Convert the Antibiotic variable to a factor and determine which treatment was most frequently used.

### Question 3.4 - Temperature Effect Investigation
Filter the dataset to include only cultures grown at 37°C (typical human body temperature). Calculate summary statistics for growth rates at this temperature and identify which bacterial strain performed best under these conditions.

### Question 3.5 - Strain-Specific Analysis with dplyr
Using dplyr, group the data by Bacterial_Strain and calculate the average Initial_OD600, Final_OD600, and Growth_Rate for each strain. Arrange the results by descending average growth rate.

---

## Dataset 4: Seed Germination Study Questions

**Dataset Description:** 90 experimental groups examining seed germination across three plant species under different soil and watering conditions.

### Question 4.1 - Experimental Design Overview
Load the seed germination dataset and analyze the experimental design. Use appropriate R functions to determine how many replicates were used for each combination of Plant_Species, Soil_Type, and Water_Frequency.

### Question 4.2 - Germination Success Analysis
Calculate summary statistics for Seeds_Germinated and Germination_Percent variables. Which experimental group achieved the highest number of germinated seeds, and what were the conditions for this group?

### Question 4.3 - Soil Type Factor Analysis
Convert Soil_Type to a factor and create a table showing the distribution of experimental groups across soil types. Calculate the average germination percentage for each soil type.

### Question 4.4 - Species-Specific Performance
Filter the dataset to include only Tomato plants and calculate the mean germination percentage, mean days to germination, and mean germination rate for this species across all experimental conditions.

### Question 4.5 - Water Frequency Impact with dplyr
Use dplyr functions to group the data by Water_Frequency and calculate the average germination percentage and average days to germination for each watering schedule. Which watering frequency produces the best germination results?

---

## Assessment Guidelines

Each question is designed to test specific R programming skills taught in the introductory biology course:

- **Questions 1, 4:** Advanced analytical skills requiring multiple R concepts
- **Questions 2, 5** Fundamental data manipulation and statistical operations  
- **Questions 3:** Data visualization and statistical testing proficiency
- **Integration across questions:** Progressive complexity building from basic operations to advanced multi-factor analysis

Students should provide both R code and biological interpretation for each answer, demonstrating technical proficiency alongside scientific reasoning skills essential for modern biological research.