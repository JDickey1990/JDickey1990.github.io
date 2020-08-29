---
layout: post
title:      "Crypto Coin Price CLI"
date:       2020-08-28 22:23:44 -0400
permalink:  crypto_coin_price_cli
---

Module 1 is coming to an end and I am writing about the first project I have completed in my coding journey. The brief overview of the project requirements were to create a CLI (command line interface) that provides the user data from a website. Using the CLI the user can enter input and receive detailed information about their selection. In order to complete this task I chose to use an API which was a newly introduced concept.

One of the hardest parts of this process for me was picking a starting point and prioritizing the work that needed to be done. Luckily for me there was a lot of incredible resources that were provided that demonstrated what steps needed to be taken to successfully complete the project. I struggled in the beginning of the project with setting up my files and requiring the correct files to run my code successfully. I highly recommend switching to a local environment early on in the program so you get used to these concepts before starting your project. 

This project was an amazing opportunity to take the concepts we have been learning over the last eight weeks and use them in a practical application that was more than passing tests on a lab. It has been challenging and stressful and hands down the most fun I have had yet in this program. 

My project consists of the following sequence of steps:

1.Making an API Call which is using the ruby gems, json, net/http and open-uri.

2.Passing my newly received data set into a method that iterates through and assigns variables equal to the name, price_usd, price_btc and symbol of each coin listed. 

3.Instantiating a new coin object by calling the .new method on my coin class and using the variables assigned above as arguments to pass in and create attributes for each coin instance.

4.All of the instances of coins that are created are stored in an array. Using this array and each.with_index method a list of coins is created and presented to the user.

5.The user selects which coin they would like to see price details of and I use the gets method to receive the choice.

6.Validate the users input and then call the method that will display the price details of the coin selected. 

7.The final step of the project simply allows the user to return and select another coin or exit.







