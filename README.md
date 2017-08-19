# Running website/server

```
npm install

mongoimport -d ttdb_sample -c users sample_data/users.json
mongoimport -d ttdb_sample -c restaurants sample_data/restaurants.json
mongoimport -d ttdb_sample -c menus sample_data/menus.json
mongoimport -d ttdb_sample -c meals sample_data/meals.json
mongoimport -d ttdb_sample -c reviews sample_data/reviews.json

npm start
```

Navigate to http://localhost:3000

# Directory Structure

```
/app                    #all code is in here
/app/app.js             #main entry point to server
/app/app.models.js      #all models init/boilerplate code
/app/app.mongo.js       #all mongo init/boilerplate code
/app/app.router.js      #all router init/boilerplate code

/app/public             #public resource folder
/app/public/index.ejs   #container for all pages (includes, navs, links, etc here)
/app/public/assets      #all css/imgs/downloaded libs
/app/public/pages       #main pages
/app/public/partials    #reused page elements (e.g. menu item)
/app/public/services    #reusable services/containers for all AJAX calls

/app/<feature>          #folder for routes/models needed for a feature to work

/sample_data            #some sample data to start out with
```

# Assets

Assets borrowed from online
- font-awesome (icon pack)

Custom made assets
- minimal-form (custom minimal design for forms)
- ratings (5-star ratings, design and functionality)
- cards (material design inspired cards)
- buttons (custom button styles)

# Pages

Home
- cover
- search results (did not implement)
- map

Restaurant
- restaurant photo
- restaurant info (name, location, ratings)
- restaurant menus

Meal Info
- meal photo
- meal info (name, restaurant, ratings)
- reviews
- review submit

Sign up/in
- sign in form
- sign up form

User profile (customer vs business owner)
- user information
- user reviews
OR
- business owner info
- restaurants owned

Account Management (customer vs business owner)
- form to modify user info
- form to delete account

# Breakpoints

0px <= A < 800px <= B < 1280px <= C

- A: mobile/small display
- C: medium display
- D: large display
