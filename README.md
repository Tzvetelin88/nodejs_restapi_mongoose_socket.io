# nodejs_restapi_mongoose_socket.io
Nodejs RestAPI Application with Express, MongoDB, Mongoose and WebSocket integration.

## External npm:

 - Crеate free account with MongoDB Atlas (https://account.mongodb.com/)
 - User Mongoose as syntax sugar.
 - Create Routes, Models and Controllers.
 - Validate requests with epxress validator.
 - Add authentication and validate with JWT

## Using: 

 -  express           - https://expressjs.com/en/api.html
 -  mongoose          - https://mongoosejs.com/docs/documents.html
 -  MongoDB Cloud     - https://account.mongodb.com/
 -  express-validator - https://express-validator.github.io/docs/   
 -  socket.io         - https://socket.io/docs/v3/index.html
 -  jsonwebtoken      - https://github.com/auth0/node-jsonwebtoken#readme
 -  multer            - https://github.com/expressjs/multer#readme

## Two Routes: 
``` 
   /feed
   /auth 
```

## API Endpoints:
```
/feed
	router GET: 
		'/posts'
		'/post/:postId'
		
	router POST: 
		'/post'
		
	router PUT:
		'/post/:postId'

	router DELETE:
		'/post/:postId'

/auth
	router PUT:
		'/signup'
	router POST:
		'/login'
	router GET:
		'/status'
	router PATH:
		'/status'
```


Front-end Application with React to access Nodejs RestAPI will come soon too...


# P.S.
## Still you can use the new ECMA syntax to import/export, but be aware that many are still Experimental, depends of the version of Nodejs:
 - v.15 https://nodejs.org/api/esm.html
 - v.14 https://nodejs.org/docs/latest-v14.x/api/esm.html

Some examples in our project:
```
// New syntac to import
import path, { dirname } from 'path'
import { fileURLToPath } from 'url'
import express from 'express'
import bodyParser from 'body-parser'
import mongoose from 'mongoose'
import multer from 'multer'

import { default as feedRoutes } from './routes/feed.js'
import { default as authRoutes } from './routes/auth.js'

// Because of the new syntax of Ecma, the do not support __filename or __dirname as global variables
// Read more: https://nodejs.org/docs/latest-v15.x/api/esm.html
// !!!! Some features are still experimental  !!!!
// We need to construct it in more long way....
const __filename = fileURLToPath(import.meta.url);
const __dirname = dirname(__filename);

// Old imports before type: module in package.json
// const path = require('path');
// const express = require('express');
// const bodyParser = require('body-parser');
// const mongoose = require('mongoose');
// const multer = require('multer');

// const feedRoutes = require('./routes/feed');
// const authRoutes = require('./routes/auth');
```