# Diet-Diary




 




Method 	Description
north()
-basic_app_new	Renders the north.html template with all the food items present in the Food_diary_new table in the database with pagination
purchase_card()
-basic_app_new	Renders the purchase.html template with the different sections of shop names.
cuisine_cards()

-home_app_new	Renders the cuisine.html template with the different sections in the assorted food items like :south indian, chinese,etc where user can select from.











cuisine_cards.html:





Method 	Description
south()
-home_app_new	Renders the assorted.html template , and passes those values in table cuisine_consumption_temp in which user_id = current user’s user_id & food_type = ‘South Indian Food’.
Also it passes all values from olf_food_diary where food_type = ‘South Indian Food’
chinese()
-home_app_new	Renders the assorted.html template , and passes those values in table cuisine_consumption_temp in which user_id = current user’s user_id & food_type = ‘Chinesel’.
Also it passes all values from olf_food_diary where food_type = ‘Chinese’
sweet()
-home_app_new	Renders the assorted.html template , and passes those values in table cuisine_consumption_temp in which user_id = current user’s user_id & food_type = ‘Sweet Dish’.
Also it passes all values from olf_food_diary where food_type = ‘Sweet DIsh’
continental()
-home_app_new	Renders the assorted.html template , and passes those values in table cuisine_consumption_temp in which user_id = current user’s user_id & food_type = ‘Continental’.
Also it passes all values from olf_food_diary where food_type = ‘Continental’


assorted.html:
  

Method 	Description
set_val2()	Sets the current item id , item name to the respective fields. Sets quantity to 1 by default and sets the meal type according to the system time for the form in the modal #modalBuyForm.
set_val3()	Sets the current item id , item name to the respective fields. Sets quantity to 1 by default and sets the meal type according to the system time  for the form in the modal #modalAddFood.
confirm_file1()
-home_app_new	Takes in csv input and converts to dataframe. Adds the values to the cusisine_consumption_temp table.
south_search()
-home_app_new	Renders south_search.html template.In this function it get a ‘southquery’ from search form present in the assorted.html file and returns only that food items related to the search query and food_type==South Indian Food from the Old_Food_Diary table.




 









 
 






Method 	Description
chinese_search()
-home_app_new	Renders chinese_search.html template.In this function it get a ‘chinesequery’ from search form present in the assorted.html file and returns only that food items related to the search query and food_type==Chinese from the Old_Food_Diary table.

continental_search()
-home_app_new	Renders continental_search.html template.In this function it get a ‘continentalquery’ from search form present in the assorted.html file and returns only that food items related to the search query and food_type==Continental from the Old_Food_Diary table.
sweet_search()
-home_app_new	Renders sweet_search.html template.In this function it get a ‘sweetquery’ from search form present in the assorted.html file and returns only that food items related to the search query and food_type==Sweet Dish from the Old_Food_Diary table.














 


Method 	Description
confirm_consumption()	Takes in the form values as inputs and stores the details into cuisine_consumption_temp table.

 










Method 	Description
confirm_consumption()
-home_app_new	Takes in the form values as inputs and stores the details into cuisine_consumption_temp table.
confirm_file1()
-home_app_new	Takes in csv input and converts to dataframe. Adds the values to the cusisine_consumption_temp table.
delete_Row()	A javascript function that extracts the corresponding food id of the item to be deleted and maps it to the url for the view function called delete_cusine().
delete_cusisne()
-home_app_new	Delete the respective food item from the cuisine_consumption_temp table.

modalAddFood:

 


Method 	Description
confirm_consumption2()	Takes in the form values as inputs and stores the details into cuisine_consumption_temp table.





cuisine_consumed.html:
 


Method 	Description
save_cuisine()
-home_app_new	Takes all rows in cuisine_consumption temp where user_id = current user_id and appends it to cuisine_consumption_det table. Clears cuisine_consumption_temp where user_id = current user_id.
confirm_file2()
-home_app_new	Takes in csv input and converts to dataframe. Adds the values to the cusisine_consumption_temp table.
delete_Row()	A javascript function that extracts the corresponding food id of the item to be deleted and maps it to the url for the view function called delete_cusine().
delete_cusisne()
-home_app_new	Delete the respective food item from the cuisine_consumption_temp table.













purchase_cards.html:
 



Method 	Description
amazon()
-home_app_new	Renders amazon.html template with all the food items related to the shop_name==amazon with pagination from the table name purchase_cards.
grofers()
-home_app_new	Renders amazon.html template with all the food items related to the shop_name==Grofers
 with pagination from the table name purchase_cards.
