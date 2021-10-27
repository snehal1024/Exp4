<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="exp3.css">
    
  </head>
  <body>
    <script> 
  function myFunction() {
            let username = document.getElementById('user').value;
            let password = document.getElementById('pwd').value;
            let email = document.getElementById('mail').value;
            let birthdate = document.getElementById('bd').value;
            let city = document.getElementById('city').value;
            let x;
            var markedCheckbox = document.getElementsByName('pl');
            for (var checkbox of markedCheckbox) {
                if (checkbox.checked)
                    x += checkbox.value + ', ';
                // x.append(checkbox.value + ', ');

            }
            
                // x.append(checkbox.value + ', ');

            if (username.length < 1) {
                alert('Please Fill Username!')
                return;
            }
            if (password.length < 8) {
                alert('Password should be at least 8 characters')
                return;
            }




            if (email.length < 1) {
                alert('Please Fill Email!')
                return;
            }

            if (birthdate.length < 1) {
                alert('Please Fill Birthdate!')
                return;
            }
            if (username.length > 20) {
                alert("Username limit exceeded!");
                return;
            }
            x = x.slice(9);
            x = x.slice(0, -1);

            if (/^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/.test(email)) {
                document.getElementById("mailo").innerHTML = email;
            } else {
                alert("You have entered an invalid email address!")
                return;
            }


            document.getElementById("ou").innerHTML = x;
            document.getElementById("usero").innerHTML = username;
            document.getElementById("bdo").innerHTML = birthdate;
            document.getElementById("cityo").innerHTML = city;
        }
        </script> 
    <div class="container">
      
      <form id="form" class="form">
        <h2>Registration Form</h2>
        <div class="form-control">
          
          <label for="username"><h3>Username</h3></label>
                <input class="input" type="text" name="username" id="user" placeholder="Username" required="required">
                
        </div>
        <div class="form-control">
          <label for="password"><h3>Password</h3></label>
                <input class="input" type="password" name="password" id="pwd" placeholder="Password" required="required">
                
        </div>
        <div class="form-control">
         <label for="email"><h3>Email</h3></label>
                <input class="input" required="required" type="email" name="email" placeholder="Email" id="mail">
                
        </div>
        <div class="form-control">
         <label for="birthdate"><h3>BirthDate</h3></label>
                <input class="input" required="required" type="date" name="birthdate" id="bd">
                
          <br><br>
                
  <!--Gender:
  <br>
  <input type="radio" name="gender">Male <input type="radio" name="gender">Female-->
         <div class="form-control">
        <label for="city"><h3>City</h3></label>
                <select class="input" required="required" name="city" id="city">
                        <option value="Mumbai">Mumbai</option>
                        <option value="Delhi">Delhi</option>
                        <option value="Bangalore">Bangalore</option>
                        <option value="Kolkata">Kolkata</option>
                    </select>
                </div>
  <label><h3>Programming Languages Known</h3></label>
                <div class="form-control">
                    <input type="checkbox" id="c" name="pl" value="C">
                    <label class="input" for="c"> C</label><br>
                    <input type="checkbox" id="cpp" name="pl" value="C++">
                    <label class="input" for="cpp"> C++</label><br>
                    <input type="checkbox" id="java" name="pl" value="Java">
                    <label class="input" for="java"> Java</label><br>
                    <input type="checkbox" id="javaScript" name="pl" value="javaScript">
                    <label class="input" for="javaScript"> JavaScript</label><br>
                    <input type="checkbox" id="python" name="pl" value="python">
                    <label class="input" for="python"> Python</label><br>
</select><br>
  

          
        </div>
        
         <button id="btn" type="submit" class="main__btn" onclick="myFunction();">Submit</button>
                <br>
      </form>
    
