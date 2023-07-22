# DoubleBusinessCard
 This project consists of showing two single-sided business cards in which the HOVER effect slightly changes the presentation through the opacity and the social networks and the role of each professional appear with a footer using animation

HTML:

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Card Profile</title>
    <link rel="stylesheet" href="micardprofile.css">
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.0.13/css/all.css">
<div class="container">
</head>

<body>
    <div class="card-wrapper">
      
      <div class="card">
        
        <div class="card-image">
          <img src="https://image.ibb.co/dUTfmJ/profile_img.jpg" alt="profile one">
        </div>

      <ul class="social-icons">
        <li>
          <a href="">
            <i class="fab fa-facebook-f"></i>
          </a>
        </li>
        <li>
          <a href="">
            <i class="fab fa-instagram"></i>
          </a>
        </li>
        <li>
          <a href="">
            <i class="fab fa-twitter"></i>
          </a>
        </li>
        <li>
          <a href="">
            <i class="fab fa-linkedin"></i>
          </a>
        </li>
      </ul>

      <div class="details">
        <h2>John Smith
          <br>
          <span class="job-title">UI Developer</span>
        </h2>
      </div>
    </div>
  </div><!-- end box wrapper --> 
    
    
<div class="card-wrapper">
      
      <div class="card profile-two">
        
        <div class="card-image profile-img--two">
          <img src="https://image.ibb.co/c9rY6J/profile02.jpg" alt="profile two">
        </div>

        <ul class="social-icons">
          <li>
            <a href="">
              <i class="fab fa-facebook-f"></i>
            </a>
          </li>
          <li>
            <a href="">
              <i class="fab fa-instagram"></i>
            </a>
          </li>
          <li>
            <a href="">
              <i class="fab fa-twitter"></i>
            </a>
          </li>
          <li>
            <a href="">
              <i class="fab fa-linkedin"></i>
            </a>
          </li>
        </ul>

        <div class="details jane">
            <h2>Jane Doe
              <br>
              <span class="job-title">UI Designer</span>
            </h2>
        </div>
    </div>
 </div><!-- END box wrapper -->
     
 </div><!-- END container -->

</body>

</html>

CSS:

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  font-family: "Khand", sans-serif;
  background: #000;
}

.container {
  max-width: 900px;
  display: flex;
  justify-content: space-evenly;
  margin: 0 auto;
}

.card-wrapper {
  width: 400px;
  height: 500px;
  position: relative;
}

.card {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 360px;
  height: 480px;
  transform: translate(-50%, -50%);
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 5px 18px rgba(0, 0, 0, 0.6);
  cursor: pointer;
  transition: 0.5s;
}

.card .card-image {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  z-index: 2;
  background-color: #000;
  transition: 0.5s;
}

.card:hover img {
  opacity: 0.4;
  transition: 0.5s;
}

.card:hover .card-image {
  transform: translateY(-100px);
  transition: all 0.9s;
}

/**** Social Icons *****/
.social-icons {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 3;
  display: flex;
}

.social-icons li {
  list-style: none;
}

.social-icons li a {
  position: relative;
  display: block;
  width: 50px;
  height: 50px;
  line-height: 50px;
  text-align: center;
  background: blue;
  font-size: 23px;
  color: orange;
  border-radius: 30px;
  font-weight: bold;
  margin: 0 6px;
  transition: 0.4s;
  transform: translateY(200px);
  opacity: 0;
}

.card:hover .social-icons li a {
  transform: translateY(0px);
  opacity: 1;
}

.social-icons li a:hover {
  background: #000;
  color: #fff;
  transition: 0.2s;
}

.social-icons li a:hover .fab {
  color: #fff;
}

.social-icons li a .fab {
  transition: 0.8s;
}

.social-icons li a .fab:hover {
  transform: rotateY(360deg);
  color: #fff;
}

.card:hover li:nth-child(1) a {
  transition-delay: 0.1s;
}

.card:hover li:nth-child(2) a {
  transition-delay: 0.2s;
}

.card:hover li:nth-child(3) a {
  transition-delay: 0.3s;
}

.card:hover li:nth-child(4) a {
  transition-delay: 0.4s;
}

/**** Personal Details ****/
.details {
  position: absolute;
  bottom: 0;
  left: 0;
  background: blue;
  color: #fff;
  width: 100%;
  height: 120px;
  z-index: 1;
  padding: 10px;
}

.details h2 {
  margin: 30px 0;
  padding: 0;
  text-align: center;
}

.details h2 .job-title {
  font-size: 1rem;
  line-height: 2.5rem;
  color: #fff;
  font-weight: 300;
}

.jane {
 position: absolute;
 left: 0;
 padding: 10px;
 transition: 0.4s;
}


.profile-two .social-icons li a {
  border-radius: 50%;
}

.card:hover .jane {
  bottom: 0;
  left: 0;
  transition-delay: 0.5s;
  opacity: 1;
}






