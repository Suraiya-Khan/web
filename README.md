# web
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8"/>
    <meta http-equiv="X-UA-Compayible" content="IE=edge"/>
    <meta name="viewport" content="width=device-width,initial-scale=1.0"/>
    <title>Restaurant</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

    
   <style>
  
    body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

* {
   box-sizing: border-box;
}
input,textarea[type=text] {
   padding: 12px;
   font-size: 17px;
   border: 1px solid grey;
   float: left;
   width: 80%;
   background: #f1f1f1;
}
button {
   float: left;
   width: 20%;
   padding: 12px;
   background: rgb(14, 81, 204);
   color: white;
   font-size: 17px;
   border: 1px solid grey;
   border-left: none;
   cursor: pointer;
}
button:hover {
   background: #1b11a5;
}

.topnav {
  overflow: hidden;
  background-color: hwb(0 91% 7%);
  font-weight: bold;
}

.topnav a {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 20px;
}

.topnav a:hover {
  background-color: #ddd;
  color: rgb(27, 12, 238);
  font-weight: bold;
}

.topnav a.active {
  color: rgb(17, 9, 234);
}

#img {
  background-image: url('https://img4.goodfon.com/wallpaper/nbig/e/e7/fastfud-gamburger-ovoshchi-ogon-dvoe-eda.jpg');
  padding: 19em 0;
  width:100%;
  background-repeat: no-repeat;
  border-image: space;
  margin: top 5px;
  background-size:cover;
  background-origin: padding-box;
  background-position: center;
  
  
}

.logo{
  position:absolute;
    top: 30%;
    left: 50%;
    transform: translate(-50%, -50%);
  text-align: center;
  padding: 50px;
  margin: 6px 4px; 
  width:300px;
  border-radius: 10px;
  background-color:blue ;}
  
  .text{position:absolute;
    top: 40%;
    left: 50%;
    transform: translate(-50%, -50%);
    padding: 8px;
    font-size: 15px;
    text-align: center;
    color: black;
    width:300px;
    margin: 6px 4px; 
    
   }

   .text1{position:absolute;
    top: 48%;
    left: 50%;
    padding: 8px;
    transform: translate(-50%, -50%);
    font-size: 15px;
    text-align: center;
    color: black;
    width:300px;
    margin: 6px 4px; 
   }



footer {
  background-color: black;
  color: white;
  bottom: 0;
  width: 100%;
  font-size: 16px;
}
footer * {
  box-sizing: border-box;
  border: none;
  outline: none;
}

.row {
  padding: 1em 1em;
}
.row.primary {
  display: grid;
  grid-template-columns: 3fr 2fr 4fr;
  align-items: stretch;
}
.column {
  width: 100%;
  display: flex;
  flex-direction: column;
  padding: 0 2em;
  min-height: 15em;
}
h3 {
  width: 100%;
  text-align: left;
  color: white;
  font-size: 1.4em;
  white-space: nowrap;
}
ul {
  list-style: none;
  display: flex;
  flex-direction: column;
  padding: 0;
  margin: 0;
}
li:not(:first-child) {
  margin-top: 0.8em;
}
ul li a {
  color: #a7a7a7;
  text-decoration: none;
}
ul li a:hover {
  color: #c7940a;
}
.about p {
  text-align: justify;
  line-height: 2;
  margin: 0;
}
input,textarea,
button {
  font-size: 1em;
  padding: 1em;
  width: 100%;
  border-radius: 5px;
  margin-bottom: 5px;
  background: #f1f1f1;
}
button {
  background-color: #c7940a;
  color: #ffffff;
}
div.social {
  display: flex;
  justify-content: space-around;
  font-size: 2.4em;
  flex-direction: row;
  margin-top: 0.5em;
}
.social i {
  color: #bac6d9;
  
}

.copyright {
  padding: 0.3em 1em;
  background-color: #25262e;
}
.footer-menu{
  
  text-align: center;
    margin-top: 10px;
}
.footer-menu a{
  color: #cfd2d6;
  padding: 6px;
  text-decoration: none;
}
.footer-menu a:hover, .social i:hover{
  color: #c7940a;
}
.copyright p {
  font-size: 0.9em;
  text-align: right;
}

@media screen and (max-width: 850px) {
  .row.primary {
    grid-template-columns: 1fr;
  }
}

.button {
  background-color: #d71919; /* Green */
  border: none;
  color: white;
  padding: 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 18px;
  margin: 4px 2px;
  cursor: pointer;
  position:absolute;
  top: 40%;
  left: 50%;
  width:200px;
  transform: translate(-50%,-50%);
  border-radius: 12px;
  transition: all 0.5s;
}

</style>
</head>

    <body onload="resetSelection()">
      <header>
        <br/>
        <div class="topnav">
          <!--<a class="logo">Food Dost</a>
            <a class="active" href="#home">Home</a>
            <a href="#about">About</a>-->
            <a href="#Create your account">Create your account</a>
            <a href="#login">Login</a><div id="img">
          </div>

          <div><a class="logo" style="font-size: 25px; font-weight: bold;">Find your taste @Food Dost</a></div>

          <div class="text" >
            <select  class="text" id="countrySelect" size="1" onchange="makeSubmenu(this.value)">
            <option class="text" value="" disabled selected>Your Location</option>
            <option>Main Road</option>
            <option>Doranda</option>
            <option>Ranchi</option>
            </select>
          </div>            

           <div class="text1" ><select class="text" id="citySelect" size="1" >
            <option  class="text1" value="" disabled selected>Choose your Restaurant</option>
            <option>Kaveri</option>
            <option>Anand</option>
            <option>The Junglee</option>
            <option>The best Restaurant</option>
            </select>
            </div>
          
            <!--<div class="text">
              <input type="text" placeholder="Enter location" /> 
              <input type="text" placeholder="Search for Restaurant" />-->

              
               
          <!--<div><button class="button">Order Now</button></div>-->
        </header>
        
        
        <footer>
          <div class="row primary">
            <div class="column link">
              <h3>Connect</h3>
              
              <div class="social">
                <i class="fa fa-facebook-square"></i>
                <i class="fa fa-twitter-square"></i>
                <i class="fa fa-linkedin-square"></i>
                <i class="fa fa-instagram"></i>
              </div>
            </div>
          
            <div class="column link">
              <h3>Contact Information</h3>
              <p>
                <i class="fa fa-map-marker" aria-hidden="true"></i>
                Resaldar Nagar, Doranda
                Ranchi, Jharkhand
                Landmark- Habib Heights
                Pin- 834002
              </p>
            </div>
          
            <div class="column subscribe">
              <h3>Feedback</h3>
              <div>
                <input type="email" placeholder="Your email id here" />
                <textarea id="w3review" name="w3review" rows="4" cols="50" placeholder="Your Feedback" ></textarea>
                <button>submit</button>
              </div>
            </div>
          </div>

          <div class="row copyright">
            <div class="footer-menu">
          
            <a href="">Home</a>
            <a href="">F.A.Q</a>
            <a href="">Cookies Policy</a>
            <a href="">Terms Of Service</a>
            <a href="">Support</a>
             </div>
            </div>
           
           <!-- <hr style="height:4px;border-width:0;color:rgb(247, 240, 240);background-color:gray">-->
            <p style="text-align: center;">Copyright &copy; Suraiya Khan || All rights reserved,2023</p>
          
        </footer>
         
    </body>

</html>
