<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="exp3.css">
    
  </head>
  <body>
    <script>
      function validateForm() { let x = document.forms["form1"]["yourname"].value;
 let y = document.forms["form1"]["Email"].value; let z = document.forms["form1"]["password1"].value;
 let a = document.forms["form1"]["password2"].value; 
 let b = document.forms["form1"]["birthday"].value; let c = document.forms["form1"]["city"];
  if (x == "") { window.alert("Name must be filled out"); 
  x.focus(); 
  return false;
   } 
   if (y == "") 
   	{ window.alert("Please enter a valid e-mail address.");
   y.focus(); return false; 
}
    if (z == "")
     { window.alert( "Please enter your password");
     z.focus(); return false;
      } if (a == "") 
      { window.alert( "Please enter confirm password.");
       a.focus(); return false; 
   } 
       if (b == "") 
       	{ window.alert("Please enter your Birthdate");
        b.focus(); return false;
        } if (c.selectedIndex < 2) { alert("Please select your city.");
         c.focus(); return false;
          } 
          return true;
          }
           function display()
          { 
          	DispWin = window.open('','NewWin', 'toolbar=no,status=no,width=600,height=400') message = "<ul><li><b>NAME: </b>" + document.form1.yourname.value; message += "<li><b>Email: </b>" + document.form1.Email.value; message += "<li><b>Confirm Password: </b>" + document.form1.password2.value ; message += "<li><b>Birthdate: </b>" + document.form1.birthday.value; message += "<li><b>City: </b>" + document.form1.city.value message += "<li><b>Languages Known: </b>" var checkBox = document.getElementById("first"); var checkBox1 = document.getElementById("second"); var checkBox2 = document.getElementById("third"); if (checkBox.checked == true){ message += "<li>C++</li>" } else { text.style.display = "none"; } if (checkBox1.checked == true){ message += "<li>Java</li>" } else { text.style.display = "none"; } if (checkBox2.checked == true){ message += "<li>Python</li>" } else { text.style.display = "none"; } + "</ul>"; DispWin.document.write(message);} 
      
   <script>
    <div class="container">
       <form name="form1" onSubmit = "return ((validateForm() & checkPassword(this) & display())== 1)" method="post" >
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
    
