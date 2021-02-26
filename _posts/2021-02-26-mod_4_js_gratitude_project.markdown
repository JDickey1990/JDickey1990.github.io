---
layout: post
title:      "Mod 4  JS Gratitude Project"
date:       2021-02-26 22:56:44 +0000
permalink:  mod_4_js_gratitude_project
---


My choice for the Mod 4 JavaScript Project is an application that allows a user to use a pseudo login page. Upon submitting the user login form a post fetch request with the users name is sent to a create action in the back end user controller. A find or create method either instantiates a new user object or finds the existing user and renders the object and its associated data in JSON format. 


Once a user is "logged in" a series of functions prevents the default action of the DOM and manipulates the HTML displayed to mimic changing pages to a user show page. On the show page gratitude objects associated with the user are displayed in individual div cards. The div cards display the objects attributes and include a button to allow for a gratitude object to be deleted. The user show page also is rendered with a form that allows a user to create a new gratitude object by filling out its attributes and triggering a post fetch when the form is submitted.


The pace that we covered the JavaScript material was difficult to keep up with but by the end of this project build I found a lot of the key concepts had solidified. Taking a concept and applying it outside of a test driven lab really forces me to visualize the intent of what I am doing and account for how each piece will integrate into the application overall.




