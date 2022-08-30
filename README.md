## 1. Declare React States for error messages and isSubmitted
   We will declare two React states as follows:

       1. errorMessages: Store an object with an error message and the name of the field.
       2. isSubmitted: boolean value to indicate if the form is successfully submitted or not.

## 2. JS function to return JSX code for error message
   The renderErrorMessage function returns JSX code for displaying the error message associated with the field name.
   
## 3. JSX code for login form
   We will add JSX code for the HTML form with input type=”text” for both user name and password along with input type=”submit” to allow users to submit the form.

   Additionally, we will also add error messages below every form input element.
   
## 4. Add function to handle form submit
   To achieve login functionality, we need to create a JS function to handle form submission with validations. The handleSubmit() function accesses the event object of      the form element, event.preventDefault() code avoids default form submit action which includes reloading of the page.
   By assigning handleSubmit() function to onSubmit property of the form, thehandleSubmit() is triggered everytime button/input of type=”submit” is clicked.
   
## 5. Validate form input with user details
   To add login functionality to the form, first, we declare all the correct user details in JS constants. The following steps are required to accomplish the                functionality:

     1. Find expected user details by matching user names.
     2.If a match is not found then add the error message “invalid username“
     3.else validate the password, show the error message “invalid password” if validation fails.
     4.setIsSubmitted(true) if all validations pass.
     
     // User Login info
        const database = [
      {
        username: "user1",
        password: "pass1"
      },
      {
        username: "user2",
        password: "pass2"
       }
     ];
    
## 6. Show success message after submit
   We will add condition rending in React JS based on the isSubmitted state value.

   If isSubmitted=true, show message “User is successfully logged in”.
   Else isSubmitted=false, display the login form.
