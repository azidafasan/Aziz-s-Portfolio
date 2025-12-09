# Aziz-s-Portfolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Azid Basha. S | IT Services & Digital Solutions</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #7c3aed;
            --accent: #06b6d4;
            --success: #10b981;
            --danger: #ef4444;
            --warning: #f59e0b;
            --dark: #0f172a;
            --dark-light: #1e293b;
            --light: #f8fafc;
            --glass-bg: rgba(255, 255, 255, 0.05);
            --glass-border: rgba(255, 255, 255, 0.1);
            --glass-border-hover: rgba(255, 255, 255, 0.2);
            --shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            --shadow-light: 0 4px 16px rgba(0, 0, 0, 0.2);
            --transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: 80px;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #334155 100%);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
            min-height: 100vh;
            background-attachment: fixed;
        }

        h1, h2, h3, h4, h5 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            line-height: 1.2;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Glass Effect */
        .glass {
            background: var(--glass-bg);
            backdrop-filter: blur(12px) saturate(180%);
            -webkit-backdrop-filter: blur(12px) saturate(180%);
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            box-shadow: var(--shadow);
        }

        .glass-hover {
            transition: var(--transition);
        }

        .glass-hover:hover {
            transform: translateY(-8px);
            border-color: var(--glass-border-hover);
            box-shadow: var(--shadow-light);
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            padding: 1.5rem 0;
            transition: var(--transition);
        }

        header.scrolled {
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(15px) saturate(180%);
            padding: 1rem 0;
            box-shadow: 0 5px 30px rgba(0, 0, 0, 0.3);
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
        }

        .logo span {
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            font-size: 1rem;
            transition: var(--transition);
            position: relative;
            opacity: 0.9;
        }

        .nav-links a:hover {
            color: var(--accent);
            opacity: 1;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            background: none;
            border: none;
            color: white;
            cursor: pointer;
            z-index: 1001;
        }

        .cta-button {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 12px 28px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 1rem;
            gap: 8px;
            white-space: nowrap;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(37, 99, 235, 0.3);
        }

        .cta-button.secondary {
            background: transparent;
            border: 2px solid var(--glass-border);
        }

        .cta-button.secondary:hover {
            border-color: var(--accent);
            background: rgba(6, 182, 212, 0.1);
        }

        .whatsapp-button {
            background: linear-gradient(135deg, #25D366, #128C7E);
        }

        .whatsapp-button:hover {
            box-shadow: 0 15px 30px rgba(37, 211, 102, 0.3);
        }

        /* Hero Section */
        .hero {
            padding: 160px 0 100px;
            position: relative;
            overflow: hidden;
            min-height: 100vh;
            display: flex;
            align-items: center;
        }

        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
        }

        .hero-bg::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 50%, rgba(37, 99, 235, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, rgba(124, 58, 237, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 40% 80%, rgba(6, 182, 212, 0.1) 0%, transparent 50%);
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
            position: relative;
            z-index: 2;
        }

        .hero-text h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(to right, #fff, var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .hero-text h2 {
            font-size: 1.5rem;
            color: var(--accent);
            margin-bottom: 1.5rem;
            font-weight: 500;
        }

        .hero-text p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            line-height: 1.8;
        }

        .highlight {
            color: var(--accent);
            font-weight: 600;
        }

        .service-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .service-tag {
            background: rgba(6, 182, 212, 0.1);
            border: 1px solid var(--accent);
            border-radius: 50px;
            padding: 8px 20px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: var(--transition);
        }

        .service-tag:hover {
            transform: translateY(-3px);
            background: rgba(6, 182, 212, 0.2);
        }

        .hero-image {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .floating-card {
            width: 380px;
            height: 380px;
            border-radius: 30px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            animation: float 6s ease-in-out infinite;
            overflow: hidden;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            33% { transform: translateY(-20px) rotate(1deg); }
            66% { transform: translateY(-10px) rotate(-1deg); }
        }

        .floating-card::before {
            content: '';
            position: absolute;
            width: 420px;
            height: 420px;
            border-radius: 30px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            opacity: 0.3;
            animation: pulse 4s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.3; }
            50% { transform: scale(1.05); opacity: 0.4; }
        }

        .floating-card i {
            font-size: 10rem;
            color: white;
            z-index: 2;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            margin-top: 2.5rem;
            flex-wrap: wrap;
        }

        /* Sections */
        section {
            padding: 100px 0;
            position: relative;
        }

        .section-title {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-title h2 {
            font-size: 2.8rem;
            display: inline-block;
            position: relative;
            margin-bottom: 1rem;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background: var(--accent);
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }

        .section-title p {
            font-size: 1.2rem;
            color: #94a3b8;
            max-width: 600px;
            margin: 2rem auto 0;
        }

        /* Cards */
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .card {
            padding: 2.5rem;
            transition: var(--transition);
        }

        .card-icon {
            font-size: 3rem;
            color: var(--accent);
            margin-bottom: 1.5rem;
        }

        .card h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: white;
        }

        .card p {
            color: #94a3b8;
            margin-bottom: 1.5rem;
            line-height: 1.7;
        }

        .feature-list {
            list-style: none;
            margin-top: 1.5rem;
        }

        .feature-list li {
            margin-bottom: 0.8rem;
            padding-left: 1.8rem;
            position: relative;
            color: #cbd5e1;
        }

        .feature-list li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--accent);
            font-weight: bold;
        }

        /* Stats */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }

        .stat-card {
            text-align: center;
            padding: 2rem;
        }

        .stat-value {
            font-size: 3rem;
            font-weight: 700;
            background: linear-gradient(135deg, var(--accent), var(--primary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            color: #94a3b8;
            font-size: 1rem;
        }

        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            padding: 2rem;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--accent), var(--primary));
        }

        .project-badge {
            display: inline-block;
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .badge-completed {
            background: rgba(16, 185, 129, 0.2);
            color: var(--success);
            border: 1px solid var(--success);
        }

        .badge-ongoing {
            background: rgba(6, 182, 212, 0.2);
            color: var(--accent);
            border: 1px solid var(--accent);
        }

        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin: 1.5rem 0;
        }

        .tech-tag {
            background: rgba(255, 255, 255, 0.1);
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.8rem;
            color: #cbd5e1;
        }

        /* Timeline */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 4rem auto;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100%;
            background: linear-gradient(to bottom, var(--accent), transparent);
        }

        .timeline-item {
            margin-bottom: 3rem;
            position: relative;
            width: calc(50% - 2rem);
        }

        .timeline-item:nth-child(odd) {
            margin-right: calc(50% + 2rem);
        }

        .timeline-item:nth-child(even) {
            margin-left: calc(50% + 2rem);
        }

        .timeline-dot {
            position: absolute;
            top: 0;
            right: -1rem;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: var(--accent);
            border: 4px solid var(--dark);
        }

        .timeline-item:nth-child(even) .timeline-dot {
            right: auto;
            left: -1rem;
        }

        .timeline-content {
            padding: 1.5rem;
        }

        .timeline-content h3 {
            color: var(--accent);
            margin-bottom: 0.5rem;
        }

        .timeline-date {
            color: #94a3b8;
            font-weight: 500;
            margin-bottom: 0.5rem;
            font-size: 0.9rem;
        }

        /* Skills */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .skill-category {
            padding: 2rem;
        }

        .skill-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .skill-icon {
            width: 60px;
            height: 60px;
            border-radius: 15px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
        }

        /* Contact Form */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            margin-top: 3rem;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 1.5rem;
        }

        .contact-icon {
            width: 60px;
            height: 60px;
            border-radius: 15px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            flex-shrink: 0;
        }

        .contact-form {
            padding: 2.5rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: #cbd5e1;
        }

        .form-control {
            width: 100%;
            padding: 14px 18px;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid var(--glass-border);
            border-radius: 12px;
            color: white;
            font-family: 'Poppins', sans-serif;
            transition: var(--transition);
            font-size: 1rem;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--accent);
            background: rgba(255, 255, 255, 0.1);
            box-shadow: 0 0 0 3px rgba(6, 182, 212, 0.1);
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        select.form-control {
            appearance: none;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='16' fill='%2394a3b8' viewBox='0 0 16 16'%3E%3Cpath d='M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z'/%3E%3C/svg%3E");
            background-repeat: no-repeat;
            background-position: right 18px center;
            background-size: 16px;
            padding-right: 45px;
        }

        /* Footer */
        footer {
            padding: 4rem 0 2rem;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            margin-top: 4rem;
            background: rgba(15, 23, 42, 0.5);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 2rem 0 3rem;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 55px;
            height: 55px;
            border-radius: 50%;
            background: var(--glass-bg);
            color: white;
            font-size: 1.3rem;
            transition: var(--transition);
            text-decoration: none;
            border: 1px solid var(--glass-border);
        }

        .social-link:hover {
            transform: translateY(-5px);
            border-color: var(--accent);
        }

        .social-link.whatsapp:hover {
            background: #25D366;
        }

        .social-link.email:hover {
            background: var(--primary);
        }

        .social-link.phone:hover {
            background: var(--accent);
        }

        .copyright {
            color: #64748b;
            font-size: 0.9rem;
            margin-top: 2rem;
            line-height: 1.6;
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes slideInLeft {
            from { opacity: 0; transform: translateX(-50px); }
            to { opacity: 1; transform: translateX(0); }
        }

        @keyframes slideInRight {
            from { opacity: 0; transform: translateX(50px); }
            to { opacity: 1; transform: translateX(0); }
        }

        .animate-on-scroll {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }

        .animate-on-scroll.animated {
            opacity: 1;
            transform: translateY(0);
        }

        /* Responsive Design */
        @media (max-width: 1200px) {
            .hero-text h1 {
                font-size: 3rem;
            }
        }

        @media (max-width: 992px) {
            .hero-content,
            .contact-container {
                grid-template-columns: 1fr;
                gap: 3rem;
            }

            .timeline::before {
                left: 30px;
            }

            .timeline-item {
                width: calc(100% - 70px);
                margin-left: 70px !important;
                margin-right: 0 !important;
            }

            .timeline-dot {
                left: 21px !important;
                right: auto !important;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .mobile-menu-btn {
                display: block;
            }

            .mobile-menu {
                position: fixed;
                top: 0;
                right: -100%;
                width: 85%;
                max-width: 400px;
                height: 100vh;
                background: rgba(15, 23, 42, 0.98);
                backdrop-filter: blur(20px);
                padding: 100px 40px 40px;
                transition: var(--transition);
                z-index: 999;
                border-left: 1px solid rgba(255, 255, 255, 0.1);
            }

            .mobile-menu.active {
                right: 0;
            }

            .mobile-menu .nav-links {
                display: flex;
                flex-direction: column;
                gap: 2rem;
            }

            .mobile-menu .nav-links a {
                font-size: 1.3rem;
                opacity: 0.8;
            }

            .mobile-menu .nav-links a:hover {
                opacity: 1;
                color: var(--accent);
            }

            .close-menu {
                position: absolute;
                top: 30px;
                right: 30px;
                font-size: 1.5rem;
                background: none;
                border: none;
                color: white;
                cursor: pointer;
            }

            .hero-text h1 {
                font-size: 2.5rem;
            }

            .section-title h2 {
                font-size: 2.2rem;
            }

            .card-grid,
            .projects-grid,
            .skills-grid {
                grid-template-columns: 1fr;
            }

            .floating-card {
                width: 300px;
                height: 300px;
            }

            .floating-card i {
                font-size: 8rem;
            }
        }

        @media (max-width: 480px) {
            .hero-text h1 {
                font-size: 2rem;
            }

            .section-title h2 {
                font-size: 1.8rem;
            }

            .hero-buttons {
                flex-direction: column;
            }

            .cta-button {
                width: 100%;
                justify-content: center;
            }
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }

        ::-webkit-scrollbar-track {
            background: rgba(15, 23, 42, 0.5);
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(to bottom, var(--accent), var(--primary));
            border-radius: 5px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(to bottom, var(--primary), var(--secondary));
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header id="header">
        <div class="container">
            <nav class="navbar">
                <a href="#home" class="logo">Azid<span>.</span></a>
                
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#founder">Founder</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#timeline">Experience</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                
                <button class="mobile-menu-btn" id="menuBtn">
                    <i class="fas fa-bars"></i>
                </button>
                
                <a href="https://wa.me/919014749722?text=Hi%20Azid,%20I'm%20interested%20in%20your%20services" 
                   target="_blank" class="cta-button whatsapp-button">
                    <i class="fab fa-whatsapp"></i> WhatsApp
                </a>
            </nav>
        </div>
    </header>

    <!-- Mobile Menu -->
    <div class="mobile-menu" id="mobileMenu">
        <button class="close-menu" id="closeMenu">
            <i class="fas fa-times"></i>
        </button>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#founder">Founder</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#timeline">Experience</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </div>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-bg"></div>
        <div class="container">
            <div class="hero-content animate-on-scroll">
                <div class="hero-text">
                    <h1>Azid Basha. S</h1>
                    <h2>IT Services & Digital Solutions Specialist</h2>
                    <p>Founder of <span class="highlight">Bright Future Infotech IT Services</span>, providing innovative digital solutions including <span class="highlight">inbound call management, chat process support, and professional web design & development</span>.</p>
                    
                    <div class="service-tags">
                        <span class="service-tag"><i class="fas fa-phone-volume"></i> Inbound Call Services</span>
                        <span class="service-tag"><i class="fas fa-comments"></i> Chat Process Support</span>
                        <span class="service-tag"><i class="fas fa-code"></i> Web Design & Development</span>
                    </div>
                    
                    <div class="hero-buttons">
                        <a href="#contact" class="cta-button">
                            <i class="fas fa-rocket"></i> Start a Project
                        </a>
                        <a href="https://wa.me/919014749722?text=Hi%20Azid,%20I'm%20interested%20in%20your%20services" 
                           target="_blank" class="cta-button whatsapp-button">
                            <i class="fab fa-whatsapp"></i> Chat on WhatsApp
                        </a>
                        <a href="#projects" class="cta-button secondary">
                            <i class="fas fa-eye"></i> View Projects
                        </a>
                    </div>
                </div>
                
                <div class="hero-image">
                    <div class="floating-card">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Services</h2>
                <p>Professional IT Services for Your Business Growth</p>
            </div>
            
            <div class="card-grid">
                <div class="card glass glass-hover">
                    <div class="card-icon">
                        <i class="fas fa-phone-volume"></i>
                    </div>
                    <h3>Inbound Call Services</h3>
                    <p>Professional inbound call handling and customer support services to manage your customer inquiries efficiently.</p>
                    
                    <ul class="feature-list">
                        <li>24/7 Customer Support</li>
                        <li>Multi-language Support</li>
                        <li>Lead Qualification & Management</li>
                        <li>Appointment Scheduling</li>
                        <li>Technical Support Calls</li>
                        <li>Call Analytics & Reporting</li>
                    </ul>
                </div>
                
                <div class="card glass glass-hover">
                    <div class="card-icon">
                        <i class="fas fa-comment-dots"></i>
                    </div>
                    <h3>Chat Process Support</h3>
                    <p>Live chat support and messaging services to engage with your customers in real-time across platforms.</p>
                    
                    <ul class="feature-list">
                        <li>Live Chat Support</li>
                        <li>Email & Ticketing Support</li>
                        <li>Social Media Messaging</li>
                        <li>Chatbot Integration Support</li>
                        <li>Customer Query Resolution</li>
                        <li>Multi-channel Support</li>
                    </ul>
                </div>
                
                <div class="card glass glass-hover">
                    <div class="card-icon">
                        <i class="fas fa-code"></i>
                    </div>
                    <h3>Web Design & Development</h3>
                    <p>Custom website design and development services to establish your digital presence effectively.</p>
                    
                    <ul class="feature-list">
                        <li>Responsive Web Design</li>
                        <li>E-commerce Websites</li>
                        <li>Business Portfolio Sites</li>
                        <li>Landing Pages</li>
                        <li>Website Maintenance</li>
                        <li>SEO Optimization</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section id="stats">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-card glass animate-on-scroll">
                    <div class="stat-value">7+</div>
                    <div class="stat-label">Years Experience</div>
                </div>
                <div class="stat-card glass animate-on-scroll">
                    <div class="stat-value">50+</div>
                    <div class="stat-label">Projects Completed</div>
                </div>
                <div class="stat-card glass animate-on-scroll">
                    <div class="stat-value">15+</div>
                    <div class="stat-label">Happy Clients</div>
                </div>
                <div class="stat-card glass animate-on-scroll">
                    <div class="stat-value">100%</div>
                    <div class="stat-label">Client Satisfaction</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <div class="section-title">
                <h2>Recent Projects</h2>
                <p>Successfully Delivered Solutions</p>
            </div>
            
            <div class="projects-grid">
                <div class="project-card glass glass-hover animate-on-scroll">
                    <div class="project-badge badge-completed">Completed</div>
                    <h3>Ashvara Technologies</h3>
                    <h4>Virtual Assistant Implementation</h4>
                    <p>Successfully implemented a virtual assistant solution for Ashvara Technologies, enhancing their customer engagement and support automation.</p>
                    
                    <div class="tech-tags">
                        <span class="tech-tag">Virtual Assistant</span>
                        <span class="tech-tag">AI Integration</span>
                        <span class="tech-tag">Customer Support</span>
                        <span class="tech-tag">Automation</span>
                    </div>
                    
                    <p><strong>Key Achievements:</strong></p>
                    <ul class="feature-list">
                        <li>Reduced response time by 60%</li>
                        <li>24/7 customer query handling</li>
                        <li>Multi-language support implementation</li>
                        <li>Seamless integration with existing systems</li>
                    </ul>
                </div>
                
                <div class="project-card glass glass-hover animate-on-scroll">
                    <div class="project-badge badge-ongoing">Ongoing</div>
                    <h3>Mobile App Installation Project</h3>
                    <h4>Cred & Tide Apps via 3rd Party</h4>
                    <p>Currently engaged with a 3rd party project for mobile app installation services, focusing on Cred and Tide applications for customer acquisition.</p>
                    
                    <div class="tech-tags">
                        <span class="tech-tag">Mobile Apps</span>
                        <span class="tech-tag">Cred App</span>
                        <span class="tech-tag">Tide App</span>
                        <span class="tech-tag">Customer Onboarding</span>
                    </div>
                    
                    <p><strong>Project Scope:</strong></p>
                    <ul class="feature-list">
                        <li>App installation guidance & support</li>
                        <li>Customer credential setup assistance</li>
                        <li>Technical troubleshooting</li>
                        <li>Customer education & training</li>
                        <li>Performance tracking & reporting</li>
                    </ul>
                </div>
                
                <div class="project-card glass glass-hover animate-on-scroll">
                    <div class="project-badge badge-completed">Completed</div>
                    <h3>Web Portfolio Development</h3>
                    <h4>Professional Online Presence</h4>
                    <p>Designed and developed multiple professional portfolio websites for clients, enhancing their online visibility and business credibility.</p>
                    
                    <div class="tech-tags">
                        <span class="tech-tag">HTML/CSS/JS</span>
                        <span class="tech-tag">Responsive Design</span>
                        <span class="tech-tag">UI/UX</span>
                        <span class="tech-tag">Glass Morphism</span>
                    </div>
                    
                    <p><strong>Features Delivered:</strong></p>
                    <ul class="feature-list">
                        <li>Mobile-responsive designs</li>
                        <li>Contact forms with lead capture</li>
                        <li>Portfolio showcase sections</li>
                        <li>Social media integration</li>
                        <li>Fast loading optimization</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Founder Section -->
    <section id="founder">
        <div class="container">
            <div class="section-title">
                <h2>Founder's Journey</h2>
                <p>Building Bright Future Infotech from Ground Up</p>
            </div>
            
            <div class="card glass animate-on-scroll">
                <div class="card-icon">
                    <i class="fas fa-rocket"></i>
                </div>
                <h3>Azid Basha. S</h3>
                <p><strong>Founder, Bright Future Infotech IT Services</strong></p>
                <p>With 7+ years of experience in IT services and digital solutions, I established Bright Future Infotech to provide specialized services in inbound call management, chat support, and web development.</p>
                
                <ul class="feature-list">
                    <li>Successfully completed projects for Ashvara Technologies and other clients</li>
                    <li>Currently engaged in mobile app installation project with 3rd party</li>
                    <li>Expert in implementing virtual assistant solutions</li>
                    <li>Skilled in web design & development using modern technologies</li>
                    <li>Focus on delivering measurable results for clients</li>
                    <li>Strong background in IT recruitment & talent management</li>
                </ul>
                
                <div class="hero-buttons" style="margin-top: 2rem;">
                    <a href="#contact" class="cta-button">
                        <i class="fas fa-handshake"></i> Work With Me
                    </a>
                    <a href="tel:+919014749722" class="cta-button secondary">
                        <i class="fas fa-phone"></i> Call Now
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <div class="section-title">
                <h2>Technical Expertise</h2>
                <p>Comprehensive Skill Set for Digital Solutions</p>
            </div>
            
            <div class="skills-grid">
                <div class="skill-category glass glass-hover animate-on-scroll">
                    <div class="skill-header">
                        <div class="skill-icon">
                            <i class="fas fa-robot"></i>
                        </div>
                        <h3>AI & Technology</h3>
                    </div>
                    <ul class="feature-list">
                        <li>AI-Enhanced Solutions Implementation</li>
                        <li>Machine Learning Algorithms</li>
                        <li>Predictive Analytics</li>
                        <li>Automated Screening Systems</li>
                        <li>Virtual Assistant Development</li>
                    </ul>
                </div>
                
                <div class="skill-category glass glass-hover animate-on-scroll">
                    <div class="skill-header">
                        <div class="skill-icon">
                            <i class="fas fa-laptop-code"></i>
                        </div>
                        <h3>Web Development</h3>
                    </div>
                    <ul class="feature-list">
                        <li>HTML5, CSS3, JavaScript</li>
                        <li>Responsive Web Design</li>
                        <li>UI/UX Design Principles</li>
                        <li>Frontend Development</li>
                        <li>Glass Morphism Effects</li>
                    </ul>
                </div>
                
                <div class="skill-category glass glass-hover animate-on-scroll">
                    <div class="skill-header">
                        <div class="skill-icon">
                            <i class="fas fa-comments"></i>
                        </div>
                        <h3>Customer Support</h3>
                    </div>
                    <ul class="feature-list">
                        <li>Inbound Call Management</li>
                        <li>Live Chat Support</li>
                        <li>Multi-channel Support</li>
                        <li>Customer Query Resolution</li>
                        <li>Technical Support</li>
                    </ul>
                </div>
                
                <div class="skill-category glass glass-hover animate-on-scroll">
                    <div class="skill-header">
                        <div class="skill-icon">
                            <i class="fas fa-chart-line"></i>
                        </div>
                        <h3>Business Management</h3>
                    </div>
                    <ul class="feature-list">
                        <li>Entrepreneurial Leadership</li>
                        <li>Client Relationship Management</li>
                        <li>Project Management</li>
                        <li>Vendor Coordination</li>
                        <li>Business Development</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Timeline -->
    <section id="timeline">
        <div class="container">
            <div class="section-title">
                <h2>Professional Experience</h2>
                <p>Career Journey & Milestones</p>
            </div>
            
            <div class="timeline">
                <div class="timeline-item animate-on-scroll">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content glass">
                        <div class="timeline-date">June 2023 - Present</div>
                        <h3>Founder & Strategic Leader</h3>
                        <h4>Bright Future Infotech IT Services</h4>
                        <p>Established IT services and recruitment firm integrating AI solutions. Developed proprietary recruitment tools, training programs, and web design services.</p>
                    </div>
                </div>
                
                <div class="timeline-item animate-on-scroll">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content glass">
                        <div class="timeline-date">Dec 2021 - May 2023</div>
                        <h3>Senior Recruitment Consultant</h3>
                        <h4>Quess Corp LTD, Bangalore</h4>
                        <p>Managed senior-level IT recruitment across multiple technology domains. Handled vendor coordination and maintained SLA compliance for major IT clients.</p>
                    </div>
                </div>
                
                <div class="timeline-item animate-on-scroll">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content glass">
                        <div class="timeline-date">Nov 2017 - Nov 2021</div>
                        <h3>Technical Recruiter</h3>
                        <h4>LOTUS INFOTECH SOLUTIONS, Bangalore</h4>
                        <p>Managed full recruitment lifecycle for IT positions across diverse technologies. Coordinated with vendors and maintained client relationships.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Get In Touch</h2>
                <p>Ready to Start Your Project? Contact Me Today</p>
            </div>
            
            <div class="contact-container">
                <div class="contact-info animate-on-scroll">
                    <div class="card glass">
                        <h3>Contact Information</h3>
                        <p>Get in touch for inbound call services, chat support, or web development projects. Quick response guaranteed.</p>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <h4>Phone / WhatsApp</h4>
                                <p>+91-9014749722</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h4>Email</h4>
                                <p>brightfuture.infotechs@gmail.com</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h4>Location</h4>
                                <p>Madanapalli, Andhra Pradesh, India</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-clock"></i>
                            </div>
                            <div>
                                <h4>Business Hours</h4>
                                <p>Monday - Saturday: 9:00 AM - 7:00 PM IST</p>
                            </div>
                        </div>
                        
                        <div class="hero-buttons" style="margin-top: 2rem;">
                            <a href="https://wa.me/919014749722?text=Hi%20Azid,%20I'm%20interested%20in%20your%20services" 
                               target="_blank" class="cta-button whatsapp-button">
                                <i class="fab fa-whatsapp"></i> WhatsApp Now
                            </a>
                            <a href="tel:+919014749722" class="cta-button">
                                <i class="fas fa-phone"></i> Call Now
                            </a>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form glass animate-on-scroll">
                    <h3>Send a Message</h3>
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Full Name *</label>
                            <input type="text" id="name" class="form-control" placeholder="Your Name" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email Address *</label>
                            <input type="email" id="email" class="form-control" placeholder="your.email@example.com" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="phone">Phone Number</label>
                            <input type="tel" id="phone" class="form-control" placeholder="Your Phone Number">
                        </div>
                        
                        <div class="form-group">
                            <label for="service">Service Interested In *</label>
                            <select id="service" class="form-control" required>
                                <option value="">Select a service</option>
                                <option value="inbound">Inbound Call Services</option>
                                <option value="chat">Chat Process Support</option>
                                <option value="web">Web Design & Development</option>
                                <option value="consulting">IT Consulting</option>
                                <option value="other">Other Services</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Project Details *</label>
                            <textarea id="message" class="form-control" placeholder="Tell me about your project requirements, timeline, and budget..." required rows="5"></textarea>
                        </div>
                        
                        <button type="submit" class="cta-button" style="width: 100%;">
                            <i class="fas fa-paper-plane"></i> Send Message
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <a href="#home" class="logo" style="font-size: 2rem; margin-bottom: 1rem;">Bright<span>Future</span>.Infotech</a>
            
            <p style="color: #94a3b8; max-width: 600px; margin: 0 auto 2rem;">
                Professional IT Services: Inbound Calls • Chat Support • Web Development
            </p>
            
            <div class="social-links">
                <a href="https://wa.me/919014749722?text=Hi%20Azid,%20I'm%20interested%20in%20your%20services" 
                   target="_blank" class="social-link whatsapp" title="WhatsApp">
                    <i class="fab fa-whatsapp"></i>
                </a>
                <a href="tel:+919014749722" class="social-link phone" title="Call">
                    <i class="fas fa-phone"></i>
                </a>
                <a href="mailto:brightfuture.infotechs@gmail.com" class="social-link email" title="Email">
                    <i class="fas fa-envelope"></i>
                </a>
            </div>
            
            <div class="copyright">
                <p>© 2024 Bright Future Infotech IT Services. All Rights Reserved.</p>
                <p>Founder: Azid Basha. S | Contact: +91-9014749722 | Email: brightfuture.infotechs@gmail.com</p>
                <p>Designed to attract clients and generate quality leads for IT services.</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // Mobile Menu Toggle
        const menuBtn = document.getElementById('menuBtn');
        const closeMenu = document.getElementById('closeMenu');
        const mobileMenu = document.getElementById('mobileMenu');
        const mobileLinks = document.querySelectorAll('.mobile-menu a');
        
        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.add('active');
            document.body.style.overflow = 'hidden';
        });
        
        closeMenu.addEventListener('click', () => {
            mobileMenu.classList.remove('active');
            document.body.style.overflow = 'auto';
        });
        
        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.remove('active');
                document.body.style.overflow = 'auto';
            });
        });
        
        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    const headerHeight = document.querySelector('header').offsetHeight;
                    const targetPosition = targetElement.offsetTop - headerHeight - 20;
                    
                    window.scrollTo({
                        top: targetPosition,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Form submission
        const contactForm = document.getElementById('contactForm');
        
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const phone = document.getElementById('phone').value;
            const service = document.getElementById('service').value;
            const message = document.getElementById('message').value;
            
            // Create the email body
            const emailBody = `Name: ${name}%0D%0AEmail: ${email}%0D%0APhone: ${phone}%0D%0AService: ${service}%0D%0AMessage: ${message}`;
            
            // Create mailto link
            const mailtoLink = `mailto:brightfuture.infotechs@gmail.com?subject=New Project Inquiry from ${name}&body=${emailBody}`;
            
            // Open email client
            window.open(mailtoLink, '_blank');
            
            // Show success message
            alert('Thank you for your message! I\'ll get back to you within 24 hours. An email has been pre-filled for your convenience.');
            
            // Reset form
            contactForm.reset();
        });
        
        // Scroll animations
        const animateElements = document.querySelectorAll('.animate-on-scroll');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animated');
                }
            });
        }, {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        });
        
        animateElements.forEach(element => {
            observer.observe(element);
        });
        
        // Initialize animations on load
        window.addEventListener('load', () => {
            // Add animation class to hero elements
            const heroContent = document.querySelector('.hero-content');
            if (heroContent) {
                heroContent.classList.add('animated');
            }
            
            // Trigger scroll to update header
            window.dispatchEvent(new Event('scroll'));
        });
        
        // Floating card interaction
        const floatingCard = document.querySelector('.floating-card');
        if (floatingCard) {
            floatingCard.addEventListener('mouseenter', () => {
                floatingCard.style.animation = 'float 3s ease-in-out infinite';
            });
            
            floatingCard.addEventListener('mouseleave', () => {
                floatingCard.style.animation = 'float 6s ease-in-out infinite';
            });
        }
        
        // Service tags hover effect
        const serviceTags = document.querySelectorAll('.service-tag');
        serviceTags.forEach(tag => {
            tag.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-5px) scale(1.05)';
            });
            
            tag.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0) scale(1)';
            });
        });
        
        // Card hover effects
        const glassCards = document.querySelectorAll('.glass-hover');
        glassCards.forEach(card => {
            card.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-10px)';
                this.style.boxShadow = '0 20px 40px rgba(0, 0, 0, 0.4)';
            });
            
            card.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0)';
                this.style.boxShadow = '0 8px 32px rgba(0, 0, 0, 0.3)';
            });
        });
    </script>
</body>
</html>
