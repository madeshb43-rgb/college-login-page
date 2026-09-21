# college-login-page
web application :college login page using html, java script, cascading stylesheet used to login to college website to access the college information 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mandya University</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #eef3ff;
            scroll-behavior: smooth;
        }

        /* Navigation */
        .navbar {
            background: #002b80;
            padding: 15px 0;
            color: white;
            text-align: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }
        .nav-links a {
            color: white;
            margin: 0 20px;
            text-decoration: none;
            font-size: 18px;
            font-weight: bold;
        }
        .nav-links a:hover {
            color: #ffdf5f;
        }

        /* Container */
        .container {
            max-width: 900px;
            margin: 120px auto 40px;
            background: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0,0,0,0.15);
            animation: fadeIn 1s ease-in-out;
        }

        /* Animations */
        @keyframes fadeIn {
            from {opacity: 0; transform: translateY(20px);} 
            to {opacity: 1; transform: translateY(0);} 
        }
        @keyframes slideUp {
            from {opacity: 0; transform: translateY(40px);} 
            to {opacity: 1; transform: translateY(0);} 
        }

        h1, h2, h3 {
            animation: slideUp 0.8s ease;
        }

        /* Login */
        #login-section input, #login-section select {
            width: 100%;
            padding: 12px;
            margin-top: 10px;
            border: 1px solid #002b80;
            border-radius: 5px;
        }
        #login-section button {
            width: 100%;
            padding: 12px;
            background: #002b80;
            color: white;
            font-size: 18px;
            border: none;
            cursor: pointer;
            margin-top: 20px;
            border-radius: 6px;
        }
        #login-section button:hover {
            background: #001f5c;
        }

        /* Footer */
        .footer {
            background: #002b80;
            padding: 20px;
            color: white;
            text-align: center;
            margin-top: 40px;
        }

        ul { margin-left: 30px; }
        li { font-weight: bold; margin-bottom: 10px; }

        .hidden { display: none; }
    </style>
</head>
<body>

    <!-- NAVIGATION BAR -->
    <div class="navbar">
        <div class="nav-links">
            <a href="#login-section">Login</a>
            <a href="#home">Home</a>
            <a href="#courses">Courses</a>
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
        </div>
    </div>

    <!-- LOGIN PAGE (Page 1) -->
    <div class="container" id="login-section">
        <h1>Student Login</h1>
        <label><b>Name:</b></label>
        <input id="name" type="text" placeholder="Enter your name" required>

        <label><b>Previous Education:</b></label>
        <select id="education">
            <option value="PUC">PUC</option>
            <option value="SSLC">SSLC</option>
            <option value="Diploma">Diploma</option>
            <option value="Other">Other</option>
        </select>

        <button onclick="login()">Login</button>
    </div>

    <!-- MAIN COLLEGE INFO PAGE (Page 2) -->
    <div class="container hidden" id="home">
        <h1>Mandya University, Mandya</h1>
        <p><b>Address:</b><br>Mandya University Mandya Boys College, Near Zudio Shop, Mandya</p>
    </div>

    <div class="container hidden" id="courses">
        <h1>Courses Offered</h1>

        <h2>Science Block</h2>
        <ul>
            <li>BCA (Bachelor of Computer Applications)</li>
            <li>B.Sc (Bachelor of Science)</li>
        </ul>

        <h2>Commerce Block</h2>
        <ul>
            <li>B.Com (Bachelor of
