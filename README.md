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

1. Registration

https://api.needify.com/v1/employer/register

https://api.needify.com/v1/ngo/register

Register either the Non Profit or Employer

1.1 Key Details entered by the Non Profit include

- Login Details (User Name, Password)
- Contact Details
- Cause (i.e. Childern, Oldage, Healthcare, Volunteer)
- Govt Approved ID Number

1.2 Key Details entered by the Employer

- Login Details (User Name, Password)
- Contact Details
- Govt issued ID Number
- No of Employees


1.3 Tables Created

1.3.1 Non Profit

- Login Name (PK)
- Password
- Contact
- Cause
- Govt ID Number

1.3.2 Employer

- Login Name (PK)
- Password
- Contact
- Govt ID Number
- Total Number of Employees
- SSO Details (Future Use)

2. Login/Logout/Update Profile



