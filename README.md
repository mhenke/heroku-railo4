# Railo4 on Heroku

This is a demo app running Railo4 on Heroku

## Create the application
 1. Go to http://java.heroku.com/
 1. Create a "Containerless web app with Embedded Jetty"

## Setup the application
 1. Clone the Heroku App you created
 ```
 $ git clone -o heroku git@heroku.com:protected-reef-1480.git
 ```

  Example of Heroku directory: /home/mhenke/git/heroku/intense-plateau-3730/src

 1. Copy the items of the heroku-railo project into your Heroku directory:
 ```
 $ git clone git://github.com/mhenke/heroku-railo4.git
 ```

  Example of heroku-railo project directory: /home/mhenke/heroku-railo4

## Running the application
 1. First build with in the heroku directory:
 ```
 $ mvn clean package
 ```

 1. Then run it with:
   
 ```
 $ java -cp target/classes:target/dependency/* com.example.Main
 ```
	
 1. Then see your app at:
 
 http://localhost:8080

## Deploying the application
 1. Deploy and see the live demo app at:
 ```
 $ git add .
 $ git commit -m "first commit to heroku"
 $ git push heroku master
 $ heroku open
 ```

 http://sleepy-depths-6628.herokuapp.com/

# Thanks
  I have to thank Denny (denny@getrailo.com) for helping me figure out the railo repository	

# References:
## How to run the jetty embedded server:
  http://wiki.eclipse.org/Jetty/Tutorial/Embedding_Jetty#Creating_a_Server
## Install Railo on Jetty:
  http://wiki.getrailo.org/wiki/installation:jetty
## URL Rewrite:
  http://tuckey.org/urlrewrite/	
## Git Related (Examples):
```
$ git remote add heroku git@heroku.com:project.git
$ git remote rm heroku
```	
http://edgar.tumblr.com/post/12610398221/how-to-link-your-git-project-with-an-existing-heroku
## Heroku
### Java on Heroku
  http://java.heroku.com/
### Getting Started with Java on Heroku 
  https://devcenter.heroku.com/articles/java
### Getting Started with Heroku & Eclipse
  https://devcenter.heroku.com/articles/getting-started-with-heroku-eclipse
