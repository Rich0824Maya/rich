<html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>My Web Portfolio</title>
  <style>
    * {
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f4f4f4;
      color: #333;
      margin: 0;
      padding: 0;
    }

    /* Navbar */
    nav {
      background-color: #222;
      color: white;
      padding: 15px 20px;
      position: sticky;
      top: 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;
    }

    nav a {
      color: white;
      margin: 0 10px;
      text-decoration: none;
      font-weight: bold;
    }

    nav a:hover {
      color: #4CAF50;
    }

    header {
      text-align: center;
      padding: 40px 20px;
      background-color: #333;
      color: #fff;
    }

    .profile {
      text-align: center;
      margin: 20px auto;
    }

    .profile img {
      width: 150px;
      border-radius: 50%;
      transition: transform 0.3s ease;
    }

    .profile img:hover {
      transform: scale(1.05);
    }

    .section {
      max-width: 800px;
      margin: 40px auto;
      padding: 20px;
      background: white;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.05);
      opacity: 0;
      transform: translateY(50px);
      transition: all 0.8s ease-out;
    }

    .section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      margin-bottom: 15px;
      color: #444;
    }

    ul {
      list-style: none;
      padding-left: 0;
    }

    ul li {
      margin-bottom: 8px;
    }

    .social a {
      margin-right: 10px;
      color: #0073e6;
      text-decoration: none;
    }

    .social a:hover {
      text-decoration: underline;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: #222;
      color: white;
    }

    #backToTop {
      position: fixed;
      bottom: 30px;
      right: 30px;
      padding: 10px 15px;
      font-size: 14px;
      background: #4CAF50;
      color: white;
      border: none;
      border-radius: 50px;
      cursor: pointer;
      display: none;
      z-index: 999;
    }

    @media (max-width: 600px) {
      nav {
        flex-direction: column;
        align-items: flex-start;
      }

      .profile img {
        width: 100px;
      }
    }
  </style>
</head>
<body>

  <nav>
    <div><strong>Rich Matthew E. Maya</strong></div>
    <div>
      <a href="#projects">Projects</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <header>
    <h1>Welcome to My Portfolio</h1>
    <p class="description">Web Developer | UI/UX Designer</p>
  </header>

  <div class="profile">
    <img src="C:\Users\ay\OneDrive\Desktop\profile.jpg" alt="Profile Picture">
  </div>

  <div class="section" id="projects">
    <h2>Projects</h2>
    <ul>
      <li><strong>Portfolio Website</strong> – HTML/CSS/JavaScript</li>
      <li><strong>Landing Page</strong> – Figma to Code</li>
      <li><strong>Mobile App UI</strong> – UI Design with Adobe XD</li>
    </ul>
  </div>

  <div class="section" id="about">
    <h2>About Me</h2>
    <p><strong>Location:</strong> Bolbok, Batangas City, Batangas</p>
    <p><strong>Skills:</strong> HTML, CSS, JavaScript, Figma</p>
    <p><strong>Experience:</strong> 2+ years freelance encoder</p>
    <p><strong>Achievements:</strong> Developed and implemented a fully functional application addressing a specific problem</p>
    <div class="social">
      <strong>Connect:</strong>
      <a href="https://facebook.com/ritsmaya">Facebook</a>
      <a href="http://Instagram.com/ritsmaya">Instagram</a>
      <a href="https://tiktok.com/ritsmaya">Tiktok</a>
    </div>
  </div>

  <div class="section" id="contact">
    <h2>Contact</h2>
    <p>Email : richmatthewmaya@gmail.com</p>
    <p>Phone Number: +63 906 418 8622</p>
  </div>

  <footer>
    <p>&copy; 2025 Rich Maya. All rights reserved.</p>
  </footer>

  <button id="backToTop">↑ Top</button>

  <script>
    // Scroll Reveal Animation
    const sections = document.querySelectorAll('.section');
    const revealOnScroll = () => {
      const triggerBottom = window.innerHeight * 0.9;
      sections.forEach(sec => {
        const boxTop = sec.getBoundingClientRect().top;
        if (boxTop < triggerBottom) {
          sec.classList.add('visible');
        }
      });
    };
    window.addEventListener('scroll', revealOnScroll);
    revealOnScroll();

    // Back to Top Button
    const backToTopBtn = document.getElementById('backToTop');
    window.onscroll = () => {
      if (document.documentElement.scrollTop > 300) {
        backToTopBtn.style.display = "block";
      } else {
        backToTopBtn.style.display = "none";
      }
    };
    backToTopBtn.onclick = () => {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    };
  </script>
</body>
</html>
