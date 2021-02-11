---
layout: post
title:  "Homework Three: Domain Driven Design"
subtitle: Homework Three
date:   2021-02-10 18:21:29 -0500
categories: Microservices Homework
permalink: /Homework-three/
---

#### Bussiness Opportunity: Retailer payment processing
A cat t-shirt clothing store is trying to setup an online shop. They allow customers to submit photos of their cats and then print them on Tshirts and provide them to the owners of the photos as well as selling them
in their shop. Currently they do this locally but their shop is really popular and they want to expand their bussiness by bringing it online. They need to have a way to submit photos of cats, they need to curate the photos to make sure only the highest quality cat photos are made into Tshirts, and things like photos of spiders aren't made into tshirts. They also need a way to keep track of orders of Tshirts, and how they'll be delievered(Shipping). 


![Cat Tshirt Flowchart](/images/BussinessFlowCatTshirts.png)


#### Descritpion
The process for creating a new product begins when customers submit photos of their beloved cats for review. If a cat is deemed sufficently photogenic, and the photo is high enough quality it is selected by the review team and the customer is notified their cat has been selected. From there, the picture is sent to the design team who will create the final Tshirt design. They will incorporate the picture of the cat into some kind of situation, perhaps in space, or eating pizza, as an egyptian pharaoh, etc. After their design is finished the Tshirt is sent to the printing team who will create the actual products. When the printing team has created the shirts for this product line, they will alert sales and provide them with the final product so promotional/marketing items can be created and the product can be placed on the online store for purchase. After a customer chooses a Tshirt to buy, sales handles the payment processing and distribution will ship the item to the customer with their preferred method. 

#### Subteam: Sales
The sales and distribution team is responsible for processing the payments of purchased orders and putting the products up on the online retail store. They also handle pricing and marketing materials.

Requirements: 
An easy process for submitting marketing materials and creating a new product entry that will be displayed on the online store.

Inventory Management for products.

A way to easily track and view these orders so they can be sent out.



#### System Architecture

![Cat Tshirt Services](/images/CatTshirtServices.png)


Sales members will submit their products and promotional materials through a standarized process to create a product entry that can be displayed on the front end. The Product Catalog service will track initial inventory and update it whenever a purchase goes through on the front end, it will notify the catalog service so it can update its inventory. When the inventory is empty, the product will be removed from the online shop or be marked as sold out. 

When a purchase is made the front end also notififes the Order Service, providing the customers shipping information. This information is then formatted for the distribution team who will work on getting the product sent to its new owner via the shipping methods they chose. It also creates a barcode for the order which can be used to track which stage of shipping it is currently in. The order team will scan an item before it goes onto a truck which will notify the Order Service that it can remove that order from its backlog and alert the customer through the stores tracking page that their new cat tshirt is on its way. 