bb()
-home_app_new	Renders amazon.html template with all the food items related to the shop_name==BigBasket with pagination from the table name purchase_cards.
others()
-home_app_new	Renders amazon.html template with all the food items excluding the list of shop_name {amazon,BigBasket,Grofers} with pagination from the table name purchase_cards.








amazon.html:
 



Method 	Description
amazon_search()
-home_app_new	Renders amazon_search.html template.In this function it get a ‘amazonquery’ from search form present in the amazon.html file and returns only that food items related to the search query and shop_name==amazon from the purchase_cards table.
confirm_file3()
-home_app_new	Takes in csv input and converts to dataframe. Adds the values to the temporary_purchase_new table.


 

Method 	Description
confirm_purchase()	Takes in the form values as inputs, also fetches values via api and stores the details into temporary_purchase_new table.

 










modalPurchase:
 

Method 	Description
confirm_purchase2()	Takes in the form values as inputs and stores the details into temporary_purchase_new table.

amazon.html:

 




Method 	Description
groffers_search()
-home_app_new	Renders groffers_search.html template.In this function it get a ‘groffersquery’ from search form present in the amazon.html file and returns only that food items related to the search query and shop_name==Grofers from the purchase_cards table.


amazon.html:

 





Method 	Description
bb_search()
-home_app_new	Renders bb_search.html template.In this function it get a ‘bbquery’ from search form present in the amazon.html file and returns only that food items related to the search query and shop_name==BigBasket from the purchase_cards table.





amazon.html:
 




Method 	Description
other_search()
-home_app_new	Renders other_search.html template.In this function it get a ‘otherquery’ from search form present in the amazon.html file and returns all the food items present in the purchase_cards table.




















north.html:

 

Method 	Description
details()
-home_app_new	Function takes in the food name as argument and calls another function get_food_details() which takes the food name as argument. Then passes the details returned by the latter to the template details.html
get_food_details()
-home_app_new	Calls tpancare api to fetch details of the food item using it’s food name.


















modalconsume:
 

Method 	Description
add_item1()
-home_app_new	Takes in the form values as inputs and stores the details into temporary_transaction_new table.

details.html:
 




API calling functions:


Method 	Description
check_user()
-home_app_new	Calls the tpancare api to verify whether the user id and password are correct. It returns the first name and last name of the user if the user exists.
get_food_details()
-home_app_new	Calls the tpancare api to get the details and nutrition values of a food item from the food master table, by passing the seqid of the food item.
store_pancare()
-home_app_new	
userfoodlogchart()
-home_app_new	


Admin Login
















Method	Description

FoodIndex_new: admin_page()	On clicking the “Admin Login” button, admin_page() function is called and it renders the admin_login.html file; redirects to Admin Login page
















Method	Description

FoodIndex_new: admin_login()	On clicking the “Login” button, admin_login() function is called.  If the Admin Id or Password is wrong, an error message is shown: “Invalid Admin or Password”; if the data is correct, it renders the fm_table.html file.








Method	Description

Food Master Table	After successful login to admin page, the food master table appears which contains data fetched from MySQL central database. 
“Add New Food” Button:- 
              FoodIndex_new: add_food()	When “Add New Food” is clicked, the webpage is rendered to add_food.html file, from which a new individual food item can be added into the database.
“Add New CSV File” Button:- 
              FoodIndex_new: xyz()	When “Add New CSV File” is clicked, the webpage is rendered to upload_file.html file, from which food items can be batch uploaded into database.
“Edit” button: 
              FoodIndex_new: update_food()	When “Edit” button is clicked, it renders update_form.html file and redirects to webpage through which the details of the food item can be modified.
“Delete” button: 
              FoodIndex_new: delete_food()	When “Delete” button is clicked, it deletes that item from the database.
“Recipe” button	On hovering over “Recipe”, the link to recipe can be found.
“Buy” button	On hovering over “Buy”, the link to purchase the food item can be found.


Add Food Item Manually


Method	Description
“Add Food Manually”	When “Add New Food” is clicked on Food Master Table, this webpage is shown. Several input fields are shown.
“Submit” button:- FoodIndex_new: getdata()	When Submit button is called, getdata() function is called and the data is added into the database. Identifies data from unique Food ID; if duplicate is entered, it throws a warning.
“Back To Add Data Page”:- FoodIndex_new: xyz()	When Back To Add Data Page button is pressed, it redirects to the webpage for csv batch upload.
“Show Food Master Table”:- FoodIndex_new(): base_table()	When “Show Food Master Table” is pressed, it redirects to Food Master Table.





