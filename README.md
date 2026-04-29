a# Pr.13.vishal
<?php
// Contact Form Logic
$msg = "";
if(isset($_POST['submit'])){
    $name = $_POST['name'];
    $email = $_POST['email'];
    $message = $_POST['message'];

    if($name && $email && $message){
        $msg = "Thank you $name! Your message has been received.";
    } else {
        $msg = "Please fill all fields!";
    }
}
?>

<!DOCTYPE html>
<html>
<head>
    <title>My College Website</title>
    <style>
        body {
            font-family: Arial;
            margin: 0;
            background: #f4f4f4;
        }

        header {
            background: #004080;
            color: white;
            padding: 15px;
            text-align: center;
        }

        nav {
            background: #333;
            padding: 10px;
            text-align: center;
        }

        nav a {
            color: white;
            margin: 10px;
            text-decoration: none;
            font-weight: bold;
        }

        nav a:hover {
            color: yellow;
        }

        .container {
            padding: 20px;
        }

        .card {
            background: white;
            padding: 15px;
            margin: 10px 0;
            border-radius: 8px;
        }

        footer {
            background: #004080;
            color: white;
            text-align: center;
            padding: 10px;
            margin-top: 20px;
        }

        input, textarea {
            width: 100%;
            padding: 8px;
            margin: 5px 0;
        }

        button {
            background: #004080;
            color: white;
            padding: 10px;
            border: none;
            cursor: pointer;
        }

        button:hover {
            background: #0066cc;
        }
    </style>
</head>

<body>

<header>
    <h1>KD Polytechnic College</h1>
    <p>Welcome to Our College Website</p>
</header>

<nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#courses">Courses</a>
    <a href="#contact">Contact</a>
</nav>

<div class="container">

    <!-- HOME -->
    <div id="home" class="card">
        <h2>Home</h2>
        <p>Welcome to KD Polytechnic Patan. We provide quality education in engineering and technology.</p>
    </div>

    <!-- ABOUT -->
    <div id="about" class="card">
        <h2>About Us</h2>
        <p>Our college is one of the best polytechnic institutes in Gujarat offering diploma courses with experienced faculty.</p>
    </div>

    <!-- COURSES -->
    <div id="courses" class="card">
        <h2>Courses</h2>
        <ul>
            <li>Computer Engineering</li>
            <li>Mechanical Engineering</li>
            <li>Civil Engineering</li>
            <li>Electrical Engineering</li>
        </ul>
    </div>

    <!-- CONTACT -->
    <div id="contact" class="card">
        <h2>Contact Us</h2>

        <form method="POST">
            <input type="text" name="name" placeholder="Enter Name">
            <input type="email" name="email" placeholder="Enter Email">
            <textarea name="message" placeholder="Enter Message"></textarea>
            <button type="submit" name="submit">Send</button>
        </form>

        <p style="color:green;"><?php echo $msg; ?></p>
    </div>

</div>

<footer>
    <p>© 2026 KD Polytechnic Patan | All Rights Reserved</p>
</footer>

</body>
</html>
