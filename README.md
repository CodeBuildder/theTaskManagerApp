The Task Manager App or the Scheduler app is created using NodeJS as a backend application.

Using different routers, the Users can CRUD their accounts and tasks which will further be authenticated using tokens for every single user.

The User account details and the password which is hashed will be stored in MongoDB along with the tasks which can be added to individual users.

Documentation for the application to be run on POSTMAN after copying the URL : https://thetaskmanagerapp.herokuapp.com
 
 
 <h1> Documentation: </h1>
 __________________________________________________________________________________________________________________________________________________________________
 POST function: 
 
/users: Creating a Username to the DataBase.

    Mandatory JSON Information to be added: {
            
            "name":"Sample",
            "email":"sample@gmail.com",
            "password":"sample"
}  


/users/login : Authentication of Users via their credentials.

      Mandatory JSON Information to be added: {
            
            "email":"Place your email to authenticate here.",
            "password":"Enter your password to be authenticated."

}  

/users/logout: Will logout the User who is currently authenticated.

/users/logoutAll: Will remove the current user from every device logged in.

/users/tasks : Allows Authenticated Users to add tasks to their profile. 

       Mandatory JSON Information to be added: {
            
            "description":"Study",
            "completed":"true"

}

/users/me/avatar: Allows to add a new Profile Picture to your profile: ( There are checkpoints to ensure that only a png file is uploaded which is less that 10MB to                                                                         manage the cloud Database with more ease.)

_______________________________________________________________________________________________________________________________________________________________

Get functions:

/users/me: Gets the userdata for the user who is currently logged in.

/tasks: Gets all the tasks added to that particular User who is logged in.

/task/(id) : Gets the particular task that is added to that particular task. (given for a search feature)

________________________________________________________________________________________________________________________________________________________________

Patch function for updating:

/users/me: updates the user details with specific to authentication. (Anything can be updated as long as it exists as category in the databse)


  Mandatory JSON Information to be added: {
  
        
    "DataToBeChanged": "Value"
  
  }
  
  eg:  {
      
      "name": "Sample2"
    
  }
  
  
  /users/tasks/(id): updates the task details with specific to authentication.
      
       Mandatory JSON Information to be added: {
  
        
    "Category": "Value"
  
  }
  
  _______________________________________________________________________________________________________________________________________________________________
  
  DELETE function for deleting the user, task or the avatar of that particular user authenticated or logged on at that moment.
  
  /users/me: Deletes that particular user who is logged on from the MongoDB.
  
  /tasks/(id): Deletes the specific task mentioned.
  
  /users/me/avatar: Deletes only the avatar or the profile picture uploaded (if any) by that particular user.
      
  ________________________________________________________________________________________________________________________________________________________________
  
























