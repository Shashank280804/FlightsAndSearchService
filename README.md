# Welcome to Flights service

# Project setup

- Clone the project on your local.
- Execute `npm install` on the same path as of your root directory of the downloaded project.

- Create a `.env` file in the root directory and add the following environment variable
  `PORT=3000`

- Inside the `src/config` folder create a new file `config.json` and then add the following piece of json

...
{
"development": {
"username": <YOUR_DB_LOGIN>,
"password": <YOUR_DB_PASSWORD>,
"database": "Flights_Search_DB_DEV",
"host": "127.0.0.1",
"dialect": "mysql"
},

}

...

-Once you've added your db config as listed above,go to the src folder from your terminal and execute `npx sequelize db:create`

- To create a new model
- `npx sequelize model:generate --name Airport --attributes name:String,cityId:integer`

after new model created
`npx sequelize db:migrate`

seeders help you to add some static and intial values to the data so that we have something to start with
--adding add airport seed
`npx sequelize seed:generate --name add-airports`
