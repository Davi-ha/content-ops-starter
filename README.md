<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Machine Company</title>
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
    
    <style>
        /* General Styles */
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            background: #f8f8f8;
            scroll-behavior: smooth;
        }

        /* Navigation */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(50, 50, 50, 0.9);
            padding: 15px 30px;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
            transition: background 0.3s;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            color: white;
        }

        .nav-links {
            list-style: none;
            display: flex;
        }

        .nav-links li {
            margin: 0 15px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-size: 18px;
            transition: color 0.3s;
        }

        .nav-links a:hover,
        .nav-links a.active {
            color: yellow;
        }

        /* Hero Section */
        header {
            background: url('https://source.unsplash.com/1600x900/?factory,machine') center/cover no-repeat;
            color: white;
            text-align: center;
            padding: 160px 20px;
        }

        .hero h1 {
            font-size: 42px;
            animation: fadeIn 2s ease-in-out;
        }

        .btn {
            background: white;
            color: black;
            padding: 12px 24px;
            text-decoration: none;
            border-radius: 5px;
            margin-top: 20px;
            font-weight: bold;
            display: inline-block;
            transition: 0.3s;
        }

        .btn:hover {
            background: yellow;
            color: black;
        }

        /* Sections */
        section {
            padding: 80px 20px;
            text-align: center;
        }

        .machine-gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }

        .machine-gallery img {
            width: 300px;
            height: 200px;
            margin: 10px;
            border-radius: 8px;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .machine-gallery img:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        /* Contact Section */
        .contact-links .btn {
            margin: 10px;
        }

        /* Footer */
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 20px;
        }

        /* Animations */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 1s, transform 1s;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Keyframes */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: scale(0.9);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }
    </style>
</head>
<body>

    <!-- Navigation -->
    <nav>
        <div class="logo">MachineCo</div>
        <ul class="nav-links">
            <li><a href="#about" class="nav-link">About</a></li>
            <li><a href="#machines" class="nav-link">Machines</a></li>
            <li><a href="#contact" class="nav-link">Contact</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <header>
        <section class="hero">
            <h1>Reliable & Powerful <span class="highlight">Machines</span></h1>
            <p>Industry Leaders in Heavy Machinery</p>
            <a href="#machines" class="btn">Explore Machines</a>
        </section>
    </header>

    <!-- About Section -->
    <section id="about" class="fade-in">
        <h2>About Us</h2>
        <p>We specialize in high-quality industrial and agricultural machines.</p>
    </section>

    <!-- Machines Gallery -->
    <section id="machines" class="fade-in">
        <h2>Our Machines</h2>
        <div class="machine-gallery">
            <img src="https://unsplash.com/photos/loading-vehicle-is-outdoors-on-the-borrow-pit-at-daytime-HQcJQL0XgYs 300x200/?excavator" alt="Excavator">
            <img src="https://source.unsplash.com/300x200/?tractor" alt="Tractor">
            <img src="https://source.unsplash.com/300x200/?bulldozer" alt="Bulldozer">
            <img src="https://source.unsplash.com/300x200/?factory,machine" alt="Factory Machine">
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="fade-in">
        <h2>Contact Us</h2>
        <p>Get in touch with us today!</p>
        <div class="contact-links">
            <a href="tel:+256700000000" class="btn">Call Us</a>
            <a href="mailto:info@machineco.com" class="btn">Email Us</a>
            <a href="sms:+256700000000" class="btn">Send SMS</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>© 2025 MachineCo. All rights reserved.</p>
    </footer>

    <script>
        document.addEventListener("DOMContentLoaded", function () {
            const fadeElements = document.querySelectorAll(".fade-in");
            const navLinks = document.querySelectorAll(".nav-link");

            function handleScroll() {
                fadeElements.forEach((el) => {
                    const rect = el.getBoundingClientRect();
                    if (rect.top < window.innerHeight - 50) {
                        el.classList.add("visible");
                    }
                });
            }

            window.addEventListener("scroll", handleScroll);
            handleScroll();

            navLinks.forEach(link => {
                link.addEventListener("click", function() {
                    navLinks.forEach(l => l.classList.remove("active"));
                    this.classList.add("active");
                });
            });
        });
    </script>

</body>
</html
