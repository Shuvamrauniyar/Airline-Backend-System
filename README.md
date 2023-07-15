# Airline-Backend-System
- Project Document - [_Software Requirement Specification (SRS).pdf](https://github.com/Shuvamrauniyar/Airline-Backend-System/files/11023100/_Software.Requirement.Specification.SRS.pdf)

## Services and Functionalities 
(Repositories link for each service functionalities is provided below)
- Flight and Search Service  - https://github.com/Shuvamrauniyar/FlightsAndSearchService
- Authentication Service - https://github.com/Shuvamrauniyar/Airline_Authentication_Service
- Ticket Booking Service - https://github.com/Shuvamrauniyar/AirlineTicketBookingService 
- Reminder Ticket Notification Service - https://github.com/Shuvamrauniyar/Airline-Reminder-Service

## Keywords: 
- Microservice Architecture
- MVC -(Model, View, Controller)
- Flight and Search Service, Authentication Service, Booking Service, Reminder Service
- Bcrypt ,JWT Token -for authentication service 
- Sequelize(ORM)
- NodeMailer- for reminder notification service
- CRON JOBS - task scheduler
- AXIOS - for making http requests(GET, POST, PATCH) 

## Test, Result Analysis and Screenshots 

![image](https://user-images.githubusercontent.com/96899142/236890506-ecfdb07f-1984-4b53-b19a-d5d3a6becd82.png)

### FLIGHTS AND SEARCH SERVICE OUTPUTS:

![image](https://user-images.githubusercontent.com/96899142/236890638-b022c285-307d-4755-a3e3-0f78942bf0f0.png)

![image](https://user-images.githubusercontent.com/96899142/236890648-691e569f-865d-4347-a99f-84da458a8b91.png)

![image](https://user-images.githubusercontent.com/96899142/236890667-7405d6ad-7801-474c-adcd-6f275cb5119f.png)

![image](https://user-images.githubusercontent.com/96899142/236890721-1452cd1f-939e-422a-bba4-352b8932a08a.png)


### AUTHENTICATION SERVICE:

- User can signup to the application using unique email and password.
- - If email already exists in the database then user will get error message as shown in picture below:
  - 
![image](https://github.com/Shuvamrauniyar/Airline-Backend-System/assets/96899142/9e90f04a-7518-4278-aa2b-bf190aca06e8)


- After the user has registered to the application, user data will be stored in users table in MySQL DB like as shown in picture below:

![image](https://github.com/Shuvamrauniyar/Airline-Backend-System/assets/96899142/d2d18d9a-bcae-4e0c-b26a-84e32574a3ee)



- You can see that password are encrypted and then stored in database. We used hook to encrypt the password before every user creation . We are encrypting the password using bcrypt.

- New user signup and assigning a role among[ADMIN, CUSTOMER, AIRLINE PERSONNEL] 

![image](https://user-images.githubusercontent.com/96899142/236890966-fd500eb7-945d-4800-8064-5bde56ca6ed8.png)

![image](https://user-images.githubusercontent.com/96899142/236890991-adb05a6f-0bb5-4625-97cd-9ed03d9c1dac.png)

![image](https://user-images.githubusercontent.com/96899142/236891000-b5962620-c92d-42ce-bec3-bfdfc9c9277b.png)


- SignIn and Authentication(token verification):

![image](https://user-images.githubusercontent.com/96899142/236891052-a8ac0a6d-dc58-4fb3-bf6f-d67b618e4521.png)

![image](https://user-images.githubusercontent.com/96899142/236891078-320c783f-93ac-4cd4-9dd2-0a82584cf0fb.png)

![image](https://user-images.githubusercontent.com/96899142/236891104-3a36f8b0-2773-4028-9e22-9d78e02a6767.png)



- CHECKING whether the user is Admin or not:(AUTHORISATION)

![image](https://user-images.githubusercontent.com/96899142/236891163-3a80e677-e986-43e6-9ef0-1c26accc10df.png)

![image](https://user-images.githubusercontent.com/96899142/236891189-7160065e-b40a-40c7-9c92-011f9ccbfb4e.png)



### BOOKING SERVICE:

- Booking the flight:

![image](https://user-images.githubusercontent.com/96899142/236891292-601d3ac5-3d17-4b5b-9da2-ffdb6cf988b8.png)


- For now the booking status is Inprocess , once the payment is done the status is updated to SUCCESS.(this part is yet to be done)

![image](https://user-images.githubusercontent.com/96899142/236891273-a5dfe49d-7816-4eb5-95a0-c9667aadf418.png)

![image](https://user-images.githubusercontent.com/96899142/236891331-fc273dd8-79af-40ad-85e7-cc7ac4b014d3.png)

![image](https://user-images.githubusercontent.com/96899142/236891398-7db1d571-3fde-4ab6-b693-4195f162a3ab.png)


### REMINDER SERVICE:

- Creating ticket:

![image](https://user-images.githubusercontent.com/96899142/236891442-88f8b94e-abe6-4484-8369-cd5d3e31f8a0.png)

![image](https://user-images.githubusercontent.com/96899142/236891522-88b19a0b-e3df-4769-b3e1-945ba6020e55.png)


![image](https://user-images.githubusercontent.com/96899142/236891563-9c12f2fb-66d7-48be-89d3-e1a696daa15a.png)


#### AFTER successful mail sent:(using nodemailer and cron job scheduler):

![image](https://user-images.githubusercontent.com/96899142/236891596-67a33f20-c59d-46a5-8420-b22fe03d58dd.png)


- The status is updated as SUCCESS now:

![image](https://user-images.githubusercontent.com/96899142/236891649-788fe8ca-fe4f-487a-b36b-d4d17a249ea3.png)


