## 🔗 Excalidraw Link :

[https://excalidraw.com/\#json=uBbmwYyThUNYvUBRB6BOP,Z2bX1bgLV6N9BxPhE23ASA](https://excalidraw.com/#json=uBbmwYyThUNYvUBRB6BOP,Z2bX1bgLV6N9BxPhE23ASA)

-----

##  Functional Requirements :

  * Employer should be able to add Job posts that have job description , budget and min requirements
  * Freelancer should be able to see job posts and apply for the job and make a proposal
  * Employer able to see Freelancer Proposal and select freelancer
  * Freelancers should be able to edit and update his profile adding some details like ( Skills , Portfolio , hourly rate , etc )
  * Employers should be able to add information like Company name , Posts , etc
  * Employers and Freelancer must be able to chat with each other anytime
  * Employers and Freelancer to make a contract and issued payment when it complete
  * Freelancer and Employers should be able to search for ( jobs , Freelancer ) by keywords
  * Employer and freelancer should be able to add review and rating

-----

##  Non Functional Requirements :

  * System should be able send notifications when Employer or freelancer receive a new massage
  * System should be able to protect user data
  * System Should be intuitive , efficient and easy for intended user to learn and operate
  * System should be designed in a way that is easy to modify , correct and enhance in the future
  * System should be scable to hold many user in the same time

-----

##  Entity :

  * Employer
  * Freelancer
  * Jobs
  * Payments

-----

##  API Design :

**POST/jobs -\> jobs**

```json
{
  description ,
  budget 
}
```

-----

**GET/jobs?limit=?\&page=?**

-----

**PATCH/Freelancer/Profile?profileID -\> profileINFO**

```json
{
  skills ,
  protofolio,
  hourly rate 
}
```

-----

**PATCH/Employers/profile?profileID -\> profileINFO**

```json
{
  company_name ,
  job_posts 
}
```

-----

**POST/payment?paymentID -\> PaymentINFO**

```json
{
  payment_number,
  status
}
```

-----

**POST/review/freelancer -\> rating**

```json
{
  rate,
  feedback
}
```

-----

**POST/review/Employer -\> rating**

```json
{
  rate,
  feedback
}
```

-----

**POST/Contract?contractID -\> contractINFO**

```json
{
  paymentINFO ,
  Date,
}
```

-----

**POST/proposal -\> proposalINFO**

```json
{
  skills, 
  CV, 
  history
}
```

-----

## Data Model

<img width="726" height="595" alt="image" src="https://github.com/user-attachments/assets/c269322f-49f7-45cf-aecc-d65017abe60a" /> 

-----

## Back of the envelope Estimation :

  * Total User = 5 million
  * Daily active User = 2 million
  * Average jobs/freelance/daily = 2
  * Total request = 2\*2/5

-----

## HLD

<img width="1186" height="911" alt="image" src="https://github.com/user-attachments/assets/3e2c2d52-b2bd-49d4-8f77-29ab9e35d12b" /> 

-----

##  Deep Dives :

<img width="1086" height="1081" alt="image" src="https://github.com/user-attachments/assets/c5af70fc-f7ee-402a-b217-25165f2a755e" /> 


  * will use a normal RestFUl API for All service expect chat will use WebsocketAPI
  * Useing Third party for sending emails Notification to alert and chatting
  * will use a payment getwat that will make payment operation more secuire and efficent
  * job posts will be limited in one page for scaliabilty and maintalbilty
  * editing account will be PATCH because PUT change all data and this edit is Partial so it will be faster
  * every service have one page for make it easy for user to use and will not be one page with two service
  * Review database , Chat Database will be only that never cach because it will not remove
  * Mobile number will not user for dieffrent accoutns

-----
