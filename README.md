# theTasters

A food/restaurant rating website project (i.e. Yelp clone) done for educational purposes in a group of three over the course of a couple of months.

With regards to this README, below are setup instructions, project directory structure, and a list of pages with screenshots.

# Instructions for running website/server

Node.js (and npm) are required for this server to run. Furthermore, mongodb might require some setup on your system. It's also possible there are other dependencies missing on your system, so some debugging/setup might be needed. In any case, this is how I run the server:

### Terminal 1
```
mkdir data
mongod --dbpath data
```

### Terminal 2
```
mongoimport -d ttdb_sample -c users sample_data/users.json
mongoimport -d ttdb_sample -c restaurants sample_data/restaurants.json
mongoimport -d ttdb_sample -c menus sample_data/menus.json
mongoimport -d ttdb_sample -c meals sample_data/meals.json
mongoimport -d ttdb_sample -c reviews sample_data/reviews.json

npm install
npm start
```

Navigate to http://localhost:3000 on your browser.

# Project directory Structure

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

# Pages and page functionality/features

Home
- cover/launch page
- search results (not fully implemented - just populates all restaurants)
- map (responsive to search, but not connected to restaurants listed)

![alt text](http://i.imgur.com/kiADvaw.jpg)

Restaurant
- restaurant photo
- restaurant info (name, location, ratings)
- restaurant menus

Meal Info
- meal photo
- meal info (name, restaurant, ratings)
- reviews listed
- ability to submit review (assuming logged in)

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
