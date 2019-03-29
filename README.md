# Post IT

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
This app will use different API's to collect IT related job postings. The user will be able to search for specific job postings related to their field, save job postings, and follow a link to apply for the job.

### App Evaluation
[Evaluation of your app across the following attributes]
- **Category:** Productivity / Business
- **Mobile:** We want to develop the app primarily for mobile and have a companion desktop app. We want the user to be able to find job postings on mobile, and if the job doesn't have easy apply, the user can continue applying on a desktop.
- **Story:** Lets the user search for IT jobs while on the go and lets them save or apply for the job. A desktop companion app would allow the user to apply for a job saved on the mobile app if the process is too hard on mobile.
- **Market:** Anyone looking for an job in an IT related field.
- **Habit:** Job seekers would be using this app throughout the day to look up new job postings or access existing job aplications.
- **Scope:** V1 Allow the user to search for job postings from different API's and save them to apply for later. User will be able to open a link directly to the application page. V2 App would let user email apps to themselves to be able to apply on a desktop. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User can create an account entering name, password,and email.
* User can search for job postings
* User can save job postings
* User can click on a link and follow the job application page
* User can view a job application

**Optional Nice-to-have Stories**

* User can email the job posting to themselves
* User can apply for a job on the app

### 2. Screen Archetypes

* Login screen
   * User can login to an existing account or be directed to the signup screen
* Signup screen
   * User can sign up for an account by suppliying name, email and a password
* Search screen
   * User can search for job postings
* Saved job applications
* View a job application

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Search IT
* Save IT
* Log out
* Settings

**Flow Navigation** (Screen to Screen)

* Login -> Sign up if no account has been created
* Search for a job application -> View a job posting -> Save a job posting
* Settings -> Modify search results

## Wireframes
<img src="https://i.imgur.com/1Oa5uLC.jpg" width=600>

### [BONUS] Digital Wireframes & Mockups
<img src="https://i.imgur.com/0HXgNpZ.png" width=600>

### [BONUS] Interactive Prototype
<img src="https://i.imgur.com/a2tLtgr.gif" width=600>

## Schema 
### Models
#### User

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | Username      | String   | Unique hashed id for the user |
   | Password      | String   | Hashed password for the user|
   | Email         | String   | Hashed email for the user |
   | Job Post      | JSON Object | Job posts saved by user  |

### Networking
- Login screen
  -(Read/GET) Verify username and password to access account
- Search screen
  -(Read/GET) Retrieve posts searched by user      
- Save screen
  -(Update/PUT) Save job post to user
- View screen
  -(Read/GET) Retrieve and display a single job post
      
- [OPTIONAL: List endpoints if using existing API such as Yelp]
