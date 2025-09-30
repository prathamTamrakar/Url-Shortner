# Url-Shortner

A simple URL shortener web application / service.

## Table of Contents

- [About](#about)  
- [Tech Stack](#tech-stack)  
- [Features](#features)  
- [Installation & Setup](#installation--setup)  
- [Usage](#usage)  
- [API Endpoints](#api-endpoints)  
- [Folder Structure](#folder-structure)

## About

This project provides a service to convert long URLs into short, easily shareable links, and redirect users from those short links to the original long URLs.

## Tech Stack

- Node.js / Express  
- EJS
- MongoDB
- Mongoose

## Features

- Shorten a given long URL  
- Redirect from short URL to original URL  
- Count / track usage or visits (optional)  
- Handle invalid / malformed URLs gracefully  
- Web interface (form to enter URL)  
- API (for programmatic use)  

## Installation & Setup

1. Clone the repository  
   ```bash
   git clone https://github.com/prathamTamrakar/Url-Shortner.git
   cd Url-Shortner
   ```
2. Install dependencies
   ```bash
   npm install
   ```
3. Create/configure environment variables
   Example .env file:
   ```
   PORT=3000
   MONGODB_URI=your_mongo_connection_string
   BASE_URL=http://localhost:3000
   ```
4. Start the server
   ```bash
   npm start
   ```
5. Visit in browser
    Open http://localhost:8001 and use the UI to shorten URLs

## Usage

- Enter a long URL in the form  
- Submit → get a shortened URL  
- Use / click the shortened URL → you’ll be redirected to the original URL  
- (If tracking is implemented) see stats/visits for each short URL  

## API Endpoints

Here are example endpoints if your service exposes an API:

| Method | Endpoint            | Description                       |
|--------|---------------------|-----------------------------------|
| POST   | `/url`      | Create a new short URL           | 
| GET    | `/url/:shortId`         | Redirect to the original long URL |
| GET    | `/url/analytics/:shortId` | Get usage stats (if supported)   |
|POST|`/user/`|User Signup|
|POST|`/user/login`|User login|

You can modify / extend these as needed.


## Folder Structure
```
Url-Shortner/
├── controller/
├── middleware/
├── models/
├── routes/
├── service/
├── views/
├── index.js
├── connect.js
├── package.json
├── .gitignore
└── README.md
```





