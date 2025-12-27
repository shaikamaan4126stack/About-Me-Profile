
<html>
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Portfolio</title>

  <style>
    *{margin:0;padding:0;box-sizing:border-box;}

    body{
      background:linear-gradient(135deg,#0c0c0c 0%,#1a1a2e 50%,#16213e 100%);
      color:aliceblue;
      font-family:'Arial',sans-serif;
      line-height:1.6;
    }

    #logo{
      width:50px;
      border-radius:50%;
      object-fit:cover;
      border:3px solid #007bff;
    }

    .navbar{
      position:sticky;
      top:0;
      width:100%;
      background:rgba(0,0,0,.9);
      backdrop-filter:blur(10px);
      padding:12px 20px;
      display:flex;
      justify-content:space-between;
      align-items:center;
      z-index:1000;
      border-bottom:1px solid rgba(0,123,255,.4);
    }

    .logo{color:#00c6ff;font-size:18px;font-weight:600;}

    .nav-links{
      display:flex;
      gap:35px;
      list-style:none;
    }

    .nav-links a{
      color:aliceblue;
      text-decoration:none;
      font-size:18px;
      padding:6px 10px;
      border-radius:20px;
      transition:.3s;
    }

    .nav-links a:hover{
      background:#007bff;
      transform:translateY(-2px);
    }

    .hamburger{
      width:32px;
      height:24px;
      display:none;
      flex-direction:column;
      justify-content:space-between;
      cursor:pointer;
    }

    .hamburger span{
      height:3px;width:100%;
      background:#00c6ff;
      border-radius:50px;
      transition:.35s;
      box-shadow:0 0 10px #00c6ff;
    }

    .hamburger.active span:nth-child(1){
      transform:translateY(10px) rotate(45deg);
    }
    .hamburger.active span:nth-child(2){opacity:0;}
    .hamburger.active span:nth-child(3){
      transform:translateY(-10px) rotate(-45deg);
    }

    @media(max-width:850px){
      .hamburger{display:flex;}
      .nav-links{
        position:absolute;
        top:62px;right:0;
        width:200px;
        background:#0a1425;
        flex-direction:column;
        gap:18px;
        padding:18px 20px;
        border-left:1px solid #007bff;
        border-bottom:1px solid #007bff;
        box-shadow:0 0 20px rgba(0,123,255,.4);
        display:none;
      }
      .nav-links.show{display:flex;}
    }

    #About{text-align:center;padding:70px 5vw;}
    #About h1{font-size:3rem;}
    #About h3{color:#007bff;margin:1rem 0;}

    button{
      width:260px;height:60px;
      border-radius:50px;
      border:none;
      background:linear-gradient(45deg,#007bff,#0056b3);
      color:white;font-weight:bold;
      cursor:pointer;
      transition:.3s;
    }
    button:hover{transform:translateY(-3px);}

    #image{text-align:center;padding:2rem 0;}

    #myimg{
      width:300px;height:300px;
      border-radius:20px;
      object-fit:cover;
      border:5px solid #007bff;
      box-shadow:0 20px 40px rgba(0,123,255,.3);
    }

    #Myself{max-width:800px;margin:auto;text-align:center;padding:40px 5vw;}
    .lead{margin:1rem 0;}

    #skills{text-align:center;padding:40px 5vw;}
    .PRJ{
      margin:10px auto;
      padding:1rem;
      border-radius:20px;
      border:1px solid rgba(0,123,255,.3);
      width:200px;
    }

    #contact{
      text-align:center;
      padding:25px;
      margin:40px auto;
      width:90%;
      max-width:600px;
      background:rgba(255,255,255,.06);
      border:1px solid rgba(0,123,255,.4);
      border-radius:15px;
    }

    .mail-btn{
      display:inline-block;
      margin-top:10px;
      padding:10px 22px;
      border-radius:25px;
      background:#007bff;
      color:white;
      text-decoration:none;
      font-weight:bold;
    }
  </style>
</head>

<body>

  <nav class="navbar">
    <div class="logo">
      <img src="https://github.com/shaikamaan4126stack/About-Me-Profile/blob/main/LOGO.jpg?raw=true" id="logo" alt="My Logo">
    </div>

    <div class="hamburger" id="menu-btn">
      <span></span><span></span><span></span>
    </div>

    <ul class="nav-links" id="nav-links">
      <li><a href="#About">Home</a></li>
      <li><a href="#Myself">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <div id="About">
    <h1>Shaik Amaan</h1>
    <h3>Aspiring Fullstack Development</h3><br><br>
    <button><b>Explore My Work</b></button>
  </div>

  <div id="image">
    <img src="https://github.com/shaikamaan4126stack/About-Me-Profile/blob/main/AMAAN%20PIC.png?raw=true" id="myimg" alt="Profile">
  </div>

  <div id="Myself">
    <h1>ABOUT ME</h1><br>
    <p id="h3">Who I am and what I do</p>

    <p class="lead">
      Hi, my name is Shaik Amaan. I've completed my Bachelor's in Computer Applications...
    </p>

    <p>
      I chose this field because I'm fascinated by how data helps in making smarter decisions.
    </p>

    <p>
      Apart from academics, I've built the <strong>Identity Card Issuance Portal</strong> project.
    </p>
  </div>

  <div id="skills">
    <h1 id="TECHINCAL">TECHNICAL EXPERTISE</h1>

    <button>HTML</button>
    <button>CSS</button>
    <button>JavaScript</button>
    <button>Python</button>
    <button>SQL</button>

    <p class="PRJ">+2<br>Web Projects</p>
    <p class="PRJ">+5<br>SQL Projects</p>
    <p class="PRJ">+1<br>Final Year Project</p>
  </div>

  <div id="contact">
    <h1>CONTACT DETAILS</h1>

    <p><strong>Name:</strong> Shaik Amaan</p>
    <p><strong>Location:</strong> Hyderabad, India</p>
    <p><strong>Phone:</strong> +91 7483948860</p>
    <p><strong>Email:</strong> shaikamaan.bca2025@gmail.com</p>

    <a href="mailto:shaikamaan@gmail.com" class="mail-btn">Send Email</a>
  </div>

  <script>
    const menuBtn = document.getElementById("menu-btn");
    const navLinks = document.getElementById("nav-links");

    menuBtn.onclick = () => {
      menuBtn.classList.toggle("active");
      navLinks.classList.toggle("show");
    };
  </script>

</body>
</html>
