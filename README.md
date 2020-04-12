# Introduction to the JAMstack

This is the code for a Frontend Masters workshop. In this workshop, we’ll learn what the JAMstack is, what it’s capable of, and how we can use it to build full-featured apps with less complexity and overhead.

### Create a DB-Backed Todo App

#### Set up a database

- Create a Fauna account (https://fauna.com)
- Write a GraphQL schema (`functions/utils/todos.gql`)
- Create a new Fauna DB (https://dashboard.fauna.com/db-new/)
- Upload the GraphQL schema to Fauna
- Explore the GraphQL Playground in Fauna
- Create a todo item in the playground
- Read all todos in the playground

#### Add a function to get all todos

- Create an API server key in the “security” tab
- Add the server key to `.env`
- Install deps `yarn add axios dotenv`
- Create a helper for serverless functions (`functions/utils/send-query.js`)
- Create a serverless function `/functions/get-all-todos.js`
- Add a `netlify.toml` to define where functions live and set up redirects
- Test the function

#### Create a Gatsby site as the app front-end

- Install deps `yarn add gatsby react react-dom`
- Create a `gatsby-config.js` to trigger Netlify’s auto-detection
- Create an index page
- Write a hook to load todos
- Create a `Todo` component to display todo items

#### Add the ability to create todos

- Create a serverless function `/functions/create-todo.js`
- Create a `Form` component
- Reload todos when a new one is created

#### Add the ability to toggle todo completed state

- Create a serverless function `/functions/toggle-completed.js`
- Add a checkbox input to show completed state and handle toggling
- Reload after a todo is toggled

#### Add the ability to delete todos

- Create a serverless function `/functions/delete-todo.js`
- Add a button to delete todos
- Reload after a todo is deleted
