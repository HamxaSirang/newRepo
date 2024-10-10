<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title id="pageTitle">HR Development</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: sans-serif;
        }

        .navbar {
            background-color: #333;
            color: #fff;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo img {
            width: 50px;
            height: 50px;
            margin-right: 5px;
        }

        .logo h1 {
            margin: 0;
            font-size: 22px;
            color: white;
            display: flex;
            align-items: center;
        }

        .nav-container {
            display: flex;
            align-items: center;
        }

        .nav-links {
            display: flex;
            list-style: none;
            margin: 0;
            padding: 0;
        }

        .nav-links li {
            margin-right: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: #fff;
            font-size: 16px;
            transition: color 0.3s ease, background-color 0.3s ease;
        }

        .nav-links a:hover {
            color: #333;
            background-color: #fff;
            padding: 5px 10px;
            border-radius: 5px;
        }

        .search-bar {
            display: flex;
            align-items: center;
            background-color: #f1f1f1;
            padding: 5px 10px;
            border-radius: 20px;
            margin-left: 20px;
        }

        .search-bar input[type="text"] {
            border: none;
            outline: none;
            background: transparent;
            padding: 5px 10px;
            font-size: 14px;
            width: 150px;
        }

        .search-bar input[type="text"]::placeholder {
            color: #aaa;
        }

        .search-icon {
            background-color: #00b3ff;
            border: none;
            color: white;
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.2s ease;
        }

        .search-icon:hover {
            background-color: #005f99;
            transform: scale(1.05);
        }

        .language-selector {
            display: flex;
            align-items: center;
            margin-left: 20px;
        }

        .language-selector select {
            background-color: #f1f1f1;
            color: #333;
            border: 1px solid #ccc;
            border-radius: 20px;
            padding: 5px 10px;
            font-size: 14px;
            cursor: pointer;
            transition: background-color 0.3s ease, border-color 0.3s ease;
        }

        .language-selector select:hover {
            background-color: #ddd;
            border-color: #00b3ff;
        }

        .background {
            position: relative;
            height: 500px;
            width: 100%;
        }

        .background img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .short_b {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 97.8%;
            background: rgba(46, 164, 255, 0.62);
            color: white;
            font-size: 30px;
            font-family: 'Arial', sans-serif;
            text-align: center;
            padding: 15px;
            z-index: 1;
            height: 55px;
        }

        .about-section {
            padding: 50px;
            background-color: #f9f9f9;
            text-align: center;
        }

        .about-section h1 {
            font-size: 36px;
            color: #333;
            margin-bottom: 20px;
        }

        .about-section p {
            font-size: 18px;
            color: #555;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.6;
        }

        footer {
            background-color: #333;
            color: #fff;
            padding: 20px 40px;
            font-size: 14px;
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            flex-wrap: wrap;
        }

        footer .footer-section {
            flex: 1;
            margin: 20px;
            min-width: 150px;
        }

        footer .footer-section h3 {
            margin-bottom: 10px;
            font-size: 16px;
            color: white;
        }

        footer .footer-section ul {
            list-style-type: none;
            padding: 0;
        }

        footer .footer-section ul li {
            margin-bottom: 8px;
        }

        footer .footer-section ul li a {
            color: #fff;
            text-decoration: none;
        }

        footer .footer-section ul li a:hover {
            color: #00b3ff;
            text-decoration: underline;
        }

        footer .social-icons {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }

        footer .social-icons a {
            color: #fff;
            width: 25px;
            height: 25px;
        }

        footer .social-icons img {
            width: 25px;
            height: 25px;
        }

        footer .social-icons a:hover {
            color: #00b3ff;
        }

        footer .download-app {
            margin-top: 20px;
        }

        footer .download-app img {
            width: 120px;
            margin-right: 10px;
        }

        .terms-container {
            display: flex;
            justify-content: space-between;
            width: 100%;
            margin-top: 20px;
            color: #aaa;
            align-items: center;
        }

        .terms-left {
            text-align: left;
        }

        .terms-right {
            text-align: right;
        }

        .terms-left a {
            color: #aaa;
            text-decoration: none;
        }

        .terms-left a:hover {
            color: #00b3ff;
            text-decoration: underline;
        }

        .cta-btn {
            background-color: #00b3ff;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.3s ease;
        }

        .cta-btn:hover {
            background-color: #005f99;
            transform: scale(1.05);
        }

        .front {
            padding: 40px;
            text-align: center;
            max-width: 800px;
            margin: 50px auto;
        }

        .front p {
            font-size: 20px;
            color:#005f99;
            line-height: 1.6;
            margin-bottom: 25px;
            font-family: Arial, sans-serif;
            font-size: 28px;
        }

        .front video {
            width: 100%;
            height: auto;
            max-width: 600px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            margin-top: 10px;
        }

        @media (max-width: 768px) {
            .front {
                padding: 20px;
            }

            .front p {
                font-size: 18px;
            }

            .front video {
                max-width: 100%;
                height: auto;
            }
        }

        .about-p {
            max-width: 1150px;
            margin: 60px 30px;
            padding: 20px;
            text-align: left;
        }

        .about-p h5 {
            font-size: 50px;
            color: black;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .about-p p {
            font-size: 16px;
            line-height: 1.6;
            color: #222;
        }

        .hint {
            font-size: 25px;
            color: light black;
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <div class="logo">
            <img src="uy.jpeg" alt="HR Logo">
            <h1 id="logoText">Development</h1>
        </div>
        <div class="nav-container">
            <ul class="nav-links">
                <li><a href="home.html" id="homeLink">Home</a></li>
                <li><a href="about.html" id="aboutLink">About</a></li>
                <li><a href="contact.html" id="contactLink">Contact</a></li>
                <li><a href="goals.html" id="goalsLink">Goals</a></li>
            </ul>
            <div class="search-bar">
                <input type="text" placeholder="Search here..." id="searchPlaceholder">
                <button class="search-icon">🔍</button>
            </div>
            <div class="language-selector">
                <select id="languageSelect" onchange="changeLanguage()">
                    <option value="english">English</option>
                    <option value="chinese">Chinese</option>
                    <option value="spanish">Spanish</option>
                    <option value="french">French</option>
                </select>
            </div>
        </div>
    </nav>

    <div class="background">
        <img src="q.jpg" alt="Image description">
        <div class="short_b" id="shortText">
            Empowering Everyone to Learn the Skills for a Successful Future
        </div>
    </div>

    <div class="about-section">
        <h1 id="aboutHeading">Our Mission</h1>
        <p id="aboutDescription">We are dedicated to helping individuals achieve financial independence through our efforts.</p>
    </div>

    <div class="front">
        <p id="frontText">Through our efforts, people all across the world are able to realize their goals of financial independence</p>
        <video width="320" height="240" controls>
            <source src="imp.mp4" type="video/mp4">
            <source src="imp.mp4" type="video/ogg">
        </video>
    </div>

    <div class="about-p">
        <h5 id="coursesHeading" class="hint">Our Courses</h5>
        <p id="coursesDescription">We offer multiple courses in our company, with top-notch instructors. The courses we offer are as follow:</p>
        <ul>
            <li id="course1">Graphic Design</li>
            <li id="course2">Front End Development</li>
            <li id="course3">Shopify</li>
            <li id="course4">Full Stack Development</li>
        </ul>
    </div>

    <footer>
        <div class="footer-section">
            <h3 id="footerTitle">HR Development</h3>
            <ul>
                <li><a href="home.html" id="footerHome">Home</a></li>
                <li><a href="about.html" id="footerAbout">About</a></li>
                <li><a href="contact.html" id="footerContact">Contact</a></li>
                <li><a href="goals.html" id="footerGoals">Goals</a></li>
            </ul>
        </div>

        <div class="footer-section">
            <h3 id="communityTitle">Community</h3>
            <ul>
                <li><a href="#">News</a></li>
            </ul>
        </div>

        <div class="footer-section">
            <h3 id="provideTitle">We Provide</h3>
            <ul>
                <li><a href="#">Graphic Designer</a></li>
                <li><a href="#">Web Developer </a></li>
                <li><a href="#">PowerPoint Expert</a></li>
                <li><a href="#">Data Entry Expert</a></li>
                <li><a href="#">Assignment Work</a></li>
                <li><a href="#">MS Word | MS Excel</a></li>
                <li><a href="#">Full Stack Developer</a></li>
            </ul>
        </div>

        <div class="footer-section">
            <h3 id="contactUsTitle">Contact Us On</h3>
            <div class="download-app">
              <p id="emailText">hiringforbenifits24@gmail.com</p>
              <p id="phoneText">+923456515537</p>
            </div>
        </div>

        <div class="terms-container">
            <div class="terms-left"> 
                <p>_____________________________________________________________________________</p>
                <p><a href="#" id="termsLink">Terms of use</a> | <a href="#" id="privacyLink">Privacy</a> | <a href="#" id="cookiesLink">Use of cookies</a></p>
            </div>   
            <div class="terms-right">
                <p>________________________________________________________________________________</p>
                <p id="copyrightText">© 2024 HR_Development Company</p>
            </div>
        </div>
    </footer>

    <script>
        const translations = {
            chinese: {
                pageTitle: "人力资源开发",
                logoText: "开发",
                homeLink: "家",
                aboutLink: "关于我们",
                contactLink: "接触",
                goalsLink: "目标",
                searchPlaceholder: "在这里搜索...",
                shortText: "赋予每个人学习成功未来技能的能力",
                aboutHeading: "我们的任务",
                aboutDescription: "我们致力于通过我们的努力帮助个人实现财务独立。",
                frontText: "通过我们的努力，世界各地的人们都能实现财务独立的目标",
                coursesHeading: "我们的课程",
                coursesDescription: "我们公司提供多种课程，由顶级讲师授课。我们提供的课程如下：",
                course1: "平面设计",
                course2: "前端开发",
                course3: "Shopify",
                course4: "全栈开发",
                footerTitle: "人力资源发展",
                communityTitle: "社区",
                provideTitle: "我们提供",
                contactUsTitle: "联系我们",
                emailText: "hiringforbenifits24@gmail.com",
                phoneText: "+923456515537",
                termsLink: "使用条款",
                privacyLink: "隐私",
                cookiesLink: "使用Cookies",
                copyrightText: "© 2024 人力资源开发公司"
            },
            english: {
                pageTitle: "HR Development",
                logoText: "Development",
                homeLink: "Home",
                aboutLink: "About",
                contactLink: "Contact",
                goalsLink: "Goals",
                searchPlaceholder: "Search here...",
                shortText: "Empowering Everyone to Learn the Skills for a Successful Future",
                aboutHeading: "Our Mission",
                aboutDescription: "We are dedicated to helping individuals achieve financial independence through our efforts.",
                frontText: "Through our efforts, people all across the world are able to realize their goals of financial independence",
                coursesHeading: "Our Courses",
                coursesDescription: "We offer multiple courses in our company, with top-notch instructors. The courses we offer are as follow:",
                course1: "Graphic Design",
                course2: "Front End Development",
                course3: "Shopify",
                course4: "Full Stack Development",
                footerTitle: "HR Development",
                communityTitle: "Community",
                provideTitle: "We Provide",
                contactUsTitle: "Contact Us On",
                emailText: "hiringforbenifits24@gmail.com",
                phoneText: "+923456515537",
                termsLink: "Terms of use",
                privacyLink: "Privacy",
                cookiesLink: "Use of cookies",
                copyrightText: "© 2024 HR_Development Company"
            },
            spanish: {
                pageTitle: "Desarrollo de RRHH",
                logoText: "Desarrollo",
                homeLink: "Inicio",
                aboutLink: "Sobre Nosotros",
                contactLink: "Contacto",
                goalsLink: "Metas",
                searchPlaceholder: "Buscar aquí...",
                shortText: "Empoderando a todos para aprender las habilidades para un futuro exitoso",
                aboutHeading: "Nuestra Misión",
                aboutDescription: "Nos dedicamos a ayudar a las personas a lograr la independencia financiera a través de nuestros esfuerzos.",
                frontText: "A través de nuestros esfuerzos, las personas de todo el mundo pueden alcanzar sus metas de independencia financiera",
                coursesHeading: "Nuestros Cursos",
                coursesDescription: "Ofrecemos múltiples cursos en nuestra empresa, con instructores de primer nivel. Los cursos que ofrecemos son los siguientes:",
                course1: "Diseño Gráfico",
                course2: "Desarrollo Front-End",
                course3: "Shopify",
                course4: "Desarrollo Full Stack",
                footerTitle: "Desarrollo de RRHH",
                communityTitle: "Comunidad",
                provideTitle: "Nosotros Proveemos",
                contactUsTitle: "Contáctanos En",
                emailText: "hiringforbenifits24@gmail.com",
                phoneText: "+923456515537",
                termsLink: "Términos de uso",
                privacyLink: "Privacidad",
                cookiesLink: "Uso de cookies",
                copyrightText: "© 2024 Compañía de Desarrollo de RRHH"
            },
            french: {
                pageTitle: "Développement RH",
                logoText: "Développement",
                homeLink: "Accueil",
                aboutLink: "À Propos",
                contactLink: "Contact",
                goalsLink: "Objectifs",
                searchPlaceholder: "Rechercher ici...",
                shortText: "Donner à chacun les moyens d'acquérir les compétences pour un avenir réussi",
                aboutHeading: "Notre Mission",
                aboutDescription: "Nous sommes dédiés à aider les individus à atteindre l'indépendance financière par nos efforts.",
                frontText: "Grâce à nos efforts, les gens du monde entier peuvent réaliser leurs objectifs d'indépendance financière",
                coursesHeading: "Nos Cours",
                coursesDescription: "Nous proposons plusieurs cours dans notre entreprise, avec des instructeurs de premier ordre. Les cours que nous proposons sont les suivants:",
                course1: "Conception Graphique",
                course2: "Développement Front End",
                course3: "Shopify",
                course4: "Développement Full Stack",
                footerTitle: "Développement RH",
                communityTitle: "Communauté",
                provideTitle: "Nous Offrons",
                contactUsTitle: "Contactez-nous",
                emailText: "hiringforbenifits24@gmail.com",
                phoneText: "+923456515537",
                termsLink: "Conditions d'utilisation",
                privacyLink: "Confidentialité",
                cookiesLink: "Utilisation des cookies",
                copyrightText: "© 2024 Développement RH"
            }
        };

        function changeLanguage() {
            const selectedLanguage = document.getElementById("languageSelect").value;
            const languageTexts = translations[selectedLanguage];

            document.getElementById("pageTitle").innerText = languageTexts.pageTitle;
            document.getElementById("logoText").innerText = languageTexts.logoText;
            document.getElementById("homeLink").innerText = languageTexts.homeLink;
            document.getElementById("aboutLink").innerText = languageTexts.aboutLink;
            document.getElementById("contactLink").innerText = languageTexts.contactLink;
            document.getElementById("goalsLink").innerText = languageTexts.goalsLink;
            document.getElementById("searchPlaceholder").placeholder = languageTexts.searchPlaceholder;
            document.getElementById("shortText").innerText = languageTexts.shortText;
            document.getElementById("aboutHeading").innerText = languageTexts.aboutHeading;
            document.getElementById("aboutDescription").innerText = languageTexts.aboutDescription;
            document.getElementById("frontText").innerText = languageTexts.frontText;
            document.getElementById("coursesHeading").innerText = languageTexts.coursesHeading;
            document.getElementById("coursesDescription").innerText = languageTexts.coursesDescription;
            document.getElementById("course1").innerText = languageTexts.course1;
            document.getElementById("course2").innerText = languageTexts.course2;
            document.getElementById("course3").innerText = languageTexts.course3;
            document.getElementById("course4").innerText = languageTexts.course4;
            document.getElementById("footerTitle").innerText = languageTexts.footerTitle;
            document.getElementById("footerHome").innerText = languageTexts.footerHome;
            document.getElementById("footerAbout").innerText = languageTexts.footerAbout;
            document.getElementById("footerContact").innerText = languageTexts.footerContact;
            document.getElementById("footerGoals").innerText = languageTexts.footerGoals;
            document.getElementById("communityTitle").innerText = languageTexts.communityTitle;
            document.getElementById("provideTitle").innerText = languageTexts.provideTitle;
            document.getElementById("contactUsTitle").innerText = languageTexts.contactUsTitle;
            document.getElementById("emailText").innerText = languageTexts.emailText;
            document.getElementById("phoneText").innerText = languageTexts.phoneText;
            document.getElementById("termsLink").innerText = languageTexts.termsLink;
            document.getElementById("privacyLink").innerText = languageTexts.privacyLink;
            document.getElementById("cookiesLink").innerText = languageTexts.cookiesLink;
            document.getElementById("copyrightText").innerText = languageTexts.copyrightText;
        }
    </script>
</body>
</html>
