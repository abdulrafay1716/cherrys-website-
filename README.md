<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Cherry's Technology - Software House</title>
<!-- Google Fonts for elegant styling -->
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet"/>
<style>
  /* Reset and base styles */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  

  body {
    font-family: 'Montserrat', sans-serif;
    background-color: #4b1e2e;
    color: #fff;
    line-height: 1.6;
    overflow-x: hidden;
  }

  a {
    text-decoration: none;
    color: inherit;
  }

  /* Navigation Styles */
  nav {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: rgba(75, 30, 46, 0.9);
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 15px 20px;
    z-index: 1000;
  }

  nav ul {
    list-style: none;
    display: flex;
    flex-wrap: nowrap;
  }

  nav li {
    margin: 0 20px;
  }

  nav a {
    font-weight: 700;
    font-size: 1.1em;
    padding: 8px 12px;
    border-radius: 5px;
    transition: background 0.3s;
  }

  nav a:hover {
    background-color: #a8324b;
  }

  /* Sections Styles */
section {
  padding: 80px 20px;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  transition: all 1s ease;
}

/* Header styles for each section */
section.header {
  background: linear-gradient(135deg, #7d3d50, #a8324b);
  justify-content: center;
  text-align: center;
  color: #fff;
}

section.header h1 {
  font-size: 3em;
  margin-bottom: 20px;
  letter-spacing: 2px;
  animation: fadeInDown 1s ease;
}

section.header p {
  font-size: 1.3em;
  max-width: 700px;
  margin: 0 auto;
  padding: 0 20px;
  animation: fadeIn 2s ease;
}

/* Animation Keyframes */
@keyframes fadeInDown {
  0% { opacity: 0; transform: translateY(-50px); }
  100% { opacity: 1; transform: translateY(0); }
}
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

section.about, section.services, section.contact, section.home {
  background-color: #561c2f;
  border-radius: 20px;
  box-shadow: 0 0 15px rgba(0,0,0,0.4);
}

/* Content styles for each section */
.content {
  max-width: 1200px;
  width: 100%;
  margin-top: 40px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: flex-start;
  opacity: 0;
  transform: translateY(50px);
  animation: fadeInUp 1s forwards;
}

@keyframes fadeInUp {
  to { opacity: 1; transform: translateY(0); }
}

/* Individual card styles for services */
.service-card {
  background-color: #7d3d50;
  margin: 15px;
  padding: 20px;
  border-radius: 12px;
  flex: 1 1 250px;
  min-width: 250px;
  max-width: 350px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.3);
  transition: transform 0.3s, box-shadow 0.3s;
}

.service-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 12px 20px rgba(0,0,0,0.5);
}

.service-card h3 {
  margin-bottom: 10px;
  color: #fff;
  font-size: 1.5em;
}

.service-card p {
  font-size: 1em;
}

/* Contact form styles */
form {
  display: flex;
  flex-direction: column;
  max-width: 600px;
  width: 100%;
  background-color: #4b1e2e;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.4);
  opacity: 0;
  animation: fadeIn 2s forwards;
}

input, textarea {
  margin-bottom: 15px;
  padding: 12px;
  border: none;
  border-radius: 8px;
  font-size: 1em;
}

input[type="submit"] {
  background-color: #a8324b;
  color: #fff;
  font-weight: bold;
  cursor: pointer;
  transition: background 0.3s;
}

input[type="submit"]:hover {
  background-color: #d64c5f;
}

.contact-details {
  margin-top: 30px;
  background-color: rgba(75, 30, 46, 0.8);
  padding: 20px;
  border-radius: 12px;
  font-size: 1.1em;
  max-width: 600px;
  width: 100%;
  color: #fff;
  box-shadow: 0 4px 12px rgba(0,0,0,0.3);
}

.office-info {
  margin-top: 20px;
  font-style: italic;
}

footer {
  background-color: rgba(75, 30, 46, 0.9);
  padding: 20px;
  margin-top: 60px;
  text-align: center;
  font-size: 1em;
  color: #ccc;
}

/* Add some global animations for scroll effect */
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

/* Main page image style */
.page-image {
  width: 100%;
  max-width: 1200px;
  height: auto;
  border-radius: 15px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.5);
  margin-top: 30px;
  transition: transform 0.5s;
}
.page-image:hover {
  transform: scale(1.02);
}

/* Button style for smooth scrolling */
button.nav-btn {
  background-color: transparent;
  border: 2px solid #a8324b;
  padding: 10px 20px;
  border-radius: 8px;
  cursor: pointer;
  color: #fff;
  font-size: 1.1em;
  margin-top: 20px;
  transition: background 0.3s, transform 0.3s;
}
button.nav-btn:hover {
  background-color: #a8324b;
  transform: scale(1.05);
}
</style>
</head>
<body>

<!-- Navigation Menu -->
<nav>
  <ul>
    <li><a href="#home" class="nav-link">Home</a></li>
    <li><a href="#about" class="nav-link">About</a></li>
    <li><a href="#services" class="nav-link">Services</a></li>
    <li><a href="#contact" class="nav-link">Contact</a></li>
  </ul>
</nav>

