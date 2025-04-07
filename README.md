🥘 Recipe Recommendation System:

A smart food recommendation system that suggests recipes based on the ingredients you have! Powered by TF-IDF Vectorization, Cosine Similarity, and a clean, rich dataset, this system helps users find recipes matching their taste, cuisine, dietary preferences, and available ingredients.

📂 Project Overview:

This project takes a CSV file of food recipes, cleans and processes the data, then uses machine learning techniques to recommend the top 5 recipes similar to the user's provided ingredients. Users can also filter results by cuisine, diet, or course. Additionally, data visualizations are provided to better understand recipe distributions.

🚀 Features:

🔍 Ingredient-based Recipe Recommendation
🧠 TF-IDF + Cosine Similarity Matching
🍽️ Filter by Cuisine, Diet, and Course
📊 Visual Analysis using Seaborn and Matplotlib
🧹 Text Preprocessing & Cleaning
✅ Missing Values Handling and Duplicate Removal

📁 Dataset:

File: Food_Recipe.csv

- Columns used:
1- name
2- ingredients_name
3- instructions
4- cuisine
5-  course
6- diet
7- cook_time (in mins)

🧪 How it Works:

- Preprocessing:

1- Remove rows with missing essential values.
2- Fill missing optional columns with 'Unknown'.
3- Convert text to lowercase and remove special characters.
4- Remove duplicate entries.

- Vectorization:
  
TF-IDF is applied on the cleaned ingredient list to convert them into numeric vectors.

- Recommendation:

1- The user enters available ingredients.
2- Cosine similarity compares user ingredients with recipes.
3- Top 5 recipes are recommended and filtered by user preference.

🖼️ Visualizations:

1- Top 10 Cuisines
2- Top 15 Common Ingredients
3- Course Distribution (Pie Chart)
4-  Dietary Preferences (Pie Chart)

📌 Requirements:

Make sure you have the following libraries installed:
          "pip install pandas numpy matplotlib seaborn scikit-learn"

▶️ How to Run:

Download the dataset and update the CSV path in the code:  
            "df = pd.read_csv("path/to/Food_Recipe.csv")"
Run the Python file:
              "python recipe_recommender.py"
Enter the ingredients and filter preferences when prompted:
              "Enter preferred cuisine (or press Enter to skip):
               Enter preferred diet (or press Enter to skip):
               Enter preferred course (or press Enter to skip):"

🔎 Sample Output:

🍕 Recipe Name: Margherita Pizza  
🌍 Cuisine: Italian  
🍽️ Course: Main Course  
🥗 Diet: Vegetarian  
⏳ Cook Time: 30 mins  
🛒 Ingredients: tomato, cheese, garlic, basil

📜 Cooking Instructions:

   🔹 Step 1: Preheat oven to 200 degrees.
   🔹 Step 2: Spread tomato sauce over dough.
   🔹 Step 3: Add cheese and basil.
   🔹 Step 4: Bake until golden and bubbly.
   

 📬 Contact:
 
Feel free to reach out if you want to collaborate or have suggestions:

  - Name: Subhaan Khokhar
  - Email: mskproductions2002@gmail.com
  - LinkedIn: https://www.linkedin.com/in/muhammad-subhan-khokhar/

              







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
