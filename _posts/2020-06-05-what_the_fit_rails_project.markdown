---
layout: post
title:      "What The Fit (Rails Project)"
date:       2020-06-05 21:11:47 +0000
permalink:  what_the_fit_rails_project
---


Here we are, at the end of my third project! It has been a whirlwind of emotions. So much has happened within the last few months while work on Rails, from Covid-19 happening and switching from a part-time to a full-time cohort. I still cannot believe that I started this wonderful program in October of last year, it still does not feel real. It has been 7 months of triumph, confusion, and accomplishments. I feel like I always say this, but there are many times where I do not feel like a developer, and there are times that I do. I feel like that is something that as programmers, we will always struggle with. Overall, I am happy with the place that I am in. I have learned so much information and have met some amazing people that I now consider friends along this journey.

### My project

My project is called What The Fit! It is a client management application specifically for fitness trainers! Trainers can sign up and then log into their accounts and can immediately start keeping track of the clients and their associated appointments so that trainers do not have to worry about losing track of their schedules! Fitness have always been a huge part of my life. At one point, I wanted to become a fitness trainer (until I found out about Flatiron of course). So, I thought creating an application like this could be of genuine help to those who can sometimes forget who their clients are and when the appointments are!

### Challenges faced

As much as I enjoyed creating this application, for me, this one has probably been the toughest thus far. Everyone is not kidding when they mention that Rails is all about convention. In order for everything to work properly, you need to make sure that all of your controllers actions, models, and views are named accordingly. 

1. Nested Forms

This was probably my biggest challenge. My associations were as follows; 

```
Trainer
has_many :appointments
has_many :clients, through: :appointments 
```
```
Client
has_many :appointments
has_many :trainers, through: :appointments
```
```
Appointment
belongs_to :trainer, optional: true 
belongs_to :client, optional: true
```

So I had to create a nested form with my clients and appointments because if I were to just create a client by itself, it would never show up on my trainers show page. I need to create an appointment at the same time as the client for the :ids to be assigned and for it to show up on my trainers page. For some reason, after I would create the client with its associated appointment, I would get a `appointment trainer id needed` error. I spent about two days trying to figure it out when Corinna and I finally figured out that we needed to explicitly whitelist the trainer id into the appointments strong params. 

2. Nested Routes

This was another big issue of mine. Especially when it came to url helpers. When I would use `link_to` with the url helpers, for some reason, it was really hard for me to grasp the concept of which helper to use where and when to pass in an instance variable as an argument. Using `rake routes` was a huge help and I finally got to the point where I did not need to look at it as much. Another great rule of thumb for when to pass in an arguement to a helper: **For every :id in the url, you need an associated instance variable arguement.** For example, if your url is `trainer/1/clients`, you will need to pass in that trainer variable so that Rails knows where to go after you have clicked on the link.


### For the future....

This is definitely a project I want to come back to and clean up. I feel there are so many more things I want to implement for this. One thing I really want to get good at is stylizing. I think I might come back and add more fancy features and make it look prettier with CSS. I am also thinking using this as the base for my Javascript project. 

This whole program has been a journey. I feel like I have been doing this for so long, but it has been a mere 7 months. I am excited for this journey for the rest of my life. I have learned so much and I have met so many amazing people because of it. I really feel like I've become a better person because of Flatiron. If you're at this point in the program, do not give up. We are so close to finishing and all the headaches and heartbreak will be worth it, I know it will. Continue to surround yourself with people who encourage you and uplift you. I can not stress enough how I would not be where I am now if it had not been for the wonderful individuals I have met along the way. 

