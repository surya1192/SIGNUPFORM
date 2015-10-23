# SIGNUPFORM
<html>
<head>
<title>Great!! You are In Right Place</title>
<script src="../jquery/jquery.js"></script>
<style type="text/css">
html{
	min-height:100%;
    }
a{
	color:blue;
}
p{
    font-family:"Comic Sans MS", cursive;
	color:black;
	text-align:center;

    }
h4{
	font-family:"Times New Roman", Times, serif;
	color:black;
	text-align:center;
   }
	
h2{
	font-family:"Trebuchet MS", Arial, Helvetica, sans-serif;
	color:Black;
	margin:0.5em auto;
	position:relative;
	width:500px;
	text-align:center;
	
    }
h3{
	font-family:"Comic Sans MS", cursive;
	
	}
	
body{
	background:url(../Images/abstract-reflective-glossy-sphere-hd-wallpaper-43441.jpg);
	font-family:"Trebuchet MS", Arial, Helvetica, sans-serif;
	color:#555;
    }
.subtext{
	font-size:.8em;
	}
.wrap{
	width:500px;
	margin:5em auto;
	background:2px 3px 6px rgba(0, 0, 0, 0.8);
	padding:2em 4em;
	border-radius:0.4em;
	box-shadow:2px 3px 6px rgba(1, 0, 0, 0.3);
	color:white;
	
	}
label{
		font-weight:bold;
		color:black;
		border-radius:0.4em;
		box-sizing: 3em;
		width:180px;
		
	}
#warning{
	text-align:center;
	display:block;
	margin:3em;
	font-weight:bolder;
	color:black;
	background:#CCC;
	clear:both; 
	padding:.5em;
	border-radius:.5em;
	border:1px solid #333;
	text-shadow:0px 0px 1px white;
	display:none;
	}	
.error{
	color:#F90000;
	font-style:italic;
	font-family:"Comic Sans MS", cursive;
	background:#FFF;
	font-size:.8em;
	width:250px;
	display:block;
	clear:both; 
	padding:.8em;
	border-radius:.5em;
	border:1px solid #FD8282;
	text-shadow:0px 0px 1px white;
	display:none;
	}
.success{
    position:absolute;
	top:20%;
	left:27%;
	z-index:1000;
	width: 39%;
	height:50%;
	margin:0 auto;
	padding:2em 3em;
	border-radius:0.5em;
	box-shadow:0px 3px 6px rgba(0, 0, 0, 0.3);
	text-align:center;
	background:#EEE;
	color:#060;
	text-shadow:1px 0.5px 1px white;
	display:none;
	}
.close{
    font-family:"Trebuchet MS", Arial, Helvetica, sans-serif;
	text-decoration:none;
	background:#2D6BFF;
	color:white;
	padding:1em;
	margin:2em auto;
	display:block;
	width:30%;
	text-align:center;
	border-radius:.5em;
	text-shadow:1px 0.5px 1px #333333;
	font-weight:bolder;
	box-shadow:20px 10px 6px rgba(5, 2, 0.5, 0.5);
	}
form{
	color:black;
	width:400px;
	margin: 5px 5px;
	text-align:right;
	
	}
input{
	padding:.3em;
	border-radius:.4em;
	border:.5em thin black ;
	margin:2.5px 20px;
	float:block;
	border-color:#CCC;
	}
#regno, #first, #last, #Name, #pass, #conpass
    {
	box-shadow:#CCC;
	font-size:0.8em;
	width:180px;
	}
#submit{
	font-family:"Trebuchet MS", Arial, Helvetica, sans-serif;
	text-decoration:none;
	background:#2D6BFF;
	color:white;
	padding:1em;
	margin-left:auto;
    margin-right:auto;
	display:block;
	width:27%;
	text-align:center;
	position:center;
	border-radius:0.4em;
	
	font-weight:bolder;

	
	}

	
</style>

</head>
<body> 

<div class="wrap" >

<div class="success">

<h3> Thank You for Signing Up </h3>

