---
layout: post
title:      "AnimeWeeb! (Sinatra Project)"
date:       2020-02-16 21:10:17 +0000
permalink:  animeweeb_sinatra_project
---


As our second module and project come to a close, I take a retrospective look on everything we've learned up until this point. I'm actually started to process how much time has gone by and how much we are learning. Everything has been moving so fast, that sometimes I don't stop and look back. There are days where I feel like I'm a developer, there are days where I dont'. I think I can now actually say that I feel like a programmer! 


### About the Project

My application is called AnimeWeeb! Anime is probably one of my favorite things ever. I talked a lot about it (maybe too much), so I thought it would be fun to create an application around that, which is actually what I did. With AnimeWeeb, you are able to signup and keep track of your favorite animes'. You are able to leave a review, along with a rating and the streaming service you use. You also can look at other peoples' favorite animes' and what they think. So if you are running out of something to watch, you can always log in and see something new!


### How does it all work?! (Challenges faced).

I think one of the biggest challenges I faced was "WHERE DO I START?!" I honestly had no idea how I wanted it to look, the flow of the application itself, there were so many things running throught my mind. So, I decided I should just start with the basics and get a simple and functional application running. These were the major requirements for the project:

* Build a has-many & belongs-to relationship between models
* Build a user authentication system
* Build an app with one resource having full C.R.U.D. functionality 

And so, that is exactly where I started. My Application has two models: my **Users** model and my **Show** model. A User "has-many" shows and a Show "belongs-to" a user. Once I had the basic idea of how I wanted my application to run, I started out with these 3 lovely gems.

* Sinatra (Domain Specific Language to Ruby for creating web applications).
* ActiveRecord (Used for mapping database tables to Ruby classes).
* Corneal (a ruby gem created by a fellow Flatiron student to help us with our Sinatra apps).

Having access to these 3 gems made all the difference when it came to setting up my environment. I had so much trouble doing that and creating a relationship between my models! But know that is a thing of the past! Another issue I had was the structure of my views.... but with the help of corneal, that was taken care of as well.

My application has 3 controllers as well:
1. Application Controller (which inherits from Sinatra::Base allowing me to use all the awesome functions Sinatra has).
2. User Controller (which has all my login/signup routes for my application).
3. Show Controller (The controller with full CRUD functionality. Allowing you to create, read, update and delete shows).

#### For the Future...

This is where I finally feel like I'm finally becoming a programmer. I learned so much from the two weeks alone working on this project.... and I know I'm only scratching the surface. I am excited for what is to come. The ups and downs, the frustrations, the victories, and the losses. There is so much more I want to add to this project. After a few more months in Rails and JS, I will definitely add more functionality to this thing. Maybe mess around with the CSS some more (that was a lot of fun). 

For all of you that have gotten to this point, don't give up! Keep going and surround yourself with people you are going to uplift you and encourage you. I wouldn't be this far if it wasn't for my amazing lead cohort and a few others in my cohort whom I talk to everyday! 



