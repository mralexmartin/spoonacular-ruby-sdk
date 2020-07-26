# openapi_client

OpenapiClient - the Ruby gem for the spoonacular API

The spoonacular Nutrition, Recipe, and Food API allows you to access over 380,000 recipes, thousands of ingredients, 80,000 food products, and 100,000 menu items. Our food ontology and semantic recipe search engine makes it possible to search for recipes using natural language queries, such as \"gluten free brownies without sugar\" or \"low fat vegan cupcakes.\" You can automatically calculate the nutritional information for any recipe, analyze recipe costs, visualize ingredient lists, find recipes for what's in your fridge, find recipes based on special diets, nutritional requirements, or favorite ingredients, classify recipes into types and cuisines, convert ingredient amounts, or even compute an entire meal plan. With our powerful API, you can create many kinds of food and especially nutrition apps.

Special diets/dietary requirements currently available include: vegan, vegetarian, pescetarian, gluten free, grain free, dairy free, high protein, whole 30, low sodium, low carb, Paleo, ketogenic, FODMAP, and Primal.

This SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0
- Package version: 1.0.0
- Build package: org.openapitools.codegen.languages.RubyClientCodegen
For more information, please visit [https://spoonacular.com/contact](https://spoonacular.com/contact)

## Installation

### Build a gem

To build the Ruby code into a gem:

```shell
gem build openapi_client.gemspec
```

Then either install the gem locally:

```shell
gem install ./openapi_client-1.0.0.gem
```

(for development, run `gem install --dev ./openapi_client-1.0.0.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the Gemfile:

    gem 'openapi_client', '~> 1.0.0'

### Install from Git

If the Ruby gem is hosted at a git repository: https://github.com/GIT_USER_ID/GIT_REPO_ID, then add the following in the Gemfile:

    gem 'openapi_client', :git => 'https://github.com/GIT_USER_ID/GIT_REPO_ID.git'

### Include the Ruby code directly

Include the Ruby code directly using `-I` as follows:

```shell
ruby -Ilib script.rb
```

## Getting Started

Please follow the [installation](#installation) procedure and then run the following code:

```ruby
# Load the gem
require 'openapi_client'

api_instance = OpenapiClient::DefaultApi.new
username = 'dsky' # String | The username.
hash = '4b5v4398573406' # String | The private hash for the username.
inline_object9 = OpenapiClient::InlineObject9.new # InlineObject9 | 

begin
  #Add to Meal Plan
  result = api_instance.add_to_meal_plan(username, hash, inline_object9)
  p result
rescue OpenapiClient::ApiError => e
  puts "Exception when calling DefaultApi->add_to_meal_plan: #{e}"
end

```

## Documentation for API Endpoints

All URIs are relative to *https://api.spoonacular.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*OpenapiClient::DefaultApi* | [**add_to_meal_plan**](docs/DefaultApi.md#add_to_meal_plan) | **POST** /mealplanner/{username}/items | Add to Meal Plan
*OpenapiClient::DefaultApi* | [**add_to_shopping_list**](docs/DefaultApi.md#add_to_shopping_list) | **POST** /mealplanner/{username}/shopping-list/items | Add to Shopping List
*OpenapiClient::DefaultApi* | [**analyze_a_recipe_search_query**](docs/DefaultApi.md#analyze_a_recipe_search_query) | **GET** /recipes/queries/analyze | Analyze a Recipe Search Query
*OpenapiClient::DefaultApi* | [**analyze_recipe_instructions**](docs/DefaultApi.md#analyze_recipe_instructions) | **POST** /recipes/analyzeInstructions | Analyze Recipe Instructions
*OpenapiClient::DefaultApi* | [**autocomplete_ingredient_search**](docs/DefaultApi.md#autocomplete_ingredient_search) | **GET** /food/ingredients/autocomplete | Autocomplete Ingredient Search
*OpenapiClient::DefaultApi* | [**autocomplete_menu_item_search**](docs/DefaultApi.md#autocomplete_menu_item_search) | **GET** /food/menuItems/suggest | Autocomplete Menu Item Search
*OpenapiClient::DefaultApi* | [**autocomplete_product_search**](docs/DefaultApi.md#autocomplete_product_search) | **GET** /food/products/suggest | Autocomplete Product Search
*OpenapiClient::DefaultApi* | [**autocomplete_recipe_search**](docs/DefaultApi.md#autocomplete_recipe_search) | **GET** /recipes/autocomplete | Autocomplete Recipe Search
*OpenapiClient::DefaultApi* | [**classify_cuisine**](docs/DefaultApi.md#classify_cuisine) | **POST** /recipes/cuisine | Classify Cuisine
*OpenapiClient::DefaultApi* | [**classify_grocery_product**](docs/DefaultApi.md#classify_grocery_product) | **POST** /food/products/classify | Classify Grocery Product
*OpenapiClient::DefaultApi* | [**classify_grocery_product_bulk**](docs/DefaultApi.md#classify_grocery_product_bulk) | **POST** /food/products/classifyBatch | Classify Grocery Product Bulk
*OpenapiClient::DefaultApi* | [**convert_amounts**](docs/DefaultApi.md#convert_amounts) | **GET** /recipes/convert | Convert Amounts
*OpenapiClient::DefaultApi* | [**create_recipe_card**](docs/DefaultApi.md#create_recipe_card) | **POST** /recipes/visualizeRecipe | Create Recipe Card
*OpenapiClient::DefaultApi* | [**delete_from_meal_plan**](docs/DefaultApi.md#delete_from_meal_plan) | **DELETE** /mealplanner/{username}/items/{id} | Delete from Meal Plan
*OpenapiClient::DefaultApi* | [**delete_from_shopping_list**](docs/DefaultApi.md#delete_from_shopping_list) | **DELETE** /mealplanner/{username}/shopping-list/items/{id} | Delete from Shopping List
*OpenapiClient::DefaultApi* | [**detect_food_in_text**](docs/DefaultApi.md#detect_food_in_text) | **POST** /food/detect | Detect Food in Text
*OpenapiClient::DefaultApi* | [**extract_recipe_from_website**](docs/DefaultApi.md#extract_recipe_from_website) | **GET** /recipes/extract | Extract Recipe from Website
*OpenapiClient::DefaultApi* | [**generate_meal_plan**](docs/DefaultApi.md#generate_meal_plan) | **GET** /mealplanner/generate | Generate Meal Plan
*OpenapiClient::DefaultApi* | [**generate_shopping_list**](docs/DefaultApi.md#generate_shopping_list) | **POST** /mealplanner/{username}/shopping-list/{start-date}/{end-date} | Generate Shopping List
*OpenapiClient::DefaultApi* | [**get_a_random_food_joke**](docs/DefaultApi.md#get_a_random_food_joke) | **GET** /food/jokes/random | Get a Random Food Joke
*OpenapiClient::DefaultApi* | [**get_analyzed_recipe_instructions**](docs/DefaultApi.md#get_analyzed_recipe_instructions) | **GET** /recipes/{id}/analyzedInstructions | Get Analyzed Recipe Instructions
*OpenapiClient::DefaultApi* | [**get_comparable_products**](docs/DefaultApi.md#get_comparable_products) | **GET** /food/products/upc/{upc}/comparable | Get Comparable Products
*OpenapiClient::DefaultApi* | [**get_conversation_suggests**](docs/DefaultApi.md#get_conversation_suggests) | **GET** /food/converse/suggest | Get Conversation Suggests
*OpenapiClient::DefaultApi* | [**get_dish_pairing_for_wine**](docs/DefaultApi.md#get_dish_pairing_for_wine) | **GET** /food/wine/dishes | Get Dish Pairing for Wine
*OpenapiClient::DefaultApi* | [**get_ingredient_information**](docs/DefaultApi.md#get_ingredient_information) | **GET** /food/ingredients/{id}/information | Get Ingredient Information
*OpenapiClient::DefaultApi* | [**get_ingredient_substitutes**](docs/DefaultApi.md#get_ingredient_substitutes) | **GET** /food/ingredients/substitutes | Get Ingredient Substitutes
*OpenapiClient::DefaultApi* | [**get_ingredient_substitutes_by_id**](docs/DefaultApi.md#get_ingredient_substitutes_by_id) | **GET** /food/ingredients/{id}/substitutes | Get Ingredient Substitutes by ID
*OpenapiClient::DefaultApi* | [**get_meal_plan_template**](docs/DefaultApi.md#get_meal_plan_template) | **GET** /mealplanner/{username}/templates/{id} | Get Meal Plan Template
*OpenapiClient::DefaultApi* | [**get_meal_plan_templates**](docs/DefaultApi.md#get_meal_plan_templates) | **GET** /mealplanner/{username}/templates | Get Meal Plan Templates
*OpenapiClient::DefaultApi* | [**get_meal_plan_week**](docs/DefaultApi.md#get_meal_plan_week) | **GET** /mealplanner/{username}/week/{start-date} | Get Meal Plan Week
*OpenapiClient::DefaultApi* | [**get_menu_item_information**](docs/DefaultApi.md#get_menu_item_information) | **GET** /food/menuItems/{id} | Get Menu Item Information
*OpenapiClient::DefaultApi* | [**get_product_information**](docs/DefaultApi.md#get_product_information) | **GET** /food/products/{id} | Get Product Information
*OpenapiClient::DefaultApi* | [**get_random_food_trivia**](docs/DefaultApi.md#get_random_food_trivia) | **GET** /food/trivia/random | Get Random Food Trivia
*OpenapiClient::DefaultApi* | [**get_random_recipes**](docs/DefaultApi.md#get_random_recipes) | **GET** /recipes/random | Get Random Recipes
*OpenapiClient::DefaultApi* | [**get_recipe_equipment_by_id**](docs/DefaultApi.md#get_recipe_equipment_by_id) | **GET** /recipes/{id}/equipmentWidget.json | Get Recipe Equipment by ID
*OpenapiClient::DefaultApi* | [**get_recipe_information**](docs/DefaultApi.md#get_recipe_information) | **GET** /recipes/{id}/information | Get Recipe Information
*OpenapiClient::DefaultApi* | [**get_recipe_information_bulk**](docs/DefaultApi.md#get_recipe_information_bulk) | **GET** /recipes/informationBulk | Get Recipe Information Bulk
*OpenapiClient::DefaultApi* | [**get_recipe_ingredients_by_id**](docs/DefaultApi.md#get_recipe_ingredients_by_id) | **GET** /recipes/{id}/ingredientWidget.json | Get Recipe Ingredients by ID
*OpenapiClient::DefaultApi* | [**get_recipe_nutrition_widget_by_id**](docs/DefaultApi.md#get_recipe_nutrition_widget_by_id) | **GET** /recipes/{id}/nutritionWidget.json | Get Recipe Nutrition Widget by ID
*OpenapiClient::DefaultApi* | [**get_recipe_price_breakdown_by_id**](docs/DefaultApi.md#get_recipe_price_breakdown_by_id) | **GET** /recipes/{id}/priceBreakdownWidget.json | Get Recipe Price Breakdown by ID
*OpenapiClient::DefaultApi* | [**get_shopping_list**](docs/DefaultApi.md#get_shopping_list) | **GET** /mealplanner/{username}/shopping-list | Get Shopping List
*OpenapiClient::DefaultApi* | [**get_similar_recipes**](docs/DefaultApi.md#get_similar_recipes) | **GET** /recipes/{id}/similar | Get Similar Recipes
*OpenapiClient::DefaultApi* | [**get_wine_description**](docs/DefaultApi.md#get_wine_description) | **GET** /food/wine/description | Get Wine Description
*OpenapiClient::DefaultApi* | [**get_wine_pairing**](docs/DefaultApi.md#get_wine_pairing) | **GET** /food/wine/pairing | Get Wine Pairing
*OpenapiClient::DefaultApi* | [**get_wine_recommendation**](docs/DefaultApi.md#get_wine_recommendation) | **GET** /food/wine/recommendation | Get Wine Recommendation
*OpenapiClient::DefaultApi* | [**guess_nutrition_by_dish_name**](docs/DefaultApi.md#guess_nutrition_by_dish_name) | **GET** /recipes/guessNutrition | Guess Nutrition by Dish Name
*OpenapiClient::DefaultApi* | [**image_analysis_by_url**](docs/DefaultApi.md#image_analysis_by_url) | **GET** /food/images/analyze | Image Analysis by URL
*OpenapiClient::DefaultApi* | [**image_classification_by_url**](docs/DefaultApi.md#image_classification_by_url) | **GET** /food/images/classify | Image Classification by URL
*OpenapiClient::DefaultApi* | [**map_ingredients_to_grocery_products**](docs/DefaultApi.md#map_ingredients_to_grocery_products) | **POST** /food/ingredients/map | Map Ingredients to Grocery Products
*OpenapiClient::DefaultApi* | [**parse_ingredients**](docs/DefaultApi.md#parse_ingredients) | **POST** /recipes/parseIngredients | Parse Ingredients
*OpenapiClient::DefaultApi* | [**quick_answer**](docs/DefaultApi.md#quick_answer) | **GET** /recipes/quickAnswer | Quick Answer
*OpenapiClient::DefaultApi* | [**search_custom_foods**](docs/DefaultApi.md#search_custom_foods) | **GET** /food/customFoods/search | Search Custom Foods
*OpenapiClient::DefaultApi* | [**search_food_videos**](docs/DefaultApi.md#search_food_videos) | **GET** /food/videos/search | Search Food Videos
*OpenapiClient::DefaultApi* | [**search_grocery_products**](docs/DefaultApi.md#search_grocery_products) | **GET** /food/products/search | Search Grocery Products
*OpenapiClient::DefaultApi* | [**search_grocery_products_by_upc**](docs/DefaultApi.md#search_grocery_products_by_upc) | **GET** /food/products/upc/{upc} | Search Grocery Products by UPC
*OpenapiClient::DefaultApi* | [**search_menu_items**](docs/DefaultApi.md#search_menu_items) | **GET** /food/menuItems/search | Search Menu Items
*OpenapiClient::DefaultApi* | [**search_recipes**](docs/DefaultApi.md#search_recipes) | **GET** /recipes/search | Search Recipes
*OpenapiClient::DefaultApi* | [**search_recipes_by_ingredients**](docs/DefaultApi.md#search_recipes_by_ingredients) | **GET** /recipes/findByIngredients | Search Recipes by Ingredients
*OpenapiClient::DefaultApi* | [**search_recipes_by_nutrients**](docs/DefaultApi.md#search_recipes_by_nutrients) | **GET** /recipes/findByNutrients | Search Recipes by Nutrients
*OpenapiClient::DefaultApi* | [**search_recipes_complex**](docs/DefaultApi.md#search_recipes_complex) | **GET** /recipes/complexSearch | Search Recipes Complex
*OpenapiClient::DefaultApi* | [**search_site_content**](docs/DefaultApi.md#search_site_content) | **GET** /food/site/search | Search Site Content
*OpenapiClient::DefaultApi* | [**summarize_recipe**](docs/DefaultApi.md#summarize_recipe) | **GET** /recipes/{id}/summary | Summarize Recipe
*OpenapiClient::DefaultApi* | [**talk_to_chatbot**](docs/DefaultApi.md#talk_to_chatbot) | **GET** /food/converse | Talk to Chatbot
*OpenapiClient::DefaultApi* | [**visualize_equipment**](docs/DefaultApi.md#visualize_equipment) | **POST** /recipes/visualizeEquipment | Visualize Equipment
*OpenapiClient::DefaultApi* | [**visualize_ingredients**](docs/DefaultApi.md#visualize_ingredients) | **POST** /recipes/visualizeIngredients | Visualize Ingredients
*OpenapiClient::DefaultApi* | [**visualize_menu_item_nutrition_by_id**](docs/DefaultApi.md#visualize_menu_item_nutrition_by_id) | **GET** /food/menuItems/{id}/nutritionWidget | Visualize Menu Item Nutrition by ID
*OpenapiClient::DefaultApi* | [**visualize_price_breakdown**](docs/DefaultApi.md#visualize_price_breakdown) | **POST** /recipes/visualizePriceEstimator | Visualize Price Breakdown
*OpenapiClient::DefaultApi* | [**visualize_product_nutrition_by_id**](docs/DefaultApi.md#visualize_product_nutrition_by_id) | **GET** /food/products/{id}/nutritionWidget | Visualize Product Nutrition by ID
*OpenapiClient::DefaultApi* | [**visualize_recipe_equipment_by_id**](docs/DefaultApi.md#visualize_recipe_equipment_by_id) | **GET** /recipes/{id}/equipmentWidget | Visualize Recipe Equipment by ID
*OpenapiClient::DefaultApi* | [**visualize_recipe_ingredients_by_id**](docs/DefaultApi.md#visualize_recipe_ingredients_by_id) | **GET** /recipes/{id}/ingredientWidget | Visualize Recipe Ingredients by ID
*OpenapiClient::DefaultApi* | [**visualize_recipe_nutrition**](docs/DefaultApi.md#visualize_recipe_nutrition) | **POST** /recipes/visualizeNutrition | Visualize Recipe Nutrition
*OpenapiClient::DefaultApi* | [**visualize_recipe_nutrition_by_id**](docs/DefaultApi.md#visualize_recipe_nutrition_by_id) | **GET** /recipes/{id}/nutritionWidget | Visualize Recipe Nutrition by ID
*OpenapiClient::DefaultApi* | [**visualize_recipe_price_breakdown_by_id**](docs/DefaultApi.md#visualize_recipe_price_breakdown_by_id) | **GET** /recipes/{id}/priceBreakdownWidget | Visualize Recipe Price Breakdown by ID


## Documentation for Models

 - [OpenapiClient::InlineObject10](docs/InlineObject10.md)
 - [OpenapiClient::InlineObject11](docs/InlineObject11.md)
 - [OpenapiClient::InlineObject12](docs/InlineObject12.md)
 - [OpenapiClient::InlineObject13](docs/InlineObject13.md)
 - [OpenapiClient::InlineObject8](docs/InlineObject8.md)
 - [OpenapiClient::InlineObject9](docs/InlineObject9.md)


## Documentation for Authorization

```
config = OpenapiClient::Configuration.default
config.api_key['api_key'] = 'abcdef'
api_client = OpenapiClient::ApiClient.new config
api_instance = OpenapiClient::DefaultApi.new api_client

result = api_instance.generate_meal_plan({
  time_frame: 'day', target_calories: 2000, diet: 'vegetarian',
  exclude: 'shellfish, olives',
})
```

### apiKeyScheme


- **Type**: API key
- **API key parameter name**: api_key
- **Location**: URL query string

