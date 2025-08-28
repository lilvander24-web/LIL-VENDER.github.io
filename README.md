# LIL-VENDER.github.io
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LIL VANDER - Développeur Web | Yagoua, Cameroun</title>
    <meta name="description" content="LIL VANDER, jeune développeur web de 19 ans basé à Yagoua. Spécialisé en développement web moderne, passionné par l'innovation technologique au Cameroun.">
    <meta name="keywords" content="LIL VANDER, développeur web, Yagoua, Cameroun, programmeur, HTML, technologie, innovation">
    <meta name="author" content="LIL VANDER">
    
    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://lilvander.com/">
    <meta property="og:title" content="LIL VANDER - Jeune Développeur Web | Yagoua">
    <meta property="og:description" content="Découvrez le parcours de LIL VANDER, développeur web de 19 ans, pionnier du numérique à Yagoua.">
    
    <!-- Twitter -->
    <meta property="twitter:card" content="summary_large_image">
    <meta property="twitter:url" content="https://lilvander.com/">
    <meta property="twitter:title" content="LIL VANDER - Développeur Web">
    <meta property="twitter:description" content="Jeune développeur web passionné, basé à Yagoua, Cameroun.">
    
    <link rel="canonical" href="https://lilvander.com/">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Navigation */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
        }

        .navbar.scrolled {
            padding: 0.5rem 0;
            box-shadow: 0 2px 30px rgba(0, 0, 0, 0.15);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-link {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-link:hover {
            color: #667eea;
        }

        .nav-link::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            transition: width 0.3s ease;
        }

        .nav-link:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 20"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="1" fill="white" opacity="0.1"/><circle cx="75" cy="75" r="1" fill="white" opacity="0.1"/><circle cx="50" cy="10" r="0.5" fill="white" opacity="0.1"/></pattern></defs><rect width="100%" height="100%" fill="url(%23grain)"/></svg>');
            opacity: 0.3;
        }

        .hero-content {
            max-width: 800px;
            z-index: 2;
            position: relative;
        }

        .profile-image {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 5px solid rgba(255, 255, 255, 0.3);
            margin: 0 auto 2rem;
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            animation: pulse 2s infinite;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        }

        .hero h1 {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease 0.2s both;
        }

        .hero .subtitle {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .hero .description {
            font-size: 1.1rem;
            margin-bottom: 2rem;
            opacity: 0.8;
            animation: fadeInUp 1s ease 0.6s both;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease 0.8s both;
        }

        .btn {
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-primary {
            background: white;
            color: #667eea;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            border: 2px solid rgba(255, 255, 255, 0.3);
            backdrop-filter: blur(10px);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-3px);
        }

        /* About Section */
        .about {
            padding: 6rem 0;
            background: white;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .section-subtitle {
            text-align: center;
            font-size: 1.1rem;
            color: #666;
            margin-bottom: 4rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text {
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .about-text p {
            margin-bottom: 1.5rem;
        }

        .highlight {
            color: #667eea;
            font-weight: 600;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .stat-card {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: #667eea;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            color: #666;
            font-weight: 500;
        }

        /* Skills Section */
        .skills {
            padding: 6rem 0;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        .skill-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .skill-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .skill-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: #333;
        }

        .skill-description {
            color: #666;
            line-height: 1.6;
        }

        /* Projects Section */
        .projects {
            padding: 6rem 0;
            background: white;
        }

        .project-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 3rem;
            border-radius: 20px;
            text-align: center;
            margin: 2rem 0;
            box-shadow: 0 20px 40px rgba(102, 126, 234, 0.3);
        }

        .project-card h3 {
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .project-card p {
            font-size: 1.1rem;
            opacity: 0.9;
            margin-bottom: 2rem;
        }

        /* Contact Section */
        .contact {
            padding: 6rem 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .contact-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .contact-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .contact-title {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .contact-detail {
            opacity: 0.9;
        }

        /* Footer */
        .footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        /* Animations */
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero .subtitle {
                font-size: 1.1rem;
            }

            .about-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .profile-image {
                width: 150px;
                height: 150px;
                font-size: 3rem;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .container {
                padding: 0 1rem;
            }
        }

        /* Scroll animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease;
        }

        .fade-in.active {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar" id="navbar">
        <div class="nav-container">
            <div class="logo">LIL VANDER</div>
            <ul class="nav-menu">
                <li><a href="#home" class="nav-link">Accueil</a></li>
                <li><a href="#about" class="nav-link">À Propos</a></li>
                <li><a href="#skills" class="nav-link">Compétences</a></li>
                <li><a href="#projects" class="nav-link">Projets</a></li>
                <li><a href="#contact" class="nav-link">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <div class="profile-image">👨‍💻</div>
            <h1>LIL VANDER</h1>
            <p class="subtitle">Développeur Web • Yagoua, Cameroun</p>
            <p class="description">
                Jeune développeur passionné de 19 ans, pionnier du numérique à Yagoua.
                <br>Spécialisé en développement web moderne et innovation technologique.
            </p>
            <div class="cta-buttons">
                <a href="#about" class="btn btn-primary">
                    <span>🚀</span> Découvrir mon parcours
                </a>
                <a href="#contact" class="btn btn-secondary">
                    <span>💬</span> Me contacter
                </a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">À Propos de Moi</h2>
            <p class="section-subtitle">
                Découvrez mon parcours et ma passion pour le développement web
            </p>
            
            <div class="about-content fade-in">
                <div class="about-text">
                    <p>
                        Bonjour ! Je suis <span class="highlight">LIL VANDER</span>, un jeune développeur web de 19 ans 
                        basé à <span class="highlight">Yagoua, dans l'Extrême-Nord du Cameroun</span>.
                    </p>
                    <p>
                        Passionné par la technologie depuis mes 17 ans, j'ai commencé mon aventure dans le 
                        développement web avec <span class="highlight">HTML</span>. Mon objectif est de 
                        poursuivre mes études en informatique pour approfondir mes compétences.
                    </p>
                    <p>
                        En tant qu'élève au <span class="highlight">Lycée Bilingue de Yagoua</span>, 
                        je concilie mes études avec ma passion pour le code. J'ai déjà réalisé des sites web 
                        pour des amis et je rêve de <span class="highlight">développer l'écosystème numérique local</span>.
                    </p>
                    <p>
                        Ma vision est de contribuer à la transformation digitale de ma région en créant 
                        des solutions innovantes adaptées aux besoins locaux.
                    </p>
                </div>
            </div>

            <div class="stats-grid fade-in">
                <div class="stat-card">
                    <div class="stat-number">19</div>
                    <div class="stat-label">Ans</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">2+</div>
                    <div class="stat-label">Années d'expérience</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">100%</div>
                    <div class="stat-label">Motivation</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">∞</div>
                    <div class="stat-label">Ambition</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section class="skills" id="skills">
        <div class="container">
            <h2 class="section-title">Mes Compétences</h2>
            <p class="section-subtitle">
                Technologies et domaines dans lesquels je me spécialise
            </p>
            
            <div class="skills-grid fade-in">
                <div class="skill-card">
                    <div class="skill-icon">🌐</div>
                    <h3 class="skill-title">Développement Web</h3>
                    <p class="skill-description">
                        Création de sites web modernes avec HTML, CSS et JavaScript. 
                        Conception d'interfaces utilisateur attrayantes et responsives.
                    </p>
                </div>
                
                <div class="skill-card">
                    <div class="skill-icon">💡</div>
                    <h3 class="skill-title">Innovation Locale</h3>
                    <p class="skill-description">
                        Développement de solutions technologiques adaptées aux besoins 
                        spécifiques de la région de l'Extrême-Nord.
                    </p>
                </div>
                
                <div class="skill-card">
                    <div class="skill-icon">📚</div>
                    <h3 class="skill-title">Apprentissage Continu</h3>
                    <p class="skill-description">
                        Autodidacte passionné, toujours en quête de nouvelles connaissances 
                        et technologies émergentes dans le domaine du développement.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="projects" id="projects">
        <div class="container">
            <h2 class="section-title">Mes Projets</h2>
            <p class="section-subtitle">
                Réalisations et projets en cours de développement
            </p>
            
            <div class="project-card fade-in">
                <h3>🚀 Projets en Développement</h3>
                <p>
                    Je travaille actuellement sur plusieurs projets innovants qui verront le jour prochainement. 
                    Mon objectif est de créer des solutions web qui répondent aux besoins de ma communauté à Yagoua.
                </p>
                <a href="#contact" class="btn btn-secondary">Suivre mes projets</a>
            </div>
            
            <div class="project-card fade-in">
                <h3>💼 Expérience Client</h3>
                <p>
                    J'ai déjà réalisé des sites web pour des amis, leur permettant d'avoir une présence en ligne 
                    professionnelle. Chaque projet est une opportunité d'apprendre et de perfectionner mes compétences.
                </p>
                <a href="#contact" class="btn btn-secondary">Discuter de votre projet</a>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title" style="color: white;">Contactez-Moi</h2>
            <p class="section-subtitle" style="color: rgba(255,255,255,0.9);">
                Collaborons ensemble sur vos projets web
            </p>
            
            <div class="contact-info fade-in">
                <div class="contact-card">
                    <div class="contact-icon">📍</div>
                    <h3 class="contact-title">Localisation</h3>
                    <p class="contact-detail">Yagoua, Extrême-Nord<br>Cameroun</p>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">🎓</div>
                    <h3 class="contact-title">Formation</h3>
                    <p class="contact-detail">Lycée Bilingue de Yagoua<br>Futur élève en Informatique</p>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">💻</div>
                    <h3 class="contact-title">Spécialité</h3>
                    <p class="contact-detail">Développement Web<br>Innovation Technologique</p>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">🌟</div>
                    <h3 class="contact-title">Mission</h3>
                    <p class="contact-detail">Développer le numérique<br>à Yagoua</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2024 LIL VANDER. Tous droits réservés. | Développeur Web - Yagoua, Cameroun</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 100) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Fade in animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Dynamic typing effect for subtitle
        const subtitles = [
            "Développeur Web • Yagoua, Cameroun",
            "Élève Passionné • Innovation Locale",
            "Futur Ingénieur • Vision Numérique"
        ];

        let currentSubtitle = 0;
        const subtitleElement = document.querySelector('.hero .subtitle');

        function changeSubtitle() {
            subtitleElement.style.opacity = '0';
            setTimeout(() => {
                currentSubtitle = (currentSubtitle + 1) % subtitles.length;
                subtitleElement.textContent = subtitles[currentSubtitle];
                subtitleElement.style.opacity = '1';
            }, 300);
        }

        // Change subtitle every 4 seconds
        setInterval(changeSubtitle, 4000);

        // Add structured data for SEO
        const structuredData = {
            "@context": "https://schema.org",
            "@type": "Person",
            "name": "LIL VANDER",
            "age": 19,
            "birthDate": "2006-03-12",
            "birthPlace": "Yagoua, Cameroun",
            "currentLocation": "Yagoua, Cameroun",
            "jobTitle": "Développeur Web",
            "description": "Jeune développeur web de 19 ans, pionnier du numérique à Yagoua, spécialisé en développement web moderne.",
            "knowsAbout": ["HTML", "Développement Web", "Innovation Technologique"],
            "alumniOf": "Lycée Bilingue de Yagoua",
            "nationality": "Camerounaise",
            "gender": "Male"
        };

        // Add to head
        const script = document.createElement('script');
        script.type = 'application/ld+json';
        script.textContent = JSON.stringify(structuredData);
        document.head.appendChild(script);
    </script>
</body>
</html>
