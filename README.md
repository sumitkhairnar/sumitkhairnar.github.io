# Sumit Khairnar
Returning soon...

   <!doctype html>
<html>
<head>
<meta http-equiv="content-type" content="text/html"; charset="utf-8"/>
<title>registration form</title>
</head>
<body>
<form id="formal" name="formal" method="post" action="index.php">
<div align="center"

    <h2>
    registration form
  </h2>
    

  <tr>
      <td width="165">name</td>
      <td width="163">
      <input type="text" name="name" id="textfield"/></td>
    </tr>
    <tr>
      <td>email</td>
      <td>
      <input type="email" name="email" id="textfield2"/></td>
    </tr>
    <tr>
      <td>username</td>
      <td><input type="text" name="u_name" id="textfield3"/></td>
    </tr>
    <tr>
      <td>password</td>
      <td><input type="password" name="password" id="textfield4"/></td>
    </tr>
    <tr>
      <td colspan="2"><input type="submit" name="submit" id="button" value="Submit" /></td>
    
	</tr>
  
  </form>
</body>
</html>

<?php $con=mysql_connect("localhost","root","") or die (mysql_error()); $db=mysql_select_db('my_db', $con)or die (mysql_error()); if(isset($_POST['submit'])){ $name=$_POST['name']; $email=$_POST['email']; $u_name=$_POST['u_name']; $password=$_POST['password'];} if($name==''){ echo"<script>alert('Enter Your Name')</script>"; } if($email==''){ echo"<script>alert('Enter Your Email')</script>"; } if($u_name==''){ echo"<script>alert('Enter Your User Name')</script>"; } if($password==''){ echo"<script>alert('Enter Your Password')</script>"; } else{ $query="insert into regitration(name,email,u_name,password)value('$name','$email','$u_name','$password')"; if(mysql_query($query)){ echo"<script>alert('You are Succesfull register')</script>"; } } ?>











      











                      

