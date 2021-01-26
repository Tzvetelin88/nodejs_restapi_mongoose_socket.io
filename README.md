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


