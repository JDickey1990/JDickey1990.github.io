---
layout: post
title:      "Mod 2 Sinatra Project-CryptoInvestments"
date:       2020-10-23 20:14:42 +0000
permalink:  mod_2_sinatra_project-cryptoinvestments
---


Building a Sinatra Application has really been an incredible way to solidify the many concepts covered in the module. After skipping the planning phase in my Mod 1 project and stumbling through design flaws, I decided to take my time in the beginning of this project and really try to think through what I wanted to create and how the layout and flow through the app should be set up. Using wireframing and the project planning resources proved to be very helpful for me.

 Once I had an idea of what I wanted to do and how it should function I used the corneal gem to set up the file structure for my Sinatra project as well as scaffolding for the routes I would need to create. 
I set up my database with rake db:create_migration entering in the separate names of my tables to create a user’s table as well as a coins table. The create migration command created files in my migrations folder creating_users.rb and creating_coins.rb which I completed with the attributes that I desired for each. 

I realized during wireframing that by using ORM my  Coin model would belongs_to :user and the User model has_many :coins so I made sure to add a foreign key into the coins table by adding the user_id and added in password_digest to the users table so I could use the bcrypt gem to salt and hash users passwords with encryption as well as authenticate them during login. I then built the user and coin models to include the macros listed above which would establish the associations between the two and included the line has_secure_password in the user model. 

The next step in my project was migrating my database and using tux to create and play around with crud functionality for the user and coin objects. When I felt comfortable that my associations were working correctly, I decided to move forward. 

Before getting too much further in the process I made sure to check that corneal mounted my user and coins controller with the use keyword and set the application controller to run. This was already done but I did add in a line to use Rack::MethodOverride so my update and delete functionality would be able use patch and update or delete data in my database.

Application controller was the next stop to enable :sessions and set :session_secret. Accessing the session hash would be crucial for me to log in and out a user as well as storing user’s data while they are logged into the application. 
At this point I felt pretty comfortable with the M(models) portion of my MVC framework so I began working on my routes or C(controllers) that act as an intermediary between the user which is interfacing with the view and sending to and receiving information from the models which is interfacing with the models and database on the back end of the application. 

Get and Post signup were the first routes I created followed by login and the user index. Once these were completed, I moved on to creating a new coin object and showing it, editing a coin object and redirecting back to the show page to display the changes made and then deleting an object which would redirect back to the index and show that it had been removed. 

I have to be totally honest I was absolutely thrilled to see the code I was writing take shape in my web browser and I had to refrain on multiple occasions from going down the proverbial rabbit hole with styling until I was able to complete the requirements of my project. 

Minimum Viable Product is one of the most important acronyms I have learned so far and kept me focused on setting up my V(views) to display the information I needed correctly. That being said, the moment the MVC framework was complete and I had met all of the CRUD requirements I decided to dig into styling my views with some added CSS classes and images and build some added functionality in for users as well as coins. 

This project was a blast and I felt it really forced me to think through the many concepts we covered in this MOD as well as be creative in conceptualizing how to navigate through the application. I am more excited than ever to be in this program and can not wait to learn what comes next. 

