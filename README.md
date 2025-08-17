<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saint Momina School - Jainpur (Meerut Road)</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #6e48aa;
            --secondary: #9d50bb;
            --accent: #2c3e50;
            --light: #f0f8ff;
            --white: #ffffff;
            --shadow: 0 4px 20px rgba(0,0,0,0.1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            color: #333;
            line-height: 1.6;
            background-attachment: fixed;
        }
        
        /* Mobile Navigation */
        .mobile-nav {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            z-index: 1000;
            padding: 15px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }
        
        .mobile-nav .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: white;
            display: flex;
            align-items: center;
        }
        
        .mobile-nav .logo i {
            margin-right: 10px;
        }
        
        .nav-toggle {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 1.8rem;
            color: white;
            background: transparent;
            border: none;
            cursor: pointer;
        }
        
        .mobile-menu {
            display: none;
            background: var(--white);
            position: absolute;
            top: 100%;
            left: 0;
            width: 100%;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .mobile-menu.active {
            display: block;
        }
        
        .mobile-menu a {
            display: block;
            padding: 12px 0;
            text-decoration: none;
            color: var(--primary);
            font-weight: 600;
            font-size: 1.1rem;
            border-bottom: 1px solid #eee;
        }
        
        .mobile-menu a:last-child {
            border-bottom: none;
        }
        
        .header {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            height: 100vh;
            min-height: 600px;
            position: relative;
            text-align: center;
            color: white;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
            opacity: 0.15;
            z-index: 1;
        }
        
        .header-content {
            position: relative;
            z-index: 3;
            max-width: 900px;
            padding: 20px;
        }
        
        .school-name {
            font-size: 2.8rem;
            font-weight: 800;
            margin-bottom: 15px;
            text-shadow: 2px 2px 8px rgba(0,0,0,0.3);
            letter-spacing: -1px;
        }
        
        .affiliation-badge {
            background: rgba(255, 255, 255, 0.9);
            color: var(--primary);
            padding: 12px 25px;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 700;
            display: inline-block;
            margin: 20px 0;
            box-shadow: var(--shadow);
            border: 2px solid var(--white);
        }
        
        .cbse-logo {
            width: 40px;
            height: 40px;
            background: var(--white);
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            margin-right: 10px;
            font-size: 1.5rem;
            color: var(--primary);
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }
        
        .scroll-down {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 2.5rem;
            color: white;
            animation: bounce 2s infinite;
            z-index: 3;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {transform: translateY(0) translateX(-50%);}
            40% {transform: translateY(-20px) translateX(-50%);}
            60% {transform: translateY(-10px) translateX(-50%);}
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 60px 20px;
        }
        
        .section {
            background: var(--white);
            border-radius: 20px;
            padding: 30px;
            margin-bottom: 40px;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
            transition: transform 0.3s ease;
        }
        
        .section:hover {
            transform: translateY(-5px);
        }
        
        .section::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 8px;
            height: 100%;
            background: linear-gradient(to bottom, var(--primary), var(--secondary));
        }
        
        h1, h2, h3 {
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        h1 {
            font-size: 2.5rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        
        h2 {
            font-size: 2rem;
            position: relative;
            padding-bottom: 15px;
            margin-top: 0;
        }
        
        h2::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border-radius: 2px;
        }
        
        p {
            font-size: 1.1rem;
            margin-bottom: 20px;
            color: #444;
        }
        
        .highlight {
            background: linear-gradient(120deg, rgba(110, 72, 170, 0.1) 0%, rgba(157, 80, 187, 0.1) 100%);
            padding: 25px;
            border-radius: 15px;
            margin: 25px 0;
            border-left: 4px solid var(--primary);
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 35px;
        }
        
        .feature-card {
            background: var(--white);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            box-shadow: var(--shadow);
            transition: all 0.3s ease;
            border-top: 4px solid var(--primary);
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.15);
        }
        
        .feature-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            font-size: 1.6rem;
            margin-bottom: 15px;
        }
        
        .map-container {
            margin: 35px 0;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 12px 30px rgba(0,0,0,0.15);
            height: 400px;
        }
        
        .map {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .payment-section {
            display: flex;
            flex-direction: column;
            gap: 30px;
            align-items: center;
            margin: 35px 0;
        }
        
        .payment-info {
            width: 100%;
        }
        
        .qr-code {
            text-align: center;
            padding: 20px;
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8eb 100%);
            border-radius: 15px;
            box-shadow: var(--shadow);
            width: 100%;
            max-width: 300px;
        }
        
        .qr-code img {
            width: 180px;
            height: 180px;
            border: 2px dashed var(--primary);
            padding: 15px;
            background: var(--white);
            border-radius: 15px;
        }
        
        .login-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            max-width: 300px;
            margin: 25px auto;
            padding: 16px;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            text-align: center;
            box-shadow: 0 6px 20px rgba(110, 72, 170, 0.4);
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .login-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(110, 72, 170, 0.6);
        }
        
        .login-btn i {
            margin-right: 10px;
            font-size: 1.3rem;
        }
        
        .footer {
            background: linear-gradient(135deg, var(--accent) 0%, #4b6584 100%);
            color: white;
            padding: 60px 20px 25px;
            position: relative;
        }
        
        .footer::before {
            content: "";
            position: absolute;
            top: -50px;
            left: 0;
            width: 100%;
            height: 100px;
            background: url('data:image/svg+xml;utf8,<svg viewBox="0 0 1200 120" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none"><path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" fill="%232c3e50"/><path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" fill="%232c3e50"/><path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" fill="%232c3e50"/></svg>');
            background-size: cover;
            background-repeat: no-repeat;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 35px;
        }
        
        .footer-section h3 {
            color: white;
            font-size: 1.6rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-section h3::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--secondary);
        }
        
        .contact-info p {
            display: flex;
            align-items: center;
            margin: 18px 0;
            color: #e0e0e0;
            font-size: 1rem;
        }
        
        .contact-info i {
            margin-right: 12px;
            font-size: 1.2rem;
            color: var(--secondary);
            min-width: 25px;
        }
        
        .admin-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 15px;
        }
        
        .admin-card {
            background: rgba(255, 255, 255, 0.08);
            padding: 18px;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .admin-card:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-5px);
        }
        
        .admin-card h4 {
            font-size: 1.2rem;
            margin-bottom: 8px;
            color: var(--secondary);
        }
        
        .copyright {
            text-align: center;
            padding-top: 35px;
            margin-top: 35px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #bbb;
            font-size: 0.9rem;
        }
        
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.7);
            backdrop-filter: blur(5px);
        }
        
        .modal-content {
            background-color: var(--white);
            margin: 10% auto;
            padding: 30px;
            border: none;
            width: 90%;
            max-width: 500px;
            border-radius: 20px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
            animation: modalopen 0.5s;
            position: relative;
        }
        
        @keyframes modalopen {
            from {opacity: 0; transform: translateY(-60px);}
            to {opacity: 1; transform: translateY(0);}
        }
        
        .close {
            color: #aaa;
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
            transition: color 0.3s;
        }
        
        .close:hover {
            color: var(--primary);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--primary);
            font-size: 1rem;
        }
        
        .form-group input {
            width: 100%;
            padding: 14px;
            box-sizing: border-box;
            border: 2px solid #ddd;
            border-radius: 10px;
            font-size: 1rem;
            transition: all 0.3s;
        }
        
        .form-group input:focus {
            border-color: var(--secondary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(157, 80, 187, 0.2);
        }
        
        .submit-btn {
            width: 100%;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            padding: 14px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-size: 1.1rem;
            font-weight: 600;
            transition: all 0.3s;
            box-shadow: 0 5px 15px rgba(110, 72, 170, 0.4);
        }
        
        .submit-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(110, 72, 170, 0.6);
        }
        
        /* Mobile-specific optimizations */
        @media (max-width: 768px) {
            .mobile-nav {
                display: block;
            }
            
            .header {
                height: 90vh;
                min-height: 500px;
                padding-top: 70px;
            }
            
            .school-name {
                font-size: 2.2rem;
            }
            
            .affiliation-badge {
                font-size: 1rem;
                padding: 10px 20px;
            }
            
            .cbse-logo {
                width: 35px;
                height: 35px;
                font-size: 1.3rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .section {
                padding: 25px 20px;
            }
            
            .highlight {
                padding: 20px;
            }
            
            .map-container {
                height: 300px;
            }
        }
        
        @media (max-width: 480px) {
            .school-name {
                font-size: 1.8rem;
            }
            
            .header {
                min-height: 450px;
            }
            
            .features {
                grid-template-columns: 1fr;
            }
            
            .feature-card {
                padding: 20px;
            }
            
            .feature-icon {
                font-size: 2.5rem;
            }
            
            .feature-card h3 {
                font-size: 1.4rem;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
            }
            
            .admin-grid {
                grid-template-columns: 1fr;
            }
            
            .modal-content {
                padding: 25px 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Mobile Navigation -->
    <nav class="mobile-nav">
        <div class="logo">
            <i class="fas fa-school"></i>
            Saint Momina
        </div>
        <button class="nav-toggle" id="navToggle">
            <i class="fas fa-bars"></i>
        </button>
        <div class="mobile-menu" id="mobileMenu">
            <a href="#about"><i class="fas fa-info-circle"></i> About Us</a>
            <a href="#location"><i class="fas fa-map-marker-alt"></i> Location</a>
            <a href="#payment"><i class="fas fa-money-bill-wave"></i> Fee Payment</a>
            <a href="#contact"><i class="fas fa-phone-alt"></i> Contact</a>
        </div>
    </nav>
    
    <!-- Header Section -->
    <header class="header">
        <div class="header-content">
            <div class="school-name">Saint Momina School</div>
            
            <div class="affiliation-badge">
                <span class="cbse-logo">
                    <i class="fas fa-graduation-cap"></i>
                </span>
                Affiliated to CBSE New Delhi
            </div>
            
            <p style="max-width: 700px; margin: 0 auto 30px; font-size: 1.1rem; text-shadow: 0 1px 3px rgba(0,0,0,0.3);">
                Jainpur, Meerut Road - Providing quality education with modern facilities and a nurturing environment
            </p>
            
            <a href="#about" class="login-btn">
                <i class="fas fa-book-open"></i> Explore Our School
            </a>
        </div>
        
        <div class="scroll-down">
            <i class="fas fa-chevron-down"></i>
        </div>
    </header>
    
    <!-- Main Content -->
    <div class="container">
        <!-- About Section -->
        <section id="about" class="section">
            <h2>About Our Prestigious Institution</h2>
            
            <div class="highlight">
                <p style="font-size: 1.2rem; font-weight: 500; text-align: center;">
                    <i class="fas fa-quote-left" style="color: var(--primary); margin-right: 10px;"></i>
                    Saint Momina School is recognized by the Central Board of Secondary Education (CBSE), New Delhi, 
                    ensuring our students receive a nationally standardized education of the highest quality.
                    <i class="fas fa-quote-right" style="color: var(--primary); margin-left: 10px;"></i>
                </p>
            </div>
            
            <p>Saint Momina School in Jainpur (Meerut Road) is a premier educational institution committed to excellence in academics, sports, and character development. Our state-of-the-art facilities and dedicated staff provide a nurturing environment where students can thrive and reach their full potential.</p>
            
            <p>As a CBSE-affiliated institution, we follow a comprehensive curriculum that balances academic rigor with creative and physical development, preparing our students to excel in all competitive examinations and life challenges.</p>
            
            <h3>Why Choose Saint Momina?</h3>
            
            <div class="features">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-book"></i>
                    </div>
                    <h3>CBSE Curriculum</h3>
                    <p>Nationally recognized curriculum with focus on conceptual understanding and application-based learning</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-flask"></i>
                    </div>
                    <h3>Modern Labs</h3>
                    <p>Fully equipped science, computer, and language labs for practical, hands-on learning</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-medal"></i>
                    </div>
                    <h3>Sports Excellence</h3>
                    <p>Olympic-standard facilities with coaching in cricket, basketball, athletics and more</p>
                </div>
            </div>
        </section>
        
        <!-- Location Section -->
        <section id="location" class="section">
            <h2>Our Campus Location</h2>
            <p>Our sprawling 5-acre campus is located in the peaceful surroundings of Jainpur, easily accessible from Meerut Road. The campus features modern classrooms, lush green spaces, and state-of-the-art facilities designed to inspire learning.</p>
            
            <div class="map-container">
                <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3507.198713780667!2d77.81242181147911!3d28.473561675650824!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x390ca394a643777f%3A0x55908d9065d3e268!2sSaint%20Momina%20School%20Jainpur!5e0!3m2!1sen!2sin!4v1755437697134!5m2!1sen!2sin" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
        </section>
        
        <!-- Payment Section -->
        <section id="payment" class="section">
            <h2>Fee Payment Portal</h2>
            
            <div class="payment-section">
                <div class="payment-info">
                    <p>Pay your school fees conveniently through our secure online payment system. As a CBSE-affiliated institution, we maintain complete transparency in our fee structure.</p>
                    
                    <div style="background: #f8f9fa; padding: 20px; border-radius: 10px; margin: 20px 0;">
                        <h3>Fee Payment Instructions</h3>
                        <ul style="padding-left: 20px; margin-top: 15px;">
                            <li>Scan the QR code with any UPI payment app</li>
                            <li>Enter the exact amount as per fee statement</li>
                            <li>Use student admission number as payment note</li>
                            <li>Keep transaction ID for future reference</li>
                        </ul>
                    </div>
                </div>
                
                <div class="qr-code">
                    <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://example.com/payment/saint-momina&bgcolor=F0F8FF&color=6E48AA" alt="QR Code for Fee Payment">
                    <p style="font-size: 1.1rem; margin-top: 15px; color: var(--primary); font-weight: 600;">Scan to Pay School Fees</p>
                </div>
            </div>
            
            <button class="login-btn" id="loginBtn">
                <i class="fas fa-user-graduate"></i> Student Login Portal
            </button>
        </section>
    </div>
    
    <!-- Footer -->
    <footer id="contact" class="footer">
        <div class="footer-content">
            <div class="footer-section">
                <h3>Contact Us</h3>
                <div class="contact-info">
                    <p><i class="fas fa-map-marker-alt"></i> Jainpur, Meerut Road, Uttar Pradesh 250001</p>
                    <p><i class="fas fa-envelope"></i> saintmominajnp@gmail.com</p>
                    <p><i class="fas fa-phone"></i> 08171989806</p>
                    <p><i class="fas fa-clock"></i> Office Hours: 9:00 AM - 3:00 PM (Mon-Sat)</p>
                </div>
            </div>
            
            <div class="footer-section">
                <h3>Administration</h3>
                <div class="admin-grid">
                    <div class="admin-card">
                        <h4>Chairman</h4>
                        <p>Mr. Shah Faisal</p>
                    </div>
                    <div class="admin-card">
                        <h4>Principal</h4>
                        <p>Mr. Ajeet Sisodia</p>
                    </div>
                    <div class="admin-card">
                        <h4>Vice Principal</h4>
                        <p>Mrs. Tanuja Chaudhary</p>
                    </div>
                </div>
                
                <div style="background: rgba(255,255,255,0.1); padding: 15px; border-radius: 10px; margin-top: 20px; text-align: center;">
                    <p style="font-size: 1.1rem; font-weight: 600;">
                        <i class="fas fa-certificate" style="color: var(--secondary); margin-right: 10px;"></i>
                        Affiliated to CBSE New Delhi
                    </p>
                </div>
            </div>
        </div>
        
        <div class="copyright">
            <p>&copy; 2023-2025 Saint Momina School, Jainpur (Meerut Road). All rights reserved.</p>
        </div>
    </footer>
    
    <!-- Login Modal -->
    <div id="loginModal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>Student Login Portal</h2>
            <form id="loginForm">
                <div class="form-group">
                    <label for="admissionNo">Admission Number:</label>
                    <input type="text" id="admissionNo" name="admissionNo" required placeholder="Enter admission number">
                </div>
                
                <div class="form-group">
                    <label for="rollNo">Roll Number:</label>
                    <input type="text" id="rollNo" name="rollNo" required placeholder="Enter roll number">
                </div>
                
                <div class="form-group">
                    <label for="studentName">Student Name:</label>
                    <input type="text" id="studentName" name="studentName" required placeholder="Enter student name">
                </div>
                
                <div class="form-group">
                    <label for="className">Class Studying Now:</label>
                    <input type="text" id="className" name="className" required placeholder="Enter current class">
                </div>
                
                <button type="submit" class="submit-btn">Login to Portal</button>
            </form>
        </div>
    </div>
    
    <script>
        // Mobile navigation toggle
        const navToggle = document.getElementById('navToggle');
        const mobileMenu = document.getElementById('mobileMenu');
        
        navToggle.addEventListener('click', () => {
            mobileMenu.classList.toggle('active');
        });
        
        // Close mobile menu when clicking a link
        document.querySelectorAll('.mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.remove('active');
            });
        });
        
        // Modal functionality
        const modal = document.getElementById("loginModal");
        const btn = document.getElementById("loginBtn");
        const span = document.getElementsByClassName("close")[0];
        
        btn.onclick = function() {
            modal.style.display = "block";
            document.body.style.overflow = "hidden";
        }
        
        span.onclick = function() {
            modal.style.display = "none";
            document.body.style.overflow = "auto";
        }
        
        window.onclick = function(event) {
            if (event.target == modal) {
                modal.style.display = "none";
                document.body.style.overflow = "auto";
            }
        }
        
        // Form submission
        document.getElementById("loginForm").onsubmit = function(e) {
            e.preventDefault();
            alert("Login successful! Welcome to Saint Momina School Portal.");
            modal.style.display = "none";
            document.body.style.overflow = "auto";
            return false;
        }
        
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