CSV Batch Upload

 


Method	Description
“Batch Upload”	When “Add New CSV File” is clicked on Food Master Table, this webpage is shown. Several input fields are shown.
“Submit” button:- FoodIndex_new: file_to_db()	When Submit button is called, file_to_db() function is called and the file is added into the database. Identifies data from unique Food ID; if duplicate is present in file, it throws a warning.
“Add Food”:- FoodIndex_new: addfood()	When Add Food button is pressed, it redirects to the webpage for adding individual item.
“Show Food Master Table”:- FoodIndex_new(): base_table()	When “Show Food Master Table” is pressed, it redirects to Food Master Table.




Update Food Details



Method	Description
“Update Food”: 
Update_form.html	When “Edit” is clicked on Food Master Table, this webpage is shown by rendering update_form.html. Several input fields are shown.
All the fields which are allowed to modify can be modified from here.
“Submit” button:-
                  FoodIndex_new: update_food()	When “Submit” is clicked, the new data gets updates in the database and is immediately reflected in the Food Master Table. The food master table is rendered after submit.

 

Calories Analysis











Method	Description
Reports dropdown>>Calories Analysis
Home_app_new: userfoodlogchart()	Redirects to the User Food Log Charts.
The webpage has date inputs which shows calories consumption from dates recorded in database.






 





Date-wise Calorie Analysis
























Method	Description
“Submit” button:  Home_app_new: userfoodlogchart()
userfoodlogchart.html	Userfoodlogchart() accepts input from “Select From Date”, “Select To Date” and “Select Meal Type”; when “Submit” button is pressed, a line graph is shown representing the calories consumption between the selected date range and selected meal type. Comparison with average calorie consumption for men and women is also shown.
“Calories Analysis for Today”:- Home_app_new: userfoodlogchart()
userfoodlogchart.html	In this block, a pie chart is shown which shows the distribution of calories consumed in present day divided between the consumed items.
“Calories Analysis of Another Date”:-
Home_app_new: otherdayanalysis()
Userdate_form.html	When “Click Here” is clicked, userdate_form.html is rendered and Other Day Analysis page is shown. It has Select Date input and Select Meal Type input.
“Submit” button:  Home_app_new: otherdayanalysis()
userdate_form.html	Otherdayanalysis() function takes  Select Date input and Select Meal Type input and shows a pie-chart which shows the distribution of calories between the food consumed on the particular date.


Consume Comparison










Method	Description
Reports dropdown>>Consume Comparison
Home_app_new: consumeComparison()
consumeComparison.html	Redirects to the Consume Comparison page.
This page shows 2 analysis graphs. First graph is a pie-chart which shows distribution of quantities of nutrients consumed in present day. Second graph is a line chart which shows various line graphs representing nutrients consumed in the recorded dates within the past 7 days.

Purchase Comparison






 
















Method	Description
Purchase Items>>Reports>>Purchase Comparison
Home_app_new: purchaseComparison()
purchaseComparison.html	When Purchase Comparison is clicked, it calls the purchaseComparison() function which renders the purchaseComparison.html file and redirects to Purchase Comparison page. This page has 3 graphs:
1.	Pie-chart that shows nutrient wise distribution of food items purchased today.
2.	Pie-chart that shows nutrient based distribution of food items purchased in last 7 recorded days.
3.	A bar graph that shows comparison b/w User Intake, Overall Intake and Average Intake of nutrients for that particular day. 


 


Method	Description
Chartof()
Templates file-Index.html
Views.py of home_app_new	In this function nuttype variable is used to get nutrition type input eg: carbohydrate,fats etc,.
Dateobj variable for taking dateinput .
With API userlogs from data is taken from date of  dateinput to last 5 days.
User_log dataframe contains all the logs of that particular user.
From another api all the details of the food present in user_log dfataframe is extracted.
Sum them and pass the list to html page
HomeView,Chartdata
Templates file-Index.html
Views.py of home_app_new	Used to present the above the chart


 


 
Method	Description
Purchase_status()
Home_app_view
Purchase_status.html	Select_from and select_to are used to take date inputs
This function extracts the data from the database and gives the output in the form of dataframe  and in the html file it converts dataframe to table
Cosumer_history ()
Home_app_view
Consumer_history.html	Userlog API is called and inputs are passed in that API after that all the content extracted from the API is converted into dataframe format after that the dataframe is passed into consumer_history.html file
context_preprocessors.py (API folder)-For Navbar
Items_left	 
Purchase_left	 
Assorted_left	 





