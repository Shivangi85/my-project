# my-project
# EatEasy
EatEasy is your go-to platform for ordering food online from your favorite restaurants, hassle-free.
## Getting Started
These are the instructions to clone and run this project in your local machine for developement and testing purpose

### Prerequisites

* Node
* Git
* MongoDB
- Node
- Git
- MongoDB

### Installation

1. First of all, Clone this repository & navigate to the directory

```
git clone https://github.com/chiragverma11/EatEasy_Food_Ordering_Website.git
cd EatEasy_Food_Ordering_Website
```

2. Install the Dependencies 
2. Install the Dependencies

```
npm install
```

### Running Locally

* First Create `.env` file in root directory using the following content and make changes if required.
- First Create `.env` file in root directory using the following content and make changes if required.

```
PORT=8080
mongoURI="YourMongoDBuri"
MONGO_URI="YourMongoDBuri"
TOKEN_SECRET="JwtSecret"
```

- Starting the Server

* Starting the Server
```
npm start 
npm start
```

or

```
npm run dev 
npm run dev
```

### Adding Food Items to Database Collection (Menu)
@@ -53,6 +56,7 @@ To add food items to database run
```
npm run menu
```

Edit `items.csv` file under `assets/csv` to change food items.

## Author
@@ -61,8 +65,8 @@ Edit `items.csv` file under `assets/csv` to change food items.

## Built Using

* [NodeJS](https://nodejs.org/en) - Server
* [Express](https://expressjs.com/) - Server Framework
* [MongoDB](https://www.mongodb.com/) - Database
* [Mongoose](https://mongoosejs.com/) - Object Modeling & Schema
* [EJS](https://ejs.co/) - Template Engine
- [NodeJS](https://nodejs.org/en) - Server
- [Express](https://expressjs.com/) - Server Framework
- [MongoDB](https://www.mongodb.com/) - Database
- [Mongoose](https://mongoosejs.com/) - Object Modeling & Schema
- [EJS](https://ejs.co/) - Template Engine
  2 changes: 1 addition & 1 deletion2  
server.js
Original file line number	Diff line number	Diff line change
@@ -12,7 +12,7 @@ app.use(cookieParser());
//Mongoose Connection
const database = async () => {
  await mongoose
    .connect(process.env.mongoURI, {
    .connect(process.env.MONGO_URI, {
      useNewUrlParser: true,
      useUnifiedTopology: true,
    })
  2 changes: 1 addition & 1 deletion2  
utils/itemImport.js
Original file line number	Diff line number	Diff line change
@@ -6,7 +6,7 @@ require("dotenv").config({ path: path.resolve(__dirname, "../.env") });

//Mongoose Connection
mongoose
  .connect(process.env.mongoURI, {
  .connect(process.env.MONGO_URI, {
    useNewUrlParser: true,
    useUnifiedTopology: true,
  })
