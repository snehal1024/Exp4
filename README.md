<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="exp3.css">
    
  </head>
  <body>
    <script> 
      
          function display() {
  DispWin = window.open('','NewWin',  'toolbar=no,status=no,width=600,height=400')
 message = "<ul><li><b>NAME: </b>" + document.form1.yourname.value;
 message += "<li><b>Email: </b>" + document.form1.Email.value;
 message += "<li><b>Password: </b>" + document.form1.password1.value ;
 message += "<li><b>Confirm Password: </b>" + document.form1.password2.value ;
 message += "<li><b>Birthdate: </b>" + document.form1.birthday.value;
 message += "<li><b>City: </b>" + document.form1.city.value 
 message += "<li><b>Languages Known: </b>" 



  var checkBox = document.getElementById("first");
  var checkBox1 = document.getElementById("second");
  var checkBox2 = document.getElementById("third");
 

  if (checkBox.checked == true){
   message += "<li>C++</li>"
  } else {
    text.style.display = "none";
  }

 if (checkBox1.checked == true){
   message += "<li>Java</li>"
  } else {
    text.style.display = "none";
  }

 if (checkBox2.checked == true){
   message += "<li>Python</li>"
  } else {
    text.style.display = "none";
  } + "</ul>";

  DispWin.document.write(message);
}

      
            // Function to check Whether both passwords 
      
            // is same or not. 
      
            function checkPassword(form) { 
      
                password1= form.password1.value; 
      
                password2 = form.password2.value; 
      
        
      
                // If password not entered 
      
                if (password1 == '') 
      
                    alert ("Please enter Password"); 
      
                      
      
                // If confirm password not entered 
      
                else if (password2 == '') 
      
                    alert ("Please enter confirm password"); 
      
                      
      
                // If Not same return False.     
      
                else if (password1 != password2) { 
      
                    alert ("\nPassword did not match: Please try again...") 
      
                    return false; 
      
                } 
      
        
      
                // If same return True. 
      
                else{ 
      
                    alert("Password Match: Welcome") 
      
                    return true; 
      
                } 
      
            } 
      
        </script> 
    <div class="container">
      <form name="form1" onSubmit = "return checkPassword(this)"  > 
      <form id="form" class="form">
        <h2>Registration Form</h2>
        <div class="form-control">
          
          Name: <input type="text"  maxlength="20" name="yourname" placeholder="Enter Username">
          
        </div>
        <div class="form-control">
          Email: <input type="email" name="Email" placeholder="Enter email-id" >
        </div>
        <div class="form-control">
          Password: <input type="password" minlength="8" title="Must contain at least  one uppercase and lowercase letter, and at least 8 or more characters and one special character" pattern="(?=^.{8,}$)((?=.\W+))(?![.\n])(?=.[A-Z])(?=.[a-z]).$" name=password1 placeholder="Enter Password" id="password" required>
          
        </div>
        <div class="form-control">
          Confirm  Password: <input type="password" name=password2 placeholder="Re-type password" id="confirm_password" required>
        </div>
        <div class="form-control">
          Birth Date: <input type="date" id="birthday" name="birthday"></div>
  <!--Gender:
  <br><br>
  <input type="radio" name="gender">Male <input type="radio" name="gender">Female-->
        Gender:
        <select id="selection">
          <option>Gender</option>
          <option>Male</option>
          <option>Female</option>
        </select>
       
        <br><br>
        City: <select name="city" id="city" value="City" >
   <option selected disabled>--Select City--</option>
  <option value="Mumbai">Mumbai</option>
  <option value="Delhi">Delhi</option>
  <option value="Pune">Pune</option>
  <option value="Bangalore">Bangalore</option>
</select><br><br>
  

          
        
        
        <input type="submit" style="background-color:grey" name="Signup" onclick="display();">
      </form>
    
