# Heroku Deployment

**Resources:**
1. https://devcenter.heroku.com/articles/getting-started-with-nodejs 
2. https://howtonode.org/deploy-blog-to-heroku

## Getting Started on Heroku with Node.js

1. `brew install heroku/brew/heroku`
    - We have to install Heroku first. (run this command from Terminal (Mac OS))
2. `heroku login`
    - Command opens your web browser to the Heroku login page
3. `heroku create`
    - Command creates an app on Heroku, which prepares Heroku to receive source code
4. `git push heroku main`
    - Command deploys your code
5. `heroku ps:scale web=1`
    - Command ensures that at least one instance of the app is running
6. `heroku open`
    - Command allows to visit deployed app

### View logs

**Heroku** treats logs as streams of time-ordered events aggregated from the output streams of all your app and Heroku components, providing a single channel for all of the events.

1. `heroku logs --tail`
    - Command allows to view information about running app

### Define a Procfile

Use a [Procfile](https://devcenter.heroku.com/articles/procfile), a text file in the root directory of your application, to explicitly declare what command should be executed to start your app.

1. `web: npm start`
    - Command declares a single process type, **web**, and the command needed to run it.

### Scale the app

Right now, your app is running on a single web [dyno](https://devcenter.heroku.com/articles/dynos). We can think of a dyno as a lightweight container that runs the command specified in the Procfile.

1. ` heroku ps`
    - Command checks how many dynos are running
    - By default, app is deployed on a free dyno. Free dynos will sleep after a half hour of inactivity (if they don’t receive any traffic)

2. `heroku ps:scale web=0`
    - Scaling an application on Heroku is equivalent to changing the number of dynos that are running.

### Run the app locally

1. `heroku local web`
    - Just like Heroku, heroku local examines the Procfile to determine what to run.
    - [http://localhost:5000](http://localhost:5000) (app should run locally)

### ACP for Heroku

1. `git add .`
2. `git commit -m " "`
3. `git push heroku main`