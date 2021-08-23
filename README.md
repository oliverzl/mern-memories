This is a full CRUD MERN App with authentication and JWT.

when deploying:

Frontend: Netlify
Backend: Heroku

when deploying to heroku, do not hide the CONNECTION_URL of the .env file. only gitignore the .env file when pushing to Github, AFTER pushing build to heroku.
in frontend, during development, api/index.js needs to point the URL localhost:5000. during deploy, we will change the URL to the heroku app URL, so that the netlify frontend react app knows to connect to that URL instead of localhost:5000
.

during development:

change the API URL in api/index.js back to localhost:5000.
Make sure .env variables are accessible.

when ready to deploy:
push server to heroku to deploy first,
change URL in api/index.js back to the heroku URL to let the frontend connect to the live deployed server, then npm run build and drop the build folder into Netlify.