<p> Congrats!! You've Successfully Registered here.Please verify the confirmation mail that you've got in your E-mail !! </p>

<p> <a class="close" href="#"> Continue </a> </p>

</div>
<h2>Create Your Account - Students / Faculty <hr/> </h2>
<form id="Form2" action="javascript:void;" >
                                     
                   <label>Registered/ Roll No : </label> <input type="text" name="Registered number" id="regno" /> <div class="error" id="reg_error" style="display:none;">Please Provide Your Registered Number </div> <br /> 
                    
                   <label>First Name : </label> <input type="text" name="firstname" id="first" /> <div class="error" id="first_error" style="display:none;">You forgot your First Name </div> <br />
                  
                   <label>Last Name : </label><input type="text" name="lastname" id="last"/><div class="error" id="last_error" style="display:none;">You forgot your Last Name </div> <br />
                                                      
                   <label>Email :</label> <input type="email" name="username" id="Name" /> <div class="error" id="un_error" style="display:none;">Please Enter your e-mail </div><br />
                  
                   <label>Password : </label> <input type="password" id="pass" name="password" /><div class="error" id="pass_error" style="display:none;">You forgot to fill your Password </div> <br />
                  
                   <label>Confirm Password: </label> <input type="password" id="conpass" name="confirm password" /> <div class="error" id="conpass_error" style="display:none;">Please confirm your password </div> <br /> <br/> 
                                    

         <input type="submit" value="Sign Up Now" id="submit"/>

</form>
      <div id="warning"></div>
      <p class="subtext"> By Signing Up You Agree to Our <a href="#"> Terms & Conditions </a><br/>
      <hr/> <h4>Already have an account? <a href="#"> Login </h4> </p>
</div>

  <script>

 $("#Form2").submit(function(){
 
    var errors = false;

  $(".error").hide();

   if($("#regno").val() ==""){
    $("#reg_error").show("slow");
    errors = true;
	}
	
   if($("#first").val() ==""){
    $("#first_error").show("slow");
    errors = true;
	}


    if($("#last").val() ==""){
    $("#last_error").show("slow");
    errors = true;
    }

      if($("#Name").val() ==""){
          $("#un_error").show("slow");
          errors = true;
    }
	
	 if($("#male").val() ==""){
           $("#radio_error1").show("slow");
            errors = true;
	 }
	 if($("#female").val() ==""){
           $("#radio_error2").show("slow");
            errors = true;
	 }
      if($("#pass").val() ==""){
           $("#pass_error").show("slow");
            errors = true;
			
    }
	
	  if($("#conpass").val() ==""){
           $("#conpass_error").show("slow");
            errors = true;
 
	}
	/*  if($("#Student").val() ==""){
           $("#option_error1").show("slow");
            errors = true;
 
	}
	if($("#Faculty").val() ==""){
           $("#option_error2").show("slow");
            errors = true;
 
	}
	if($("#Alumni").val() ==""){
           $("#option_error3").show("slow");
            errors = true;
 
	}
	
	  function checkPasswordMatch(){
		  var password = $("#pass").val();
		  var password = $("#conpass").val();
		  
		  if(password!=confirmPassword)
		  ("#divCheckPasswordMatch").html("Passwords Match");
		  
		  
		  
		  
		   <input type="radio"  name="sex" value="male" />Male <div class="error" id="radio_error1" style="display:none;">Please Select Your Sex </div> 
                  
                   <input type="radio" name="sex" value="female">Female <div class="error" id="radio_error2" style="display:none;">Please Select Your Sex </div>  <br/><br /> 
				   
<select name="Select Your Grade">Select Your Grade
<option value="Student">Student</option>
<option value="Faculty">Faculty</option></select>
                   
	  } */

      if(errors){
           $("#warning").html("Sorry,You left some field").show("slow").fadeOut(20000);
           return false;
    } 
           $(".success").fadeIn();
           return true;
 

});

$(".close").click(function(){
  $(".success").fadeOut();
  });

</script>
</body>


</html>
