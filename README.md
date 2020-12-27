# Open Philanthropy
Open Source Platform to Connect Enterprises with the Needy

Written Primarily in Golang and Java Script and run on any public clouds

References

https://jaxenter.com/go-micro-microservice-framework-154603.html

https://techbeacon.com/app-dev-testing/9-best-open-source-options-building-microservice-apps

https://www.velotio.com/engineering-blog/build-a-containerized-microservice-in-golang

https://github.com/golang-standards/project-layout

https://www.infoq.com/news/2016/01/gizmo-microservices-toolkit/

https://github.com/dhax/go-base/

https://levelup.gitconnected.com/building-a-todo-api-in-golang-with-kubernetes-1ec593f85029



# Version 1 Alpha API

# User Management Micro Service

1. Registration

https://api.needify.com/v1/employer/register

https://api.needify.com/v1/ngo/register

Register either the Non Profit or Employer

1.1 Key Details entered by the Non Profit include

- Login Details (User Name, Password)
- Name
- Description
- Contact Details
- Cause (i.e. Childern, Oldage, Healthcare, Volunteer)
- Govt Approved ID Number
- Website

1.2 Key Details entered by the Employer

- Login Details (User Name, Password)
- Name
- Contact Details
- Govt issued ID Number
- No of Employees
- Website


1.3 Tables Created

1.3.1 Non Profit

- Login Name (PK)
- Password
- Name
- Description
- Contact
- Cause
- Govt ID Number
- Website Link


1.3.2 Employer

- Login Name (PK)
- Password
- Name
- Contact
- Govt ID Number
- Total Number of Employees
- SSO Details (Future Use)
- Website Link

2. Login/Logout/Update Details/Delete/Refresh Token

2.1 Login

https://api.needify.com/v1/employer/login

https://api.needify.com/v1/ngo/login

Login will result in JWT being issued as the response

The token will be used for future secure encrypted communication (Potentially Phase-2 of iteration)

2.2 Logout

https://api.needify.com/v1/employer/:id/logout

https://api.needify.com/v1/ngo/:id/logout

Logout redirects to the home page

2.3 Update/Delete

The following API will be impremented in the next Phase

https://api.needify.com/v1/employer/:id/update

https://api.needify.com/v1/ngo/:id/update

https://api.needify.com/v1/employer/:id/delete

https://api.needify.com/v1/ngo/:id/delete

# NGO Microservice

The NGO service allows the NGO to create externally visble profile with images and videos. It will also enable the NGO to create events 

1. Profile

1.1 Profile
The NGO can create a profile describing their work. 

https://api.needify.com/v1/ngo/:id/createprofile


1.2 File Uploads

An NGO can upload an image and a video that would be stored in S2 bucket with a unique link

https://api.needify.com/v1/ngo/:id/uploadimage
https://api.needify.com/v1/ngo/:id/uploadvideo

1.3 Table

Table Details - Non Profit Description. The profile information is stored as xml doc in Dynamo DB

Login Name (PK)
Description (Doc XML)
Image Link
Video Link

2. Events

The NGO can create and delete events. The 

https://api.needify.com/v1/ngo/:id/event
https://api.needify.com/v1/ngo/:id/event/:id/delete




