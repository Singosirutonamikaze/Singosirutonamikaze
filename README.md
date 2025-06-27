<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SINGO Yao Dieu Donné - Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #6C63FF;
            --secondary: #4A44B5;
            --accent: #FF6584;
            --dark: #121212;
            --light: #F5F5F7;
            --transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: var(--light);
            line-height: 1.6;
            min-height: 100vh;
            padding: 2rem;
            background-attachment: fixed;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            padding: 3rem 1rem;
            position: relative;
            overflow: hidden;
        }
        
        .profile-pic {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 5px solid var(--primary);
            margin: 0 auto 1.5rem;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(108, 99, 255, 0.4);
            transition: var(--transition);
        }
        
        .profile-pic:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 40px rgba(108, 99, 255, 0.6);
        }
        
        .profile-pic i {
            font-size: 5rem;
            color: white;
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 0.5rem;
            background: linear-gradient(to right, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }
        
        .tagline {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            opacity: 0.9;
            font-weight: 300;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            transition: var(--transition);
            text-decoration: none;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .social-link:hover {
            background: var(--primary);
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(108, 99, 255, 0.4);
        }
        
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }
        
        .card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 2rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: var(--transition);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }
        
        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
            background: rgba(255, 255, 255, 0.08);
            border-color: rgba(108, 99, 255, 0.4);
        }
        
        .card h2 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 0.8rem;
        }
        
        .card h2 i {
            background: linear-gradient(45deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .card ul {
            padding-left: 1.5rem;
        }
        
        .card li {
            margin-bottom: 0.8rem;
            position: relative;
        }
        
        .card li:before {
            content: "•";
            color: var(--accent);
            font-weight: bold;
            position: absolute;
            left: -1.2rem;
        }
        
        .badge-container {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin-top: 1.5rem;
        }
        
        .badge {
            background: rgba(108, 99, 255, 0.15);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-size: 0.9rem;
            border: 1px solid var(--primary);
            transition: var(--transition);
        }
        
        .badge:hover {
            background: var(--primary);
            transform: scale(1.05);
        }
        
        .contact-btn {
            display: block;
            width: 100%;
            max-width: 300px;
            margin: 3rem auto;
            padding: 1rem;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            text-align: center;
            text-decoration: none;
            box-shadow: 0 10px 20px rgba(108, 99, 255, 0.3);
        }
        
        .contact-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(108, 99, 255, 0.5);
            letter-spacing: 1px;
        }
        
        .fun-fact {
            text-align: center;
            padding: 2rem;
            background: rgba(255, 101, 132, 0.1);
            border-radius: 20px;
            margin-top: 3rem;
            border: 1px solid rgba(255, 101, 132, 0.2);
        }
        
        .fun-fact p {
            font-style: italic;
            font-size: 1.2rem;
        }
        
        .fun-fact p:before, .fun-fact p:after {
            content: '"';
            color: var(--accent);
            font-size: 1.5rem;
        }
        
        footer {
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .card-grid {
                grid-template-columns: 1fr;
            }
        }
        
        /* Animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        .floating {
            animation: float 4s ease-in-out infinite;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="profile-pic floating">
                <i class="fas fa-user-astronaut"></i>
            </div>
            <h1>SINGO Yao Dieu Donné</h1>
            <p class="tagline">Web Developer • AI Enthusiast • Creative Problem Solver</p>
            
            <div class="social-links">
                <a href="mailto:yaodieudonnesingo60@gmail.com" class="social-link">
                    <i class="fas fa-envelope"></i>
                </a>
                <a href="mailto:yaodieudonnesingo6@gmail.com" class="social-link">
                    <i class="fas fa-envelope-open"></i>
                </a>
                <a href="https://www.linkedin.com/in/singo-yao-dieu-donne" target="_blank" class="social-link">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="https://github.com/Singosirutonamikaze" target="_blank" class="social-link">
                    <i class="fab fa-github"></i>
                </a>
            </div>
        </header>
        
        <div class="card-grid">
            <div class="card">
                <h2><i class="fas fa-heart"></i> Interests</h2>
                <p>I'm passionate about creating innovative solutions at the intersection of:</p>
                <ul>
                    <li>Web development and application programming</li>
                    <li>Artificial intelligence and machine learning</li>
                    <li>Creative UI/UX design experiences</li>
                    <li>Turning ideas into impactful digital products</li>
                </ul>
            </div>
            
            <div class="card">
                <h2><i class="fas fa-graduation-cap"></i> Currently Learning</h2>
                <p>Expanding my skillset with focus on:</p>
                <ul>
                                        <li>JavaScript for interactive web experiences</li>
                    <li>Advanced HTML & CSS techniques</li>
                    <li>Responsive design principles</li>
                </ul>
                
                <div class="badge-container">
                    <div class="badge">JavaScript</div>
                    <div class="badge">HTML5</div>
                    <div class="badge">CSS3</div>
                    <div class="badge">React</div>
                    <div class="badge">React Native</div>
                </div>
            </div>
            
            <div class="card">
                <h2><i class="fas fa-hands-helping"></i> Collaboration</h2>
                <p>Looking to partner on exciting projects:</p>
                <ul>
                    <li>Website development (especially HTML/CSS based)</li>
                    <li>Creative web applications</li>
                    <li>Educational technology solutions</li>
                    <li>Projects with Binasery School peers</li>
                </ul>
                <p>Let's combine our skills to solve problems and build something meaningful!</p>
            </div>
        </div>
        
        <a href="mailto:yaodieudonnesingo60@gmail.com" class="contact-btn">
            <i class="fas fa-paper-plane"></i> Contact Me
        </a>
        
        <div class="fun-fact">
            <p>I once created a small AI that generates unique crosswords, combining my love for puzzles and programming!</p>
        </div>
        
        <footer>
            <p>© 2023 SINGO Yao Dieu Donné | He/Him</p>
            <p>Let's build something amazing together!</p>
        </footer>
    </div>
    
    <script>
        // Add subtle animations on scroll
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.card');
            
            cards.forEach(card => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(20px)';
            });
            
            setTimeout(() => {
                cards.forEach((card, index) => {
                    setTimeout(() => {
                        card.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
                        card.style.opacity = '1';
                        card.style.transform = 'translateY(0)';
                    }, 200 * index);
                });
            }, 500);
        });
    </script>
</body>
</html>
