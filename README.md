<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Shaik Amaan - Portfolio</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(135deg, #0c0c0c 0%, #1a1a2e 50%, #16213e 100%);
      color: aliceblue;
      font-family: 'Arial', sans-serif;
      line-height: 1.6;
    }

    #logo {
      width: 50px;
      border-radius: 50%;
      object-fit: cover;
      border: 3px solid #007bff;
    }

    /* ==============================
       STICKY NAV + HAMBURGER MENU
       ============================== */
    .navbar {
      position: sticky;
      top: 0;
      width: 100%;
      background: rgba(0, 0, 0, 0.9);
      backdrop-filter: blur(10px);
      padding: 12px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;
      border-bottom: 1px solid rgba(0,123,255,.4);
    }

    /* Logo text inside navbar */
    .logo {
      color: #00c6ff;
      font-size: 18px;
      font-weight: 600;
      letter-spacing: .5px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    /* Nav Links Desktop */
    .nav-links {
      display: flex;
      gap: 35px;
      list-style: none;
    }

    .nav-links a {
      color: aliceblue;
      text-decoration: none;
      font-size: 18px;
      padding: 6px 10px;
      border-radius: 20px;
      transition: .3s ease;
    }

    .nav-links a:hover {
      background: #007bff;
      transform: translateY(-2px);
    }

    /* ========== HAMBURGER ICON (3 Stirring Lines) ========== */
   .hamburger {
  width: 32px;
  height: 24px;
      display: none;
      flex-direction: column;
      justify-content: space-between;
      cursor: pointer;
    }

    .hamburger span {
      height: 3px;
      width: 100%;
      background: #00c6ff;
      border-radius: 50px;
      transition: .35s ease;
      box-shadow: 0 0 10px #00c6ff;
    }

    /* Animated Cross */
    .hamburger.active span:nth-child(1) {
      transform: translateY(10px) rotate(45deg);
    }

    .hamburger.active span:nth-child(2) {
      opacity: 0;
    }

    .hamburger.active span:nth-child(3) {
      transform: translateY(-10px) rotate(-45deg);
    }

    /* ========== MOBILE DROPDOWN MENU ========== */
    @media(max-width: 850px) {
      .hamburger {
        display: flex;
      }

      .nav-links {
        position: absolute;
        top: 62px;
        right: 0;
        width: 200px;
        background: #0a1425;
        flex-direction: column;
        gap: 18px;
        padding: 18px 20px;
        border-left: 1px solid #007bff;
        border-bottom: 1px solid #007bff;
        box-shadow: 0 0 20px rgba(0,123,255,.4);
        display: none;
      }

      .nav-links.show {
        display: flex;
      }

      .nav-links a {
        text-align: left;
        padding: 10px;
      }
    }

    /* HERO SECTION */
    #About {
      text-align: center;
      padding: clamp(50px, 15vh, 100px) 5vw;
    }

    #About h1 {
      font-size: clamp(2.5rem, 8vw, 5rem);
      margin-bottom: 1rem;
    }

    #About h3 {
      font-size: clamp(1.5rem, 5vw, 2.5rem);
      color: #007bff;
      margin-bottom: 2rem;
    }

    button {
      width: clamp(200px, 30vw, 300px);
      height: 60px;
      font-size: clamp(16px, 2.5vw, 20px);
      background: linear-gradient(45deg, #007bff, #0056b3);
      color: white;
      border: none;
      border-radius: 50px;
      cursor: pointer;
      font-weight: bold;
      transition: all 0.3s ease;
    }

    button:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 30px rgba(0, 123, 255, 0.4);
    }

    /* Profile Image */
#image {
  text-align: center;
  padding: 0.5rem 0;
}

    #myimg {
      width: clamp(200px, 35vw, 350px);
      height: clamp(200px, 35vw, 350px);
      border-radius: 20px;
      object-fit: cover;
      border: 5px solid #007bff;
      box-shadow: 0 20px 40px rgba(0, 123, 255, 0.3);
    }

    /* About Section */
 #Myself {
  text-align: center;
  padding: 2rem 5vw;
  max-width: 800px;
  margin: 0 auto;
}

    #Myself h1 {
      font-size: clamp(2rem, 6vw, 3rem);
      margin-bottom: 1rem;
    }

    #h3 {
      font-size: clamp(16px, 3vw, 20px);
      color: #888;
      margin-bottom: 2rem;
      font-weight: normal;
    }

    .lead {
      font-size: 1.2rem;
      margin-bottom: 1.5rem;
      opacity: 0.9;
    }

    /* Skills Section */
