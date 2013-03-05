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

### Option 2 

 1. Go to http://java.heroku.com/
 2. Create a "Containerless web app with Embedded Jetty"
 3. Clone the Heroku App you created
  
 ```
 $ git clone -o heroku git@heroku.com:intense-plateau-3730.git
 ```

## Setup the application

  Option 1 of Heroku directory: /home/mhenke/git/heroku/railo
  Option 2 of Heroku directory: /home/mhenke/git/heroku/intense-plateau-3730  

 1. Download the heroku-railo project and unzip into your Heroku directory:
   - This command is ran beneath the Heroku directory: /home/mhenke/git/heroku

 ```
 $ sudo wget -qO- -O tmp.zip https://github.com/mhenke/heroku-railo4/archive/master.zip && unzip -qd . tmp.zip && rm -f tmp.zip && cp -R heroku-railo4-master/* railo && rm -r heroku-railo4-master
 ```

## Running the application
 1. First build with in the heroku directory:

 ```
 $ mvn clean package
 ```

 1. Then run it with:
   
 ```
 $ java -cp target/classes:target/dependency/* com.example.Main
 ```
	
 1. Then see your app at http://localhost:8080
 
 1. Initial initalize git, add, and commit changes

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
