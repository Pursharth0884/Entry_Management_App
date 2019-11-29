
# Entry Management Web App

> An entry management app built using Node.js that can manage the records of visitors and perform functions accordingly.


- This web app can take the input from the visitor's as well as Host's details like Name, Email, Phone number, Checkin time and Checkout time.
- At the same time can perform the management options like:
   - sending email and sms to the host regarding visitor's stay, after checking in by visitor.
   - After checking out, email would be sent to the visitor regarding their stay.


## Table of Contents


- [Installation](#installation)
- [Features](#features)



---

## Installation

> Requirements 
- Node Js, Mongo db, NPM
- Mailjet username (API KEY) and Password (API KEY) for sending emails. Account can be created <a href="https://app.mailjet.com/signup" target="_blank">here!</a>
- Datagen authorisation key and verified sender ID for sending sms. Account can be created <a href="https://global.datagenit.com/register.html" target="_blank">here!</a>


### Clone

- Clone this repo to your local machine using `https://github.com/Vaibhavraj10/Entry_Management_App.git`

### Setup
> Enter your Mailjet and Datagen credentials in config/mailer.js and save it.

> Install required npm packages

```shell
$ npm install
```
> Run the mongoDb sever
```shell
$ mongod
```
> Run app.js

```shell
$ node app.js
```
> Open the browser and enter the URL
```
http://localhost:3000/
```
---

## Features
- Login, Signup and Logout feature 
- Visitor's Checkin in functionality and sending the details of the visitor to the host by sms and email.
- Visitor's Checking out and sending of email to visitor regarding the details of his stay by email.


## Code and technologies used
- I used `Node.Js` and `Express.js` for designing the backend, along with `EJS` as templating engine. For database, I used `MongoDB` with `Mongoose` as its object modeling tool.
- Further, I also used Nodemailer and Mailjet SMTP for sending emails and Datagen API for sending sms.

---
Entry Management is a software biuld to manage the entries made by visitors to meet the hosts at Innovaccer Office.
Resources Used

    Android Studio (Java and XML)
    Firebase Realtime Database
    Java Mail API
    SMS services

Database Structure

|__Hosts
	|__1
	   |__Email
	   |__Name
	   |__Phone
	|__2
	   |__Email
	   |__Name
	   |__Phone
|_Visitors
	 |__Generated ID
	 		|__checkin
			|__checkin-date
			|__checkout
			|__email
			|__host_object
			|__name
			|__ongoing
			|__phone
			|__token

Approach

I have thought of this software as a simple entry management done at the gate entry. The current way to make entry is to write your and the host details in a register while making an entry and siging that entry with your signature. I have tried to bring the same process in an application on which the visitor can easily make an entry.
Application Flow

    When you open the application a splash screen appears

After a moment the splash finishes and a list of current entries made appears. If no current entries are made a list empty message is displayed.Clicking on "make a new entry" button will display a list of hosts available at the department and whom the visitor can meet.

    The visitor can select one of the hosts he/she wants to meets. You can also add a host by clicking the plus button at the bottom right corner of the screen. A form appears asking the details of the host to be added.

HostForm

    Click on add host button after filling the form. The page closes and the updated list of hosts is again displayed.
    When the visitor selects a host of his/her choice then he/she is asked to fill a form.

After filling in his/her details the visitor presses the "Check-in" button. Doing this the user check-in entry is completed and a token is mailed to the visitor as well.

    After clicking "ok" button, the entry list page again opens with the details of the checked-in user.

FilledEntryList
The host receives an email as well as the message describing the details of the visitor. Image of the mail is attached.After the visit is done the visitor selects his/her details from the list. When the item on the entry lis is clicked a page appears showing the visit details as well as an option to checkout.

    When the "checkout" button is pressed the visitor is asked to confirm the checkout after entering the provided token.

EnterToken
If the visitor enters right token then he/she is successfully checked-out. Also the details of that visitor is removed from that list. The updated list is shown herewith.The visitor then gets an email describing the details of the visit.


