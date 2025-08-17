

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Waweru Architecture Designs</title>
  <style>
    /* ===== CSS START ===== */
    * {margin:0;padding:0;box-sizing:border-box;}
    body {font-family:'Segoe UI',sans-serif;background:#f9f9f9;color:#333;line-height:1.6;}

    header {background:#222;color:#fff;padding:1rem 2rem;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;}
    header .logo {font-size:1.4rem;font-weight:bold;}
    header nav ul {list-style:none;display:flex;flex-wrap:wrap;}
    header nav ul li {margin:0 10px;}
    header nav ul li a {color:#fff;text-decoration:none;padding:6px 12px;border-radius:4px;transition:.3s;}
    header nav ul li a:hover,header nav ul li a.active {background:#ff9900;}

    .hero {text-align:center;padding:4rem 2rem;background:url('https://images.unsplash.com/photo-1505691938895-1758d7feb511?auto=format&fit=crop&w=1500&q=80') no-repeat center/cover;color:#fff;}
    .hero h1 {font-size:2.5rem;margin-bottom:1rem;text-shadow:2px 2px 5px rgba(0,0,0,.6);}
    .btn {background:#ff9900;color:#fff;padding:.8rem 1.5rem;border-radius:25px;text-decoration:none;transition:.3s;}
    .btn:hover {background:#e68a00;}

    .tabs {max-width:1000px;margin:auto;padding:2rem;}
    .tab-content {display:none;animation:fadeIn .6s ease-in-out;}
    .tab-content.active {display:block;}
    .tab-content img {width:100%;max-width:800px;margin:1rem auto;display:block;border-radius:12px;box-shadow:0 4px 12px rgba(0,0,0,.2);}

    .gallery {display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:15px;margin-top:1rem;}
    .gallery img {width:100%;border-radius:10px;transition:.3s;}
    .gallery img:hover {transform:scale(1.05);box-shadow:0 6px 18px rgba(0,0,0,.3);}

    #contact {background:#fff;padding:2rem;text-align:center;border-radius:12px;box-shadow:0 2px 8px rgba(0,0,0,.1);}
    footer {text-align:center;background:#222;color:#fff;padding:1rem;margin-top:2rem;}

    @keyframes fadeIn {from{opacity:0}to{opacity:1}}
    /* ===== CSS END ===== */
  </style>
</head>
<body>

<header>
  <div class="logo">Waweru Architecture Designs</div>
  <nav>
    <ul>
      <li><a href="#" class="tab-link active" data-tab="about">About</a></li>
      <li><a href="#" class="tab-link" data-tab="gallery">Gallery</a></li>
      <li><a href="#" class="tab-link" data-tab="contact">Contact</a></li>
    </ul>
  </nav>
</header>

<section class="hero">
  <h1>Innovative Designs, Quality Craftsmanship</h1>
  <p>Delivering sustainable solutions for modern architecture</p>
  <a href="#contact" class="btn">Contact Us</a>
</section>

<section class="tabs">
  <div id="about" class="tab-content active">
    <h2>About Us</h2>
    <p>We specialize in architectural designs with a focus on sustainability and innovation.</p>
    <img src="https://images.unsplash.com/photo-1496307042754-b4aa456c4a2d?auto=format&fit=crop&w=1500&q=80" alt="Architecture design">
  </div>

  <div id="gallery" class="tab-content">
    <h2>Our Work</h2>
    <div class="gallery">
      <img src="https://images.unsplash.com/photo-1501594907352-04cda38ebc29?auto=format&fit=crop&w=800&q=80" alt="House design">
      <img src="https://images.unsplash.com/photo-1505691938895-1758d7feb511?auto=format&fit=crop&w=800&q=80" alt="Building design">
      <img src="https://images.unsplash.com/photo-1484154218962-a197022b5858?auto=format&fit=crop&w=800&q=80" alt="Interior design">
    </div>
  </div>

  <div id="contact" class="tab-content">
    <h2>Contact Us</h2>
    <p>Call us at: <strong>0758206162</strong></p>
    <p>Email: info@waweruarchitecture.com</p>
  </div>
</section>

<footer>
  <p>&copy; 2025 Waweru Architecture Designs. All rights reserved.</p>
</footer>

<script>
  // ===== JavaScript =====
  document.addEventListener("DOMContentLoaded", function () {
    const tabLinks = document.querySelectorAll(".tab-link");
    const tabContents = document.querySelectorAll(".tab-content");

    tabLinks.forEach(link => {
      link.addEventListener("click", function (e) {
        e.preventDefault();
        tabLinks.forEach(l => l.classList.remove("active"));
        tabContents.forEach(c => c.classList.remove("active"));
        this.classList.add("active");
        document.getElementById(this.dataset.tab).classList.add("active");
      });
    });
  });
</script>

</body>
</html>