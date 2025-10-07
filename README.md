# Aashi-techai_eda_2
# Aashi-techai_eda
The notebook is structured into a few simple steps, and I used pandas, numpy, and matplotlib—the essential trio, apparently!

1. Setup and Loading
Imports: Just getting pandas, numpy, and matplotlib.pyplot ready.

Data Load: Reading in the main CSV file. I checked the basic info (.info()) and the first few rows (.head()) to get a feel for what I'm dealing with.

2. Initial Cleaning and Prep
Column Focus: I mainly worked with Mass_g (mass in grams), Classification, and Year_of_Fall.

Handling Missing Data: I noticed a good chunk of missing data in some key columns (Mass_g, Year_of_Fall), so I had to drop those rows. Gotta keep the analysis clean!

Data Type Fixes: Made sure the Year_of_Fall column was converted to a clean integer format so I could actually use it for filtering and plotting time-series data.

3. Data Filtering (Getting a Usable Subset)
This section was important because the raw data is huge and sometimes messy.

I created a new DataFrame that filters out the super-tiny meteorites and also only looks at recorded falls between the years 1500 and 2024. This helps focus the analysis on reliable and historically relevant records.

I also created a new log-transformed column for the Mass_g because the mass distribution is extremely skewed (a few huge ones, lots of tiny ones). Log-transforming it helped me create a histogram that actually makes sense!

4. Data Preparation for Plots
Mass Distribution: I calculated the log-transformed mass to create a meaningful distribution plot.

Classification Analysis: I focused on finding the Top 10 most common meteorite classifications to see which types of space rocks land on Earth the most. Then, I calculated the average mass for each of those top 10 to see if common types are generally bigger or smaller.

5. Visualizing the Findings 
I made a few basic plots using matplotlib:

Distribution of Log-Transformed Mass: A histogram showing the distribution of mass. This plot is essential for understanding why we had to use log transformation in the first place!

Average Mass by Top 10 Classification: A bar chart to easily compare the size of the most common meteorite types.

Dependencies
You'll need a standard Python environment with these libraries installed:

pandas (for data wrangling)

numpy (for math operations like the log transformation)

matplotlib (for plotting)