<!-- Home Section -->
<section id="home" class="header">
  <h1>Welcome to Cherry's Technology</h1>
  <p>Innovating Solutions for Your Business Growth. Serving since 2020 with 90+ satisfied clients in Karachi, Pakistan.</p>
  <!-- Office image -->
  <img src="https://media.istockphoto.com/id/1342421368/photo/modern-bright-office-space.jpg?s=612x612&w=0&k=20&c=bI4-2ilaPc_gsHe0QcYM3cVIjqsprETTvk5PVQ--BDA=" alt="Office Karachi" class="page-image"/>
</section>

<!-- About Section -->
<section id="about" class="about">
  <h2 style="margin-top:20px; margin-bottom:30px;">About Cherry's Technology</h2>
  <div class="content" style="flex-direction: column; align-items: center; text-align: center;">
    <p style="max-width:800px; margin-bottom:20px;">Established 5 years ago, Cherry's Technology has been providing top-notch software solutions to businesses across Karachi. With a dedicated team and 90+ clients, we specialize in custom finance solutions, Power BI dashboards, Payroll systems, POS, Gate Pass systems, and administrative automation to elevate your operations.</p>
    <p style="max-width:800px;">Our mission is to deliver innovative, reliable, and efficient technology services tailored to your needs. Our office is located in Pechs, Karachi, Pakistan.</p>
    <div class="office-info">
      <strong>Office Location:</strong> Pechs, Karachi, Pakistan<br/>
      <strong>Contact:</strong> +92 300 1234567, +92 322 9876543<br/>
      <strong>Email:</strong> info@cherrys-tech.com
    </div>
  </div>
</section>

<!-- Services Section -->
<section id="services" class="services">
  <h2 style="margin-top:20px; margin-bottom:30px;">Our Services</h2>
  <div class="content" style="flex-wrap: wrap; justify-content: center;">
    <!-- Service Card: Finance -->
    <div class="service-card">
      <h3>Finance Management</h3>
      <p>Customized financial solutions including invoicing, expenses tracking, and financial reporting to streamline your financial operations.</p>
    </div>
    <!-- Power BI Dashboard -->
    <div class="service-card">
      <h3>Power BI Dashboard</h3>
      <p>Advanced data visualization and analytics dashboards to help you make data-driven decisions effortlessly.</p>
    </div>
    <!-- Payroll System -->
    <div class="service-card">
      <h3>Payroll System</h3>
      <p>Automated payroll processing, salary calculations, and employee management integrated seamlessly with your HR system.</p>
    </div>
    <!-- POS System -->
    <div class="service-card">
      <h3>Point of Sale (POS)</h3>
      <p>Efficient and reliable POS solutions for retail businesses, including inventory management and sales analytics.</p>
    </div>
    <!-- Gate Pass System -->
    <div class="service-card">
      <h3>Gate Pass System</h3>
      <p>Secure gate pass management system for visitor and employee tracking, enhancing security protocols.</p>
    </div>
    <!-- Administrator System -->
    <div class="service-card">
      <h3>Admin & Management</h3>
      <p>Custom admin panels & management tools for your business operations, user management, and more.</p>
    </div>
    <!-- Additional services: Custom Software & Support -->
    <div class="service-card">
      <h3>Custom Software & Support</h3>
      <p>Tailored software development and ongoing support to meet your specific business requirements.</p>
    </div>
  </div>
</section>

<!-- Contact Section -->
<section id="contact" class="contact">
  <h2 style="margin-top:20px; margin-bottom:30px;">Contact Us</h2>
  <div class="content" style="flex-direction: column; align-items: center;">
    <form id="contactForm">
      <input type="text" name="name" placeholder="Your Name" required />
      <input type="email" name="email" placeholder="Your Email" required />
      <textarea name="message" rows="6" placeholder="Your Message" required></textarea>
      <input type="submit" value="Send Message" />
    </form>
    <div class="contact-details">
      <p><strong>Owner Nadeem:</strong> nadeem@cherrys-tech.com</p>
      <p><strong>Owner Sadiq:</strong> sadiq@cherrys-tech.com</p>
      <p><strong>Location:</strong> Pechs, Karachi, Pakistan</p>
      <p><strong>Phone:</strong> +92 300 1234567 | +92 322 9876543</p>
    </div>
  </div>
</section>

<!-- Footer -->
<footer>
  <p>&copy; 2025 Cherry's Technology. All rights reserved.</p>
</footer>

<!-- Animation and Interaction Scripts -->
<script>
  // Smooth scroll for navigation links
  document.querySelectorAll('.nav-link').forEach(link => {
    link.addEventListener('click', e => {
      e.preventDefault();
      const targetId = link.getAttribute('href').substr(1);
      document.getElementById(targetId).scrollIntoView({ behavior: 'smooth' });
    });
  });

  // Contact Form Submission Handling
  document.getElementById('contactForm').addEventListener('submit', function(e){
    e.preventDefault();
    alert('Thank you for reaching out! We will contact you soon.');
    this.reset();
  });

  // Placeholder for more features: animations, carousel, off-canvas menu, etc.
  // For simplicity, here is a basic dynamic animation effect
  window.addEventListener('scroll', () => {
    // Could add scroll animations or lazy loading here
  });

  // Office picture animation (pulse effect)
  const officeImage = document.querySelector('.page-image');
  officeImage.addEventListener('mouseover', () => {
    officeImage.style.transform = 'scale(1.05)';
  });
  officeImage.addEventListener('mouseout', () => {
    officeImage.style.transform = 'scale(1)';
  });
</script>
</body>
</html>
