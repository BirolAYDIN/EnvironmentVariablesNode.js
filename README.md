### Environment Variables With Node.JS

           

Development with **multiple environment variables** quickly becomes difficult to maintain. It would be better if the **environment variables** that we should configure were stored in a central place for the application, such as a file.

           

### Multiple Environments with DotEnv

If we want to configure our application in **different environments**, **dotenv** allows us to define as many environments as we need. Suppose we need to configure 2 basic environments: **development** and **production**.

Then we will create 2 new files **development.env** and **production.env**, one for each environment, which will contain the following configuration:

```.env
// development.env file
	NODE_ENV=development  
	HOST=127.0.0.1  
	PORT=5000
	
// production.env  file
	NODE_ENV=production  
	HOST=localhost  
	PORT=8000
```

We can try three different environments
```bash
	npm run test
	
	# NODE_ENV=development
	# App listening on  http://localhost:8000 
```
```bash
	npm run dev
	
	# NODE_ENV=development
	# App listening on http://127.0.0.1:5000
```
```bash
	npm run prod
	
	# NODE_ENV=production
	# App listening on http://localhost:8000
```