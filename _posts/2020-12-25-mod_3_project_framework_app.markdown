---
layout: post
title:      "Mod 3 Project_Framework App"
date:       2020-12-26 03:59:32 +0000
permalink:  mod_3_project_framework_app
---


The Mod 3 Ruby on Rails project has been an incredible learning experience for me. The fast-paced curriculum really has a chance to set in when deployed in a project. I chose to make a basic project management application. The functionality of the application as it stands allows a user to create a project by defining a name, description and deadline. 

The project has_many requirements that are defined by the user. A requirement is set up with a has_ many relationship to the projects model. The project and requirement models are joined through the deadline table which has a completed attribute that tracks the status of a requirements completion with a Boolean value. The join table also makes the requirement unique to the project with a deadline attribute for the requirement object. 

Once a project is created a user can see the project information displayed on the project show page along with each project requirement. The basic crud functions are available to a user for a project and a requirement. There is a nested new form for creating a project that belongs to a user while creating three of the top requirements at the same time. 
Nested forms were by far the most time consuming and complicated part of this project for me. For instance, I learned that with a new form if you have a nested resource for the object being passed to the form while using form for you must also have resources for that object outside of your nested resources or else the form will error saying:

```
No route matches [POST] "/project/:id/requirements/new"
```
Thanks to the help of my cohort lead and a couple of the members of my cohort I was able to move past this and several other hurdles while creating my forms. While in the process of troubleshooting I was not particularly thrilled but by the end I felt that I had learned a tremendous amount about nested forms. 

I really enjoyed this mod even though the timing for the final project landing on Christmas was unfortunate. As always, I am looking forward to what comes next on this journey and hope to carry forward the lessons learned over the past few weeks.

