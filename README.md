# Functional Requirements :
     - Employer should be able to add Job posts that have job description , budget and min requirements

    - Freelancer should be able to see job posts and apply for the job and make a proposal 

    - Employer able to see Freelancer Proposal and select freelancer 
    
    - Freelancers should be able to edit and update his profile adding 
      some details like ( Skills , Portfolio , hourly rate , etc )

    - Employers should be able to add information like Company name , Posts , etc 
 
    - Employers and Freelancer must be able to chat with each other anytime  

    - Employers and Freelancer to make a contract and issued payment when it complete 
    
    - Freelancer and Employers should be able to search for ( jobs , Freelancer )  by keywords 

    - Employer and freelancer should be able to add review and rating 

# Non Functional Requirements : 

    - System should be able send notifications when Employer or freelancer receive a new massage
    - System should be able to protect user data 
    - System Should be intuitive , efficient and easy for intended user to learn and operate 
    - System should be designed in a way that is easy to modify , correct and enhance in the future
    - System should be scable to hold many user in the same time

# Entity : 
    - Employer 
    - Freelancer 
    - Jobs 
    - Payments
    
# API Design : 
          - POST/jobs -> jobs
            
          {
          
          description ,
             
          budget 
              
          } 
------------------------------------------------

     - GET/jobs?limit=?&page=? 
     
------------------------------------------------

          - PATCH/Freelancer/Profile?profileID -> profileINFO
          
          {
          
          skills ,
          
          protofolio,
          
          hourly rate 
          
          }

------------------------------------------------

     - PATCH/Employers/profile?profileID -> profileINFO
       
     {
     
     company_name ,
     
     job_posts 
     
     }
------------------------------------------------
          
          - POST/payment?paymentID -> PaymentINFO
          
          {
          
          payment_number,
          
          status
          
          }
------------------------------------------------

          - POST/review/freelancer -> rating
            
          {
          
          rate,
          
          feedback
          
          }
------------------------------------------------
     - POST/review/Employer -> rating
       
     {
     
     rate,
     
     feedback
     
     }
------------------------------------------------
# Data Model
<img width="726" height="595" alt="image" src="https://github.com/user-attachments/assets/c269322f-49f7-45cf-aecc-d65017abe60a" />


