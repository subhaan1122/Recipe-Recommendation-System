This project leverages a dataset of food recipes to recommend recipes to users based on the ingredients they have on hand. It includes data preprocessing, text cleaning, and machine learning techniques, specifically TF-IDF vectorization and cosine similarity, to suggest recipes that match the user-provided ingredients.

-> Overview:

The goal of this project is to recommend food recipes based on the ingredients the user provides. The system processes a dataset containing food recipes, cleans and preprocesses the data, and uses machine learning techniques like TF-IDF vectorization and cosine similarity to suggest the best-matching recipes. Additionally, users can filter recommendations by cuisine, diet, and course preferences.

-> Dataset:

The dataset used in this project contains various food recipes with the following columns:

1-name: The name of the recipe.

2-ingredients_name: A list of ingredients for the recipe.

3-instructions: Step-by-step instructions for preparing the recipe.

4-cuisine: The cuisine type (e.g., Italian, Mexican).

5-course: The type of meal (e.g., breakfast, lunch).

6-diet: Dietary preferences (e.g., vegetarian, gluten-free).

7-cook_time (in mins): The estimated cook time in minutes.

-> Data Preprocessing:

Selection of Essential Columns: We keep only the relevant columns: name, ingredients_name, instructions, cuisine, course, diet, and cook_time (in mins).

- Handling Missing Data:
  
Rows with missing values in essential columns (name, ingredients_name, and instructions) are dropped.
Missing values in optional columns are filled with the string 'Unknown'.

- Text Cleaning:

All text columns (e.g., name, ingredients_name, instructions) are converted to lowercase for consistency.
Special characters are removed from the ingredients_name column.
Extra spaces are stripped and redundant spaces are removed from ingredient lists.
Duplicate Removal: Exact duplicate rows are removed to ensure the dataset is unique.

-> TF-IDF Vectorization:

To transform the ingredients into a format suitable for machine learning, we use the TF-IDF (Term Frequency-Inverse Document Frequency) technique. This technique converts the list of ingredients into numerical vectors, making it easier to calculate the similarity between the user's input and the recipes.
The vectorizer is fitted and transformed using the ingredients_name column, which is cleaned and processed to ensure proper consistency.

-> Recipe Recommendation:

The system uses cosine similarity to match the user’s input ingredients with the recipes in the dataset. It works as follows:

1-User Input: The user provides a list of ingredients.

2-Ingredient Cleaning: The input ingredients are cleaned in the same manner as the dataset.

3-Cosine Similarity Calculation: The input ingredients are transformed into a TF-IDF vector and compared with the vectors of all recipes using cosine similarity.

4-Top Recipes: The top 5 recipes with the highest similarity scores are selected.

5-Filtering Recipes by Preferences

-Users can further filter the recommended recipes based on their preferences:

1-Cuisine: Filter by preferred cuisine type (e.g., Italian, Chinese).

2-Diet: Filter by dietary preferences (e.g., vegetarian, gluten-free).

3-Course: Filter by meal type (e.g., breakfast, lunch, dinner).

The system first recommends recipes based on the ingredients and then filters the results based on the user's preferences.

-> Visualizations
The system also includes various visualizations to analyze the dataset:

-Cuisine Distribution: A bar plot showing the top 10 cuisines in the dataset.

-Most Common Ingredients: A bar plot showing the top 15 most common ingredients.

-Recipe Course Distribution: A pie chart showing the distribution of different meal courses (e.g., breakfast, lunch).

-Dietary Preference Distribution: A pie chart showing the distribution of different dietary preferences (e.g., vegetarian, gluten-free).

-> Usage:
To use the recipe recommendation system:

1- Input Ingredients: Enter the ingredients you have on hand.
2- Optional Filters: Provide additional preferences for cuisine, diet, and course (or leave them empty to skip).
Recommendations: The system will display the top 5 recipes matching your ingredients, along with their cuisine, course, diet, cook time, and cooking instructions.
