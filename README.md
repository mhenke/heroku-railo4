# Railo4 on Heroku

This is a demo app running Railo4 on Heroku

## Create the application
### Option 1
 1. Create a directory and create heroku app

 ```
 $ mkdir railo
 $ cd railo
 $ heroku create
 ```

## Setup the application

 - Heroku directory: /home/mhenke/git/heroku/railo

 1. Download the heroku-railo project and unzip into your Heroku directory:
   - This command is ran beneath the Heroku directory in /home/mhenke/git/heroku

 ```
 $ sudo wget -qO- -O tmp.zip https://github.com/mhenke/heroku-railo4/archive/master.zip && unzip -qd . tmp.zip && rm -f tmp.zip && cp -R heroku-railo4-master/* railo && rm -r heroku-railo4-master
 ```

## Running locally and Deploying the application
 1. First build with in the heroku directory:

 ```
 $ mvn clean package
 ```

 1. Then run command below and see your app at http://localhost:8080
   
 ```
 $ java -cp target/classes:target/dependency/* com.example.Main
 ```

 1. Initialize git, add, and commit changes

 ```
 $ git init
 $ git add .
 $ git commit -m "first commit to heroku"
 ```

 1. Deploy and see the live demo app at:

 ```
 $ git push heroku master
 $ heroku open
 ```

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