#skills {
  padding: 3rem 5vw;
  margin-top: 10px;
  text-align: center;
}

    #TECHINCAL {
      font-size: clamp(2rem, 6vw, 3rem);
      margin-bottom: 3rem;
      background: linear-gradient(45deg, #007bff, #00d4ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
      gap: 1rem;
      max-width: 600px;
      margin: 0 auto 3rem;
    }

    .skills-grid button {
      width: 100%;
      height: 50px;
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border: 2px solid #007bff;
      border-radius: 25px;
      font-weight: bold;
    }

    .skills-grid button:hover {
      background: #007bff;
      transform: translateY(-2px);
    }

    .PRJ {
      background: rgba(255, 255, 255, 0.05);
      padding: 2rem 1rem;
      border-radius: 20px;
      border: 1px solid rgba(0, 123, 255, 0.3);
      font-size: 1.5rem;
      font-weight: bold;
      display: inline-block;
      margin: 0 10px;
    }

    /* Contact Section */
    #contact {
      text-align: center;
      padding: 25px;
      margin: 40px auto;
      width: 90%;
      max-width: 600px;
      background: rgba(255, 255, 255, 0.06);
      border: 1px solid rgba(0, 123, 255, 0.4);
      border-radius: 15px;
    }

    #contact p { 
      margin: 6px 0; 
    }

    .mail-btn {
      display: inline-block;
      margin-top: 12px;
      padding: 10px 22px;
      border-radius: 25px;
      text-decoration: none;
      font-weight: bold;
      background: #007bff;
      color: white;
    }

    .mail-btn:hover { 
      opacity: 0.9; 
    }
    @media(max-width:768px){

  #About{
    padding: 30px 20px;
  }

  #Myself{
    padding: 20px;
  }

  #skills{
    margin-top: 0;
    padding-top: 30px;
  }

  .PRJ{
    width: 100%;
    margin: 10px 0;
  }
}
  </style>
</head>

<body>
  <!-- 🌟 STIRRING HAMBURGER NAVBAR -->
  <nav class="navbar">
    <div class="logo">
      <img src="LOGO.jpg" alt="Shaik Amaan Logo" id="logo">
    </div>

    <!-- 3 Lines Stirring Menu -->
    <div class="hamburger" id="menu-btn">
      <span></span>
      <span></span>
      <span></span>
    </div>

    <ul class="nav-links" id="nav-links">
      <li><a href="#About">Home</a></li>
      <li><a href="#Myself">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- ABOUT SECTION -->
  <div id="About">
    <h1>Shaik Amaan</h1>
    <h3>Trainee Software Engineer </h3>
    <button id="buttton"><b>Explore My Work</b></button>
  </div>

  <!-- IMAGE -->
  <div id="image">
    <img src="./file_0000000059a071f5a1b0bd1a393e681b.png" alt="Shaik Amaan Profile" id="myimg">
  </div>

  <!-- ABOUT ME SECTION -->
  <div id="Myself">
    <h1>ABOUT ME</h1>
<p class="lead">
  Hi, my name is Shaik Amaan. I completed my Bachelor of Computer Applications (BCA) from Karnataka Arts & Science College, Bidar.
  Currently, I am working as a <strong>Trainee Software Engineer</strong> at
  <strong>Accord Software Pvt Ltd, Bangalore</strong>.
</p>

<p>
  I have hands-on experience in <strong>React JS, JavaScript, HTML, CSS,
  Python, SQL, REST APIs and Git</strong>.
</p>

<p>
  I am currently working on the <strong>Nabhmitra Project</strong>, a real-world enterprise application where I contribute to React JS development, API integration, UI enhancement, bug fixing and support activities.
</p>

<p>
  Apart from corporate projects, I have developed the <strong>Identity Card Issuance Portal</strong> and several web applications that strengthened my frontend and full-stack development skills.
</p>

<p>
  I enjoy learning new technologies and building user-friendly web applications that solve real business problems.
</p>
    </div>

  <!-- SKILLS -->
  <div id="skills">
    <h1 id="TECHINCAL">TECHNICAL EXPERTISE</h1>

   <div class="skills-grid">
  <button>React JS</button>
  <button>JavaScript</button>
  <button>HTML</button>
  <button>CSS</button>
  <button>Python</button>
  <button>SQL</button>
  <button>REST API</button>
  <button>Git</button>
</div>

    <div>
      <p class="PRJ">1+<br>Real World Project</p>
<p class="PRJ">5+<br>Web & SQL Projects</p>
<p class="PRJ">1+<br>Corporate Experience</p>
    </div>
  </div>

  <!-- CONTACT -->
  <div id="contact">
    <h1>CONTACT DETAILS</h1>

    <p><strong>Name:</strong> Shaik Amaan</p>
    <p><strong>Location:</strong> Bangalore, Karnataka, India</p>
    <p><strong>Phone:</strong> +91 7483948860</p>
    <p><strong>Email:</strong> shaikamaan.bca2025@gmail.com</p>

    <a href="mailto:shaikamaan.bca2025@gmail.com" class="mail-btn">Send Email</a>
  </div>

  <!-- MENU TOGGLE SCRIPT -->
  <script>
    const menuBtn = document.getElementById("menu-btn");
    const navLinks = document.getElementById("nav-links");

    menuBtn.onclick = () => {
      menuBtn.classList.toggle("active");
      navLinks.classList.toggle("show");
    };
  </script>
