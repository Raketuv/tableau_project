Readme


# Finding the dataset

Searched Awesome Public Data Sets and Kaggle Data Sets for medical datasets suitable for statistical analysis and tableau visualization. Found:

Heart Disease UCI https://www.kaggle.com/ronitf/heart-disease-uci ,which contains several measures associated with heart disease.

Had to go to the source to correctly interprete measures.


# Exploring the dataset

Explored the dataset to find associations between dimensions and heart disease. Used Fisher's exact test and multivariable linear regression OLS (see heart_preprocessing.ipynb). Input: heart.csv, output: heart_edited.csv


# Breaking down into different steps

Analysed binary measures first, then continous measures. Put additional emphasis on cholesterol, as it's connection with heart disease was unclear.


# Use the tools in your tool kit

Used statistical analysis, as well as crosstabs, boxplots and scatter plots in Tableau. Combined multiple graphics into one Dashboard to put into Story.



# Results presented in Tableau story

Tableau Story 1 in : ironhack_project_heartdisease.twbx
(https://public.tableau.com/profile/raketuv.johnson#!/vizhome/ironhack_project_heartdisease/Story1)

1. All binary measures with stastically significant association with heart disease at p>0.005 (statistical significance threshold adjusted for multivariable testing of 10 measures

2. Displays maximum heart rate during exercise and ST-segment depression (some ECG measure) of heart disease and non-heart disease groups. Both are significantly associated with heart disease.

3. Displays sex and age differences in cholesterol. Males have lower mean and variance in total cholesterol.

4. Boxplot visualization of sex differences in cholesterol levels

5. Applied a calculated field in Tableau to filter for only high cholesterol levels, found no association with heart disease.

-> This is interesting, since initial OLS found no association of cholesterol with heart disease. Including sex into regression moves cholesterol association p-value into statistical significance, indicating some sort of interaction. Adding an interaction term (sex*cholesterol) removes the significance again. 


