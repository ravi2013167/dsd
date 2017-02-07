# Course code for Udacity's Implementing Web Security with OAuth 2.0 class.
![oauth](https://cloud.githubusercontent.com/assets/19377159/15414488/86f80b9e-1e58-11e6-9f11-b760b605bac3.png)

## Application Overview
A simple restaurant menu application that provides a list of items within a variety of categories as well as provides a user registration and authentication system. Registered users will have the ability to post, edit and delete their own items.

Uses:
- OAuth 2.0 framework to allow users to securely login to the web application. 
- Google+ Sign-In and Facebook Login in options so users can create restaurant menus that are viewable by everyone but only modifiable by the original creator.

# Local Development


## Dependencies

**VirtualBox**

https://www.virtualbox.org/

**Vagrant**

https://www.vagrantup.com/

**SQL Alchemy**

http://www.sqlalchemy.org/

**Flask**

http://flask.pocoo.org/


## Setup

Set up VirtualBox and Vagrant to create your own server. With Vagrant installed, run:

```
$ vagrant up
$ vagrant ssh
$ cd <SYNCED PATH TO REPOSITORY>
$ pip install -r requirements.txt
```

Initialize and fill the database with these scripts.

```
$ python database_setup.py
$ python lotsofmenus.py
```

## Run

Run the web app finalproject.py:

```
$ python project.py
```

The app runs on port `5000`:

```
http://localhost:5000/

```



## REST API Endpoints

Available in JSON and XML at the following endpoints:

List all restaurants:

```
https://ani-udacity-oauth-project.herokuapp.com/restaurant/JSON
```

List all menu items for a given RESTAURANT_ID:

```
https://ani-udacity-oauth-project.herokuapp.com/restaurant/<RESTAURANT ID>/menu/JSON
```

List a single menu item:

```
https://ani-udacity-oauth-project.herokuapp.com/restaurant/<RESTAURANT ID>/menu/<ITEM ID>/JSON
```
