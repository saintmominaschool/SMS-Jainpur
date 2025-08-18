<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saint Momina School - Jainpur | Premium CBSE Education</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #0a0a2a;
            --secondary: #d4af37;
            --accent: #6a0dad;
            --light: #f8f9fa;
            --white: #ffffff;
            --dark: #050517;
            --success: #4CAF50;
            --error: #f44336;
            --section-height: 100vh;
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            --gold-gradient: linear-gradient(135deg, #d4af37 0%, #f9e076 100%);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: var(--dark);
            color: #e0e0e0;
            line-height: 1.7;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }
        
        /* Header & Navigation */
        .header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            padding: 20px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            background: rgba(10, 10, 42, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: var(--shadow);
            transition: var(--transition);
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo-icon {
            width: 50px;
            height: 50px;
            background: var(--gold-gradient);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            color: var(--primary);
            margin-right: 15px;
            box-shadow: 0 0 20px rgba(212, 175, 55, 0.3);
        }
        
        .logo-text {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
            font-size: 1.8rem;
            color: var(--white);
        }
        
        .logo-text span {
            background: var(--gold-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .nav-links {
            display: flex;
            gap: 30px;
        }
        
        .nav-links a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            position: relative;
            padding: 5px 0;
            transition: var(--transition);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--secondary);
            transition: var(--transition);
        }
        
        .nav-links a:hover {
            color: var(--secondary);
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .nav-btn {
            background: var(--gold-gradient);
            color: var(--primary);
            padding: 12px 25px;
            border: none;
            border-radius: 30px;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: 0 5px 15px rgba(212, 175, 55, 0.3);
        }
        
        .nav-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(212, 175, 55, 0.5);
        }
        
        /* Hero Section */
        .hero {
            height: var(--section-height);
            min-height: 800px;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 0 5%;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
            opacity: 0.15;
            z-index: 1;
        }
        
        .hero::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, rgba(10,10,42,0.6) 0%, rgba(5,5,23,0.9) 100%);
            z-index: 2;
        }
        
        .hero-content {
            position: relative;
            z-index: 3;
            text-align: center;
            max-width: 1000px;
            padding: 100px 0;
        }
        
        .hero-tag {
            background: rgba(212, 175, 55, 0.15);
            color: var(--secondary);
            padding: 8px 20px;
            border-radius: 30px;
            font-size: 1rem;
            font-weight: 500;
            display: inline-block;
            margin-bottom: 20px;
            border: 1px solid rgba(212, 175, 55, 0.3);
            backdrop-filter: blur(5px);
        }
        
        .school-name {
            font-family: 'Playfair Display', serif;
            font-size: 4.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--white);
            text-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        
        .school-name span {
            background: var(--gold-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .hero-text {
            font-size: 1.4rem;
            max-width: 700px;
            margin: 0 auto 40px;
            color: #e0e0e0;
        }
        
        .affiliation-badge {
            background: rgba(255, 255, 255, 0.1);
            color: var(--white);
            padding: 15px 40px;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            margin: 30px 0;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .cbse-logo {
            width: 50px;
            height: 50px;
            background: var(--white);
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-size: 1.8rem;
            color: var(--primary);
        }
        
        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }
        
        .hero-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 16px 35px;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            text-align: center;
            text-decoration: none;
            transition: var(--transition);
            min-width: 220px;
        }
        
        .primary-btn {
            background: var(--gold-gradient);
            color: var(--primary);
            box-shadow: 0 6px 20px rgba(212, 175, 55, 0.4);
        }
        
        .primary-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.6);
        }
        
        .secondary-btn {
            background: transparent;
            color: var(--white);
            border: 2px solid var(--secondary);
        }
        
        .secondary-btn:hover {
            background: rgba(212, 175, 55, 0.1);
            transform: translateY(-5px);
        }
        
        .hero-btn i {
            margin-right: 10px;
            font-size: 1.2rem;
        }
        
        .scroll-down {
            position: absolute;
            bottom: 40px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 2.5rem;
            color: var(--secondary);
            animation: bounce 2s infinite;
            z-index: 3;
            cursor: pointer;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {transform: translateY(0) translateX(-50%);}
            40% {transform: translateY(-20px) translateX(-50%);}
            60% {transform: translateY(-10px) translateX(-50%);}
        }
        
        /* Main Sections */
        .section {
            min-height: var(--section-height);
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: 120px 5%;
            position: relative;
            overflow: hidden;
        }
        
        .section-content {
            max-width: 1400px;
            margin: 0 auto;
            width: 100%;
            position: relative;
            z-index: 2;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 70px;
        }
        
        .section-title h2 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            font-weight: 700;
            color: var(--white);
            margin-bottom: 20px;
            position: relative;
            display: inline-block;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: var(--secondary);
            border-radius: 2px;
        }
        
        .section-title p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 30px auto 0;
            color: #b0b0b0;
        }
        
        .section-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 50px;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: var(--transition);
        }
        
        .section-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.25);
        }
        
        .section-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 8px;
            height: 100%;
            background: var(--gold-gradient);
        }
        
        /* About Section */
        #about {
            background: linear-gradient(135deg, var(--dark) 0%, #1a1a40 100%);
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .about-image {
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            height: 500px;
            position: relative;
        }
        
        .about-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.8s ease;
        }
        
        .about-image:hover img {
            transform: scale(1.05);
        }
        
        .about-text h3 {
            font-family: 'Playfair Display', serif;
            font-size: 2.2rem;
            color: var(--white);
            margin-bottom: 25px;
        }
        
        .about-text p {
            font-size: 1.1rem;
            margin-bottom: 25px;
            color: #d0d0d0;
        }
        
        .highlight-box {
            background: rgba(212, 175, 55, 0.1);
            padding: 30px;
            border-radius: 15px;
            margin: 40px 0;
            border-left: 4px solid var(--secondary);
        }
        
        .highlight-box p {
            font-size: 1.3rem;
            font-weight: 500;
            color: var(--white);
            font-style: italic;
            margin: 0;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .feature-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            background: rgba(212, 175, 55, 0.05);
            border-color: rgba(212, 175, 55, 0.2);
        }
        
        .feature-icon {
            width: 80px;
            height: 80px;
            background: var(--gold-gradient);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            font-size: 2rem;
            color: var(--primary);
        }
        
        .feature-card h3 {
            font-size: 1.6rem;
            margin-bottom: 15px;
            color: var(--white);
        }
        
        .feature-card p {
            color: #b0b0b0;
            margin-bottom: 0;
        }
        
        /* Campus Section */
        #campus {
            background: linear-gradient(135deg, #1a1a40 0%, var(--dark) 100%);
        }
        
        .campus-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .map-container {
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            height: 500px;
            position: relative;
        }
        
        .map {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .campus-features {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 30px;
            margin: 25px 0;
            border-left: 4px solid var(--accent);
        }
        
        .campus-features h3 {
            font-size: 1.8rem;
            color: var(--white);
            margin-bottom: 25px;
            text-align: center;
        }
        
        .campus-features ul {
            padding-left: 20px;
            margin-top: 15px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }
        
        .campus-features li {
            margin-bottom: 15px;
            color: #d0d0d0;
            display: flex;
            align-items: flex-start;
        }
        
        .campus-features li::before {
            content: '✓';
            color: var(--secondary);
            font-weight: bold;
            margin-right: 10px;
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }
        
        .stat-card {
            text-align: center;
            padding: 25px 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            transition: var(--transition);
        }
        
        .stat-card:hover {
            background: rgba(212, 175, 55, 0.05);
            transform: translateY(-5px);
        }
        
        .stat-value {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            font-weight: 700;
            color: var(--secondary);
            margin-bottom: 10px;
            line-height: 1;
        }
        
        .stat-label {
            font-size: 1.1rem;
            color: #b0b0b0;
        }
        
        /* Payment Section */
        #payment {
            background: linear-gradient(135deg, var(--dark) 0%, #1a1a40 100%);
        }
        
        .payment-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .payment-info {
            padding-right: 30px;
        }
        
        .payment-info h3 {
            font-family: 'Playfair Display', serif;
            font-size: 2.2rem;
            color: var(--white);
            margin-bottom: 25px;
        }
        
        .payment-instructions {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 30px;
            margin: 40px 0;
            border-left: 4px solid var(--secondary);
        }
        
        .payment-instructions h4 {
            font-size: 1.5rem;
            color: var(--white);
            margin-bottom: 20px;
            text-align: center;
        }
        
        .payment-instructions ul {
            padding-left: 20px;
            margin-top: 15px;
        }
        
        .payment-instructions li {
            margin-bottom: 15px;
            color: #d0d0d0;
            position: relative;
            padding-left: 30px;
        }
        
        .payment-instructions li::before {
            content: '•';
            color: var(--secondary);
            font-size: 1.5rem;
            position: absolute;
            left: 0;
            top: -5px;
        }
        
        .qr-container {
            text-align: center;
            background: rgba(255, 255, 255, 0.05);
            padding: 40px;
            border-radius: 20px;
            box-shadow: var(--shadow);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }
        
        .qr-code {
            width: 220px;
            height: 220px;
            background: var(--white);
            padding: 15px;
            border-radius: 15px;
            margin: 0 auto 25px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }
        
        .qr-code img {
            max-width: 100%;
            height: auto;
        }
        
        .security-badges {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }
        
        .badge {
            background: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 30px;
            font-size: 0.9rem;
            color: #b0b0b0;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .badge i {
            color: var(--secondary);
        }
        
        /* Portal Section */
        .portal-section {
            margin-top: 40px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 30px;
            border-top: 3px solid var(--secondary);
        }
        
        .portal-section h3 {
            text-align: center;
            color: var(--white);
            margin-bottom: 25px;
            font-size: 1.8rem;
        }
        
        .portal-btns {
            display: flex;
            justify-content: center;
            gap: 25px;
            flex-wrap: wrap;
        }
        
        .portal-btn {
            min-width: 220px;
            padding: 18px 30px;
            border-radius: 12px;
            font-weight: 600;
            font-size: 1.1rem;
            cursor: pointer;
            transition: var(--transition);
            text-align: center;
            border: none;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 12px;
        }
        
        .portal-btn.student {
            background: linear-gradient(135deg, #4a00e0 0%, #8e2de2 100%);
            color: var(--white);
            box-shadow: 0 6px 20px rgba(78, 0, 224, 0.4);
        }
        
        .portal-btn.teacher {
            background: linear-gradient(135deg, #11998e 0%, #38ef7d 100%);
            color: var(--white);
            box-shadow: 0 6px 20px rgba(17, 153, 142, 0.4);
        }
        
        .portal-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .portal-icon {
            font-size: 2.5rem;
        }
        
        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(5px);
            z-index: 2000;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background: var(--dark);
            border-radius: 20px;
            padding: 40px;
            width: 90%;
            max-width: 500px;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5);
            position: relative;
            border: 1px solid rgba(212, 175, 55, 0.3);
        }
        
        .close-modal {
            position: absolute;
            top: 20px;
            right: 25px;
            font-size: 28px;
            color: var(--secondary);
            cursor: pointer;
            transition: var(--transition);
        }
        
        .close-modal:hover {
            transform: rotate(90deg);
        }
        
        .modal-title {
            font-family: 'Playfair Display', serif;
            font-size: 2.2rem;
            text-align: center;
            margin-bottom: 30px;
            color: var(--white);
        }
        
        .modal-form {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .form-group {
            position: relative;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--secondary);
            font-weight: 500;
        }
        
        .form-group input {
            width: 100%;
            padding: 15px;
            border-radius: 10px;
            border: 2px solid rgba(255, 255, 255, 0.1);
            background: rgba(255, 255, 255, 0.05);
            color: var(--white);
            font-size: 1rem;
            transition: var(--transition);
        }
        
        .form-group input:focus {
            outline: none;
            border-color: var(--secondary);
            box-shadow: 0 0 0 3px rgba(212, 175, 55, 0.2);
        }
        
        .submit-btn {
            background: var(--gold-gradient);
            color: var(--primary);
            border: none;
            padding: 16px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1rem;
            cursor: pointer;
            margin-top: 15px;
            transition: var(--transition);
        }
        
        .submit-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(212, 175, 55, 0.6);
        }
        
        /* Footer */
        .footer {
            background: linear-gradient(135deg, #050517 0%, #0a0a2a 100%);
            padding: 100px 5% 50px;
            position: relative;
        }
        
        .footer::before {
            content: "";
            position: absolute;
            top: -50px;
            left: 0;
            width: 100%;
            height: 100px;
            background: url('data:image/svg+xml;utf8,<svg viewBox="0 0 1200 120" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none"><path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" fill="%23d4af37"/><path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" fill="%23d4af37"/><path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" fill="%23d4af37"/></svg>');
            background-size: cover;
            background-repeat: no-repeat;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .footer-section h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            color: var(--white);
            margin-bottom: 30px;
            position: relative;
            padding-bottom: 15px;
        }
        
        .footer-section h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 3px;
            background: var(--secondary);
        }
        
        .contact-info p {
            display: flex;
            align-items: flex-start;
            margin: 20px 0;
            color: #d0d0d0;
            font-size: 1.1rem;
        }
        
        .contact-info i {
            margin-right: 15px;
            font-size: 1.2rem;
            color: var(--secondary);
            min-width: 25px;
            margin-top: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 30px;
        }
        
        .social-link {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.05);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            color: var(--secondary);
            transition: var(--transition);
        }
        
        .social-link:hover {
            background: var(--secondary);
            color: var(--primary);
            transform: translateY(-5px);
        }
        
        .admin-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        
        .admin-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            transition: var(--transition);
        }
        
        .admin-card:hover {
            background: rgba(212, 175, 55, 0.05);
            transform: translateY(-5px);
        }
        
        .admin-card h4 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .admin-card p {
            color: #b0b0b0;
            margin: 0;
        }
        
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 14px;
            margin-bottom: 20px;
            border: none;
            border-radius: 8px;
            background: rgba(255, 255, 255, 0.05);
            color: var(--white);
            font-size: 1rem;
            transition: var(--transition);
        }
        
        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            background: rgba(255, 255, 255, 0.08);
            box-shadow: 0 0 0 2px var(--secondary);
        }
        
        .contact-form button {
            background: var(--gold-gradient);
            color: var(--primary);
            border: none;
            padding: 14px 30px;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 600;
            transition: var(--transition);
            font-size: 1.1rem;
            width: 100%;
        }
        
        .contact-form button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(212, 175, 55, 0.5);
        }
        
        .copyright {
            text-align: center;
            padding-top: 60px;
            margin-top: 60px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #b0b0b0;
            font-size: 1rem;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        /* Mobile Responsiveness */
        @media (max-width: 1100px) {
            .about-content, 
            .campus-content, 
            .payment-content {
                grid-template-columns: 1fr;
            }
            
            .about-image {
                height: 400px;
            }
            
            .section {
                padding: 100px 5%;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .school-name {
                font-size: 3rem;
            }
            
            .hero-text {
                font-size: 1.2rem;
            }
            
            .hero-btns {
                flex-direction: column;
                align-items: center;
            }
            
            .section-title h2 {
                font-size: 2.8rem;
            }
            
            .campus-features ul {
                grid-template-columns: 1fr;
            }
            
            .features {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
            }
            
            .portal-btns {
                flex-direction: column;
                align-items: center;
            }
        }
        
        @media (max-width: 480px) {
            .school-name {
                font-size: 2.5rem;
            }
            
            .section-title h2 {
                font-size: 2.2rem;
            }
            
            .section-card {
                padding: 30px 20px;
            }
            
            .feature-card {
                padding: 25px 20px;
            }
            
            .stat-value {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="logo">
            <div class="logo-icon">
                <i class="fas fa-graduation-cap"></i>
            </div>
            <div class="logo-text">Saint <span>Momina</span></div>
        </div>
        
        <nav class="nav-links">
            <a href="#hero">Home</a>
            <a href="#about">About</a>
            <a href="#campus">Campus</a>
            <a href="#payment">Payments</a>
            <a href="#footer">Contact</a>
        </nav>
        
        <button class="nav-btn" id="studentPortalBtn">
            <i class="fas fa-user-graduate"></i> Student Portal
        </button>
    </header>
    
    <!-- Hero Section -->
    <section class="hero" id="hero">
        <div class="hero-content">
            <div class="hero-tag">
                <i class="fas fa-star"></i> Premium CBSE Education
            </div>
            
            <h1 class="school-name">Saint <span>Momina</span> School</h1>
            
            <p class="hero-text">
                Premier CBSE affiliated school providing quality education and holistic development for future leaders.
            </p>
            
            <div class="affiliation-badge">
                <span class="cbse-logo">
                    <i class="fas fa-graduation-cap"></i>
                </span>
                Affiliated to CBSE New Delhi
            </div>
            
            <div class="hero-btns">
                <a href="#about" class="hero-btn primary-btn">
                    <i class="fas fa-book-open"></i> Explore Academics
                </a>
                <a href="#footer" class="hero-btn secondary-btn">
                    <i class="fas fa-calendar-check"></i> Schedule Visit
                </a>
            </div>
        </div>
        
        <div class="scroll-down">
            <i class="fas fa-chevron-down"></i>
        </div>
    </section>
    
    <!-- About Section -->
    <section id="about" class="section">
        <div class="section-content">
            <div class="section-title">
                <h2>About Our Institution</h2>
                <p>Saint Momina School is recognized by CBSE, New Delhi, ensuring our students receive a nationally standardized education of the highest quality.</p>
            </div>
            
            <div class="section-card">
                <div class="about-content">
                    <div class="about-image">
                        <img src="https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Saint Momina School Campus">
                    </div>
                    
                    <div class="about-text">
                        <h3>Quality Education for Future Leaders</h3>
                        <p>Saint Momina School in Jainpur (Meerut Road) is a premier educational institution committed to excellence in academics, sports, and character development. Our state-of-the-art facilities and dedicated staff provide a nurturing environment where students can thrive and reach their full potential.</p>
                        
                        <div class="highlight-box">
                            <p>"Education is not the filling of a pail, but the lighting of a fire." - William Butler Yeats</p>
                        </div>
                        
                        <p>As a CBSE-affiliated institution, we follow a comprehensive curriculum that balances academic rigor with creative and physical development, preparing our students to excel in all competitive examinations and life challenges.</p>
                    </div>
                </div>
                
                <h3 style="color: var(--white); text-align: center; margin: 70px 0 30px;">Why Choose Saint Momina?</h3>
                
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
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-paint-brush"></i>
                        </div>
                        <h3>Arts & Culture</h3>
                        <p>Comprehensive arts program including music, dance, theater, and visual arts</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Campus Section -->
    <section id="campus" class="section">
        <div class="section-content">
            <div class="section-title">
                <h2>Our Campus</h2>
                <p>Discover our state-of-the-art facilities designed to inspire learning and personal growth.</p>
            </div>
            
            <div class="section-card">
                <div class="campus-content">
                    <div class="campus-features">
                        <h3>Campus Features</h3>
                        <ul>
                            <li>Modern classrooms with smart boards</li>
                            <li>Extensive library with over 5,000 books</li>
                            <li>Indoor and outdoor sports facilities</li>
                            <li>Science and computer laboratories</li>
                            <li>Auditorium with 250-seat capacity</li>
                            <li>Art and music studios</li>
                            <li>Cafeteria with nutritious meals</li>
                            <li>Medical room with full-time nurse</li>
                        </ul>
                    </div>
                    
                    <div class="map-container">
                        <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3507.198713780667!2d77.81242181147911!3d28.473561675650824!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x390ca394a643777f%3A0x55908d9065d3e268!2sSaint%20Momina%20School%20Jainpur!5e0!3m2!1sen!2sin!4v1755437697134!5m2!1sen!2sin" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                    </div>
                </div>
                
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-value">25+</div>
                        <div class="stat-label">Years of Excellence</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">2,500+</div>
                        <div class="stat-label">Students</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">120+</div>
                        <div class="stat-label">Qualified Staff</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">15+</div>
                        <div class="stat-label">Acres Campus</div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Payment Section -->
    <section id="payment" class="section">
        <div class="section-content">
            <div class="section-title">
                <h2>Fee Payment</h2>
                <p>Convenient and secure payment options for our students and parents.</p>
            </div>
            
            <div class="section-card">
                <div class="payment-content">
                    <div class="payment-info">
                        <h3>Secure Payment Portal</h3>
                        <p>Pay your school fees conveniently through our secure online payment system. As a CBSE-affiliated institution, we maintain complete transparency in our fee structure.</p>
                        
                        <div class="payment-instructions">
                            <h4>Payment Instructions</h4>
                            <ul>
                                <li>Scan the QR code with any UPI payment app</li>
                                <li>Enter the exact amount as per fee statement</li>
                                <li>Use student admission number as payment note</li>
                                <li>Keep transaction ID for future reference</li>
                                <li>Fees can also be paid at the school office</li>
                                <li>Contact accounts department for any queries</li>
                            </ul>
                        </div>
                    </div>
                    
                    <div class="qr-container">
                        <div class="qr-code">
                            <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://saintmomina.edu/payment&bgcolor=F0F8FF&color=0a0a2a" alt="QR Code for Fee Payment">
                        </div>
                        <p style="font-size: 1.1rem; margin-top: 15px; color: var(--white); font-weight: 500;">
                            Scan to Pay School Fees
                        </p>
                        
                        <div class="security-badges">
                            <div class="badge">
                                <i class="fas fa-lock"></i> 256-bit SSL
                            </div>
                            <div class="badge">
                                <i class="fas fa-shield-alt"></i> Secure Payment
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Portal Section -->
                <div class="portal-section">
                    <h3>Access Your Portal</h3>
                    <div class="portal-btns">
                        <button class="portal-btn student" id="studentPortalBtn2">
                            <i class="fas fa-user-graduate portal-icon"></i>
                            Student Portal
                        </button>
                        <button class="portal-btn teacher" id="teacherPortalBtn">
                            <i class="fas fa-chalkboard-teacher portal-icon"></i>
                            Teacher Portal
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer class="footer" id="footer">
        <div class="footer-content">
            <div class="footer-section">
                <h3>Contact Us</h3>
                <div class="contact-info">
                    <p><i class="fas fa-map-marker-alt"></i> Jainpur, Meerut Road, Uttar Pradesh 250001</p>
                    <p><i class="fas fa-envelope"></i> admissions@saintmomina.edu</p>
                    <p><i class="fas fa-phone"></i> 08171989806</p>
                    <p><i class="fas fa-clock"></i> Office Hours: 8:30 AM - 4:00 PM (Mon-Sat)</p>
                    <p><i class="fas fa-bus"></i> School Transport Available</p>
                </div>
                
                <div class="social-links">
                    <a href="#" class="social-link"><i class="fab fa-facebook-f"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-youtube"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
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
            </div>
            
            <div class="footer-section">
                <h3>Send a Message</h3>
                <form class="contact-form">
                    <input type="text" placeholder="Your Name" required>
                    <input type="email" placeholder="Your Email" required>
                    <input type="tel" placeholder="Phone Number">
                    <textarea placeholder="Your Message" rows="4" required></textarea>
                    <button type="submit">
                        <i class="fas fa-paper-plane"></i> Send Message
                    </button>
                </form>
            </div>
        </div>
        
        <div class="copyright">
            <p>&copy; 2023 Saint Momina School, Jainpur (Meerut Road). All rights reserved.</p>
            <p>Affiliated with CBSE New Delhi | Recognized by the Government of Uttar Pradesh</p>
        </div>
    </footer>
    
    <!-- Student Portal Modal -->
    <div class="modal" id="studentModal">
        <div class="modal-content">
            <span class="close-modal" id="closeStudentModal">&times;</span>
            <h2 class="modal-title">Student Portal</h2>
            <form class="modal-form" id="studentForm">
                <div class="form-group">
                    <label for="studentId">Student ID:</label>
                    <input type="text" id="studentId" required>
                </div>
                <div class="form-group">
                    <label for="studentName">Full Name:</label>
                    <input type="text" id="studentName" required>
                </div>
                <div class="form-group">
                    <label for="studentClass">Class:</label>
                    <input type="text" id="studentClass" required>
                </div>
                <div class="form-group">
                    <label for="studentSection">Section:</label>
                    <input type="text" id="studentSection" required>
                </div>
                <button type="submit" class="submit-btn">Access Portal</button>
            </form>
        </div>
    </div>
    
    <!-- Teacher Portal Modal -->
    <div class="modal" id="teacherModal">
        <div class="modal-content">
            <span class="close-modal" id="closeTeacherModal">&times;</span>
            <h2 class="modal-title">Teacher Portal</h2>
            <form class="modal-form" id="teacherForm">
                <div class="form-group">
                    <label for="teacherId">Teacher ID:</label>
                    <input type="text" id="teacherId" required>
                </div>
                <div class="form-group">
                    <label for="teacherName">Full Name:</label>
                    <input type="text" id="teacherName" required>
                </div>
                <div class="form-group">
                    <label for="teacherContact">Contact Number:</label>
                    <input type="tel" id="teacherContact" required>
                </div>
                <div class="form-group">
                    <label for="teacherDept">Department:</label>
                    <input type="text" id="teacherDept" required>
                </div>
                <button type="submit" class="submit-btn">Access Portal</button>
            </form>
        </div>
    </div>
    
    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.querySelector('.header');
            if (window.scrollY > 100) {
                header.style.padding = '15px 5%';
                header.style.boxShadow = '0 5px 20px rgba(0, 0, 0, 0.2)';
            } else {
                header.style.padding = '20px 5%';
                header.style.boxShadow = '0 10px 30px rgba(0, 0, 0, 0.15)';
            }
        });
        
        // Scroll down button
        document.querySelector('.scroll-down').addEventListener('click', function() {
            document.getElementById('about').scrollIntoView({ behavior: 'smooth' });
        });
        
        // Form submission
        const contactForm = document.querySelector('.contact-form');
        if (contactForm) {
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Thank you for your message! We will contact you shortly.');
                contactForm.reset();
            });
        }
        
        // Portal Modals
        const studentModal = document.getElementById('studentModal');
        const teacherModal = document.getElementById('teacherModal');
        
        // Student Portal Buttons
        document.getElementById('studentPortalBtn').addEventListener('click', openStudentModal);
        document.getElementById('studentPortalBtn2').addEventListener('click', openStudentModal);
        
        // Teacher Portal Button
        document.getElementById('teacherPortalBtn').addEventListener('click', openTeacherModal);
        
        // Close buttons
        document.getElementById('closeStudentModal').addEventListener('click', closeStudentModal);
        document.getElementById('closeTeacherModal').addEventListener('click', closeTeacherModal);
        
        // Close modals when clicking outside
        window.addEventListener('click', function(e) {
            if (e.target === studentModal) {
                closeStudentModal();
            }
            if (e.target === teacherModal) {
                closeTeacherModal();
            }
        });
        
        function openStudentModal() {
            studentModal.style.display = 'flex';
            document.body.style.overflow = 'hidden';
        }
        
        function closeStudentModal() {
            studentModal.style.display = 'none';
            document.body.style.overflow = 'auto';
        }
        
        function openTeacherModal() {
            teacherModal.style.display = 'flex';
            document.body.style.overflow = 'hidden';
        }
        
        function closeTeacherModal() {
            teacherModal.style.display = 'none';
            document.body.style.overflow = 'auto';
        }
        
        // Form submissions
        document.getElementById('studentForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Student portal access request received. Redirecting to dashboard...');
            closeStudentModal();
        });
        
        document.getElementById('teacherForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Teacher portal access request received. Redirecting to dashboard...');
            closeTeacherModal();
        });
        
        // Animation on scroll
        const observerOptions = {
            threshold: 0.1
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animated');
                }
            });
        }, observerOptions);
        
        document.querySelectorAll('.section-card, .feature-card, .stat-card').forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(30px)';
            card.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
            observer.observe(card);
            
            card.classList.contains('animated') && 
            setTimeout(() => {
                card.style.opacity = '1';
                card.style.transform = 'translateY(0)';
            }, 200);
        });
    </script>
</body>
</html>
