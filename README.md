# Recipy 
#### Recipe Search Engine
Recipy is a website which allows you to search for recipes of a provided item. It also extends to provide you with the ingredients based on the number of servings. And providing an option to add those ingredients to a shopping list where you can increase or decrease portion sizes based on your availability.

#### Approach:

Recipy site adapted MVC architecture where the functionalities are mainly divided into:
* Search Model - Search View
* Recipe Model - Recipe View
* List Model - List View (Shopping list)
* Like Model-Likeke View (Favourite recipe)

Each "model" has its own associated "view" to handle the user interactions on the interface. All the communications between model and 
views are controlled by the Controller.

#### Search - (Model,View):
Search model fetches and returns the results to search view from APIs using async- await for an input item, where search view renders the results and displays it in search results container using DOM manipulations which has the title, author, image, URL for the recipe. The search results container incorporates a pagination technique to display 
10 results per page and page navigation.

#### Recipe - (Model,View):
Recipe model handles on getting the ingredients, calculating, updating, parsing the servings for a selected recipe from search view results.  All these calculations are rendered on the interface using a recipe view where user can interact to change the servings and add the ingredients to the shopping list.

#### Shopping List - (Model,View):
When a user clicks the shopping list buttons all the ingredients are added to the shopping cart where the shopping model performs operations like
add, delete and update the item based on the user interacting with options. All the options operations are displayed using Recipe View. 

#### Favourite recipe - (Model,View):
When a user clicks the heart item on like view, these interaction leads to add the recipe to a favourite recipe list and implements this list to local storage to store the list locally.

#### App controller:
App controller handles the communication between the controller for each model and a view. It will also setups the global event listener which has to be initialized on load stage.

#### Production stage:
With the help of webpack and npm configuring to the development stage and production, the development stage was done through a local server. All the models and views have a separate js file which helps to import and export required functions. All these separate
js files are combined into the single file as bundle.js which is production-ready.
npm helps to install all the required packages using "npm install" command.

#### Techniques Implemented:
* Model View Controller architecture.
* Modern JavaScript - WebPack, npm, Babel, Configurations, Callbacks, Promises, Async - Await, Classes, Arrow Functions, APIs, Pagination, 
Local Storage.
* Prototype Chain, Hoisting, Scope Chain, Closures, Array Methods (ForEach, Map, Splice, Slice, findIndex), DOM Manipulations, Event Delegation - Event Bubbling.


###### Note: This project has been implemented as a part of Udemy - The Complete JavaScript Course 2019: Build Real World Projects
