# Lab 12: Componentization and HTML5 Forms

## Configuration

_Your repository must include the following config files:_

- `.env` - with your PORT and DATABASE_URL. Make sure this file is included in your `.gitignore`
- `README.md` - with documentation regarding your lab and it's current state of development. Check the "documentation" section below for more details on how that should look **AT MINIMUM**
- `.gitignore` - with standard NodeJS configurations
- `.eslintrc.json` - with Code 301 course standards for the linter
- `package.json` - with all dependencies and any associated details related to configuration
- Note that the `package-lock.json` file is automatically created when dependencies are installed and ensures that future installations of the project use the same versions of the dependencies.
Use the following as a guide for your directory structure.

```sh
book_app (repository)
├──public
│  ├── js
│  │   └── app.js
│  └── styles
│      ├── base.css
│      ├── fonts
│      │   ├── icomoon.eot
│      │   ├── icomoon.svg
│      │   ├── icomoon.ttf
│      │   └── icomoon.woff
│      ├── icons.css
│      ├── layout.css
│      ├── modules.css
│      └── reset.css
├──views
│  ├── layout
│  │   ├── footer.ejs
│  │   ├── head.ejs
│  │   └── header.ejs
│  └── pages
│      ├── error.ejs
│      ├── index.ejs
│      ├── books
│      │   ├── detail.ejs
│      │   └── show.ejs
│      └── searches
│          ├── new.ejs
│          └── show.ejs
├── .env
├── .eslintrc.json
├── .gitignore
├── package-lock.json
├── package.json
├── README.md
└── server.js
```

## User Acceptance Tests

### Overview

For today's assignment, you will be adding the ability for a user to select a book from the API search results and add it to their collection, which will be persisted in a PostgreSQL database. Then, when a user navigates to the home page of the application, all of the books will be retrieved from the database and displayed on the screen. The API search form will be accessible through the menu.

You will also be adding a detail view where a user can view the description, ISBN, and current bookshelf of a single book from the collection.

### Time Estimate

For each of the features listed below, make an estimate of the time it will take you to complete the feature, and record your start and finish times for that feature:

```
Number and name of feature: ________________________________

Estimate of time needed to complete: _____

Start time: _____

Finish time: _____

Actual time needed to complete: _____
```

Add this information to your README.

Note that there are a lot of features in today's lab assignment. If you do not complete all of the features today, submit what you have and carry over the remaining features to the next lab session. You can continue to work on any incomplete features, then move on to implementing the lab 13 features.

### Database configuration

- You will be creating a table in which to store each book added by the user. Create a schema for your books table. If you would like to, you can make a file in your repo called `books.sql` which contains SQL queries for setting up your table.
- This schema should contain the following properties:
  - `id` as the primary key
  - `author`
  - `title`
  - `isbn`
  - `image_url`
  - `description`
  - `bookshelf`
- Use Postman to request book data from the Google Books API. For example, you can enter a search query at the end of this route: `https://www.googleapis.com/books/v1/volumes?q=`
- Use the search results to determine the data types of each field in your table. Note that the `bookshelf` value will be manually entered by the user and should not directly reflect a specific piece of data returned from the Google Books API.
- For reference, here is a sample from the API:
```json
  {
    "title": "Dune",
    "author": "Frank Herbert",
    "isbn": "ISBN_13 9780441013593",
    "image_url": "http://books.google.com/books/content?id=B1hSG45JCX4C&printsec=frontcover&img=1&zoom=5&edge=curl&source=gbs_api",
    "description": "Follows the adventures of Paul Atreides, the son of a betrayed duke given up for dead on a treacherous desert planet and adopted by its fierce, nomadic people, who help him unravel his most unexpected destiny."
  }
```
- Within your PostgreSQL shell, create a new database named `books_app`.
- Execute the SQL commands to create a new table in your database called `books` according to your schema.
  - If you chose to write a `books.sql` file to create your table, you can load it into your Postgres database from the terminal command line:
    - `psql books_app -f /path/to/books.sql`
- Add at least two books to your database, with bookshelf info. 
- Make sure that your schema is properly documented in your book app repository's main `README.md` file. If you made a schema file, make sure it is added, commited, and pushed to GitHub.
- In your Heroku instance, provision a Postgres database.
- Migrate your local database to Heroku, using the following format for your command: `heroku pg:push books_app DATABASE_URL --app <partner 1 initials>-<partner 2 initials>-booklist`
  - _Note: Unless the local database is pushed to Heroku again, any changes to the local database will not be reflected in the production database._
  
### Feature Tasks

See the Trello board for your feature tasks for today's lab.

## Documentation

_Your `README.md` must include:_

```md
# Project Name

**Author**: Your Name Goes Here
**Version**: 1.0.0 (increment the patch/fix version number if you make more commits past your first submission)

## Overview
<!-- Provide a high level overview of what this application is and why you are building it, beyond the fact that it's an assignment for a Code Fellows 301 class. (i.e. What's your problem domain?) -->

## Getting Started
<!-- What are the steps that a user must take in order to build this app on their own machine and get it running? -->

## Architecture
<!-- Provide a detailed description of the application design. What technologies (languages, libraries, etc) you're using, and any other relevant design information. -->

## Change Log
<!-- Use this area to document the iterative changes made to your application as each feature is successfully implemented. Use time stamps. Here's an examples:

01-01-2001 4:59pm - Application now has a fully-functional express server, with GET and POST routes for the book resource.

## Credits and Collaborations
<!-- Give credit (and a link) to other people or resources that helped you build this application. -->
-->
```

## Submission Instructions

- Continue working in the same repository from the previous class.
- Continue to work on semantically-named non-master branches.
- Complete your Feature Tasks for the day (below)
- Create a Pull Request (PR) back to the `master` branch of your repository
- On Canvas, submit a link to your PR and a link to your deployed application on Heroku. **Make sure to include the following:**
  - A question within the context of today's lab assignment
  - An observation about the lab assignment, or related 'Ah-hah!' moment
  - How long you spent working on this assignment
