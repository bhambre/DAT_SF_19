**Brian Hambre**

**12/7/2015**

**DAT_SF_19**

**1.**

BRIANs-MacBook-Air:~ bhambre$ head chipotle.tsv
* order_id  quantity  item_name choice_description  item_price
* 1 1 Chips and Fresh Tomato Salsa  NULL  $2.39 
* 1 1 Izze  [Clementine]  $3.39 
* 1 1 Nantucket Nectar  [Apple] $3.39 
* 1 1 Chips and Tomatillo-Green Chili Salsa NULL  $2.39 
* 2 2 Chicken Bowl  [Tomatillo-Red Chili Salsa (Hot), [Black Beans, Rice, Cheese, Sour Cream]]  $16.98 
* 3 1 Chicken Bowl  [Fresh Tomato Salsa (Mild), [Rice, Cheese, Sour Cream, Guacamole, Lettuce]] $10.98 
* 3 1 Side of Chips NULL  $1.69 
* 4 1 Steak Burrito [Tomatillo Red Chili Salsa, [Fajita Vegetables, Black Beans, Pinto Beans, Cheese, Sour Cream, Guacamole, Lettuce]]  $11.75 
* 4 1 Steak Soft Tacos  [Tomatillo Green Chili Salsa, [Pinto Beans, Cheese, Sour Cream, Lettuce]] $9.25 

BRIANs-MacBook-Air:~ bhambre$ tail chipotle.tsv
* 1831  1 Carnitas Bowl [Fresh Tomato Salsa, [Fajita Vegetables, Rice, Black Beans, Cheese, Sour Cream, Lettuce]] $9.25 
* 1831  1 Chips NULL  $2.15 
* 1831  1 Bottled Water NULL  $1.50 
* 1832  1 Chicken Soft Tacos  [Fresh Tomato Salsa, [Rice, Cheese, Sour Cream]]  $8.75 
* 1832  1 Chips and Guacamole NULL  $4.45 
* 1833  1 Steak Burrito [Fresh Tomato Salsa, [Rice, Black Beans, Sour Cream, Cheese, Lettuce, Guacamole]] $11.75 
* 1833  1 Steak Burrito [Fresh Tomato Salsa, [Rice, Sour Cream, Cheese, Lettuce, Guacamole]]  $11.75 
* 1834  1 Chicken Salad Bowl  [Fresh Tomato Salsa, [Fajita Vegetables, Pinto Beans, Guacamole, Lettuce]]  $11.25 
* 1834  1 Chicken Salad Bowl  [Fresh Tomato Salsa, [Fajita Vegetables, Lettuce]]  $8.75 
* 1834  1 Chicken Salad Bowl  [Fresh Tomato Salsa, [Fajita Vegetables, Pinto Beans, Lettuce]] $8.75 

BRIANs-MacBook-Air:~ bhambre$ wc -l chipotle.tsv
    
    4623 

BRIANs-MacBook-Air:~ bhambre$ grep -i 'chicken burrito' chipotle.tsv | wc -l
     
     553

BRIANs-MacBook-Air:~ bhambre$ grep -i 'steak burrito' chipotle.tsv | wc -l
     
     368

BRIANs-MacBook-Air:~ bhambre$ grep -i 'chicken burrito' chipotle.tsv | grep -i 'black beans' | wc -l
     
     282

BRIANs-MacBook-Air:~ bhambre$ grep -i 'chicken burrito' chipotle.tsv | grep -i 'pinto beans' | wc -l
     
     105

* i. The columns mean Order Number, Item Qty, Item, Ingredients/Flavor, and Total Item Price. Each row is an order of a specific item.
* ii. 1834
* iii. 4623
* iv. chicken(553)
* v. black beans(282)

**2.** 

BRIANs-MacBook-Air:dat_sf_19 bhambre$ find . -name ****.****sv
* ./data/airlines.csv
* ./data/chipotle.tsv
* ./data/drinks.csv
* ./data/hitters.csv
* ./data/housing-data.csv
* ./data/imdb_1000.csv
* ./data/titanic.csv
* ./data/ufo.csv
* ./data/vehicles_test.csv
* ./data/vehicles_train.csv
* ./data/yelp.csv*

**3.** 

BRIANs-MacBook-Air:dat_sf_19 bhambre$ grep -r -i 'dictionary' . | wc -l

5

* 5 occurences

**4.** 
* Chicken Bowl is the most popular food item and bottled water is the most popular drink item. 

BRIANs-MacBook-Air:~ bhambre$ cut -f3 chipotle.tsv | sort | uniq -c | sort
      
   1 Carnitas Salad
   
   1 Chips and Mild Fresh Tomato Salsa
   
   1 Veggie Crispy Tacos
   
   1 item_name
   
   2 Bowl
   
   2 Crispy Tacos
   
   2 Salad
   
   4 Steak Salad
   
   6 Burrito
   
   6 Carnitas Salad Bowl
   
   6 Veggie Salad
   
   7 Carnitas Crispy Tacos
   
   7 Veggie Soft Tacos
   
   9 Chicken Salad
  
  10 Barbacoa Salad Bowl
  
  11 Barbacoa Crispy Tacos
  
  18 Chips and Roasted Chili-Corn Salsa
  
  18 Veggie Salad Bowl
  
  20 Chips and Tomatillo-Red Chili Salsa
  
  20 Izze
  
  22 Chips and Roasted Chili Corn Salsa
  
  25 Barbacoa Soft Tacos
  
  27 Nantucket Nectar
  
  29 Steak Salad Bowl
  
  31 Chips and Tomatillo-Green Chili Salsa
  
  35 Steak Crispy Tacos
  
  40 Carnitas Soft Tacos
  
  43 Chips and Tomatillo Green Chili Salsa
  
  47 Chicken Crispy Tacos
  
  48 Chips and Tomatillo Red Chili Salsa
  
  54 6 Pack Soft Drink
  
  55 Steak Soft Tacos
  
  59 Carnitas Burrito
  
  66 Barbacoa Bowl
  
  68 Carnitas Bowl
  
  85 Veggie Bowl
  
  91 Barbacoa Burrito
  
  95 Veggie Burrito
 
 101 Side of Chips
 
 104 Canned Soda
 
 110 Chicken Salad Bowl
 
 110 Chips and Fresh Tomato Salsa
 
 115 Chicken Soft Tacos
 
 162 Bottled Water
 
 211 Chips
 
 211 Steak Bowl
 
 301 Canned Soft Drink
 
 368 Steak Burrito
 
 479 Chips and Guacamole
 
 553 Chicken Burrito
 
 726 Chicken Bowl

