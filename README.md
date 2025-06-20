<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Long Piseth - Software Engineer</title>
    <style>
        :root {
            --bg-color: #ffffff;
            --text-color: #333333;
            --primary-color: #00D9FF;
            --secondary-color: #FF6B6B;
            --accent-color: #4ECDC4;
            --card-bg: #f8f9fa;
            --border-color: #e9ecef;
            --code-bg: #f6f8fa;
        }

        @media (prefers-color-scheme: dark) {
            :root {
                --bg-color: #0D1117;
                --text-color: #FFFFFF;
                --primary-color: #00D9FF;
                --secondary-color: #FF6B6B;
                --accent-color: #4ECDC4;
                --card-bg: #161B22;
                --border-color: #30363D;
                --code-bg: #161B22;
            }
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 40px;
            padding: 60px 0;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            border-radius: 15px;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: wave 6s ease-in-out infinite;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            50% { transform: rotate(180deg); }
        }

        .header h1 {
            font-size: 3.5rem;
            font-weight: bold;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }

        .header p {
            font-size: 1.5rem;
            position: relative;
            z-index: 1;
        }

        .typing-animation {
            background: var(--card-bg);
            padding: 30px;
            margin: 30px 0;
            border-radius: 10px;
            text-align: center;
            border: 1px solid var(--border-color);
        }

        .typing-text {
            font-family: 'JetBrains Mono', monospace;
            font-size: 1.2rem;
            color: var(--primary-color);
            font-weight: 500;
        }

        .section {
            margin: 50px 0;
            padding: 30px;
            background: var(--card-bg);
            border-radius: 15px;
            border: 1px solid var(--border-color);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 217, 255, 0.1);
        }

        .section h2 {
            color: var(--primary-color);
            font-size: 2.5rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .section h3 {
            color: var(--secondary-color);
            font-size: 1.8rem;
            margin: 20px 0 10px 0;
        }

        .code-block {
            background: var(--code-bg);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 25px;
            margin: 20px 0;
            font-family: 'JetBrains Mono', monospace;
            overflow-x: auto;
            font-size: 0.9rem;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin: 20px 0;
            justify-content: center;
        }

        .tech-badge {
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            color: white;
            padding: 8px 16px;
            border-radius: 25px;
            font-weight: 600;
            font-size: 0.9rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }

        .tech-badge:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(0, 217, 255, 0.3);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 30px;
            margin: 30px 0;
        }

        .project-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 15px;
            padding: 25px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 217, 255, 0.15);
        }

        .project-title {
            color: var(--primary-color);
            font-size: 1.5rem;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .project-desc {
            color: var(--accent-color);
            font-style: italic;
            margin-bottom: 15px;
        }

        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .stat-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .stat-card:hover {
            transform: scale(1.02);
        }

        .contact-links {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin: 30px 0;
        }

        .contact-link {
            background: linear-gradient(135deg, var(--secondary-color), var(--primary-color));
            color: white;
            padding: 12px 24px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .contact-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 107, 107, 0.3);
        }

        .strengths-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .strength-item {
            background: linear-gradient(135deg, var(--accent-color), var(--primary-color));
            color: white;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            font-weight: 600;
            transition: transform 0.3s ease;
        }

        .strength-item:hover {
            transform: scale(1.05);
        }

        .education-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
        }

        .education-table th,
        .education-table td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid var(--border-color);
        }

        .education-table th {
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            color: white;
            font-weight: 600;
        }

        .footer {
            text-align: center;
            margin-top: 50px;
            padding: 40px 0;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            border-radius: 15px;
            color: white;
        }

        .quote {
            font-size: 1.5rem;
            font-style: italic;
            color: var(--primary-color);
            text-align: center;
            margin: 30px 0;
            padding: 20px;
            background: var(--card-bg);
            border-left: 5px solid var(--primary-color);
            border-radius: 5px;
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5rem;
            }
            
            .header p {
                font-size: 1.2rem;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .tech-stack {
                justify-content: center;
            }
            
            .section {
                padding: 20px;
            }
        }

        .theme-toggle {
            position: fixed;
            top: 20px;
            right: 20px;
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            font-size: 1.5rem;
            cursor: pointer;
            transition: transform 0.3s ease;
            z-index: 1000;
        }

        .theme-toggle:hover {
            transform: scale(1.1);
        }

        .pulse {
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>
    <button class="theme-toggle" onclick="toggleTheme()" title="Toggle Theme">🌓</button>

    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <h1>LONG PISETH</h1>
            <p>Software Engineer | Full Stack Developer</p>
        </div>

        <!-- Typing Animation -->
        <div class="typing-animation">
            <div class="typing-text" id="typingText">
                Flexible problem solver with leadership skills
            </div>
        </div>

        <!-- About Me Section -->
        <div class="section">
            <h2>🚀 About Me</h2>
            <div class="code-block">
<pre>
interface SoftwareEngineer {
  name: string;
  role: string;
  location: string;
  contact: {
    phone: string;
    email: string;
    address: string;
  };
  personal: {
    dateOfBirth: string;
    nationality: string;
    gender: string;
  };
  education: {
    university: string;
    degree: string;
    year: string;
  };
  strengths: string[];
  philosophy: string;
}

const piseth: SoftwareEngineer = {
  name: "Long Piseth",
  role: "Software Engineer & Full Stack Developer",
  location: "Phnom Penh, Cambodia 🇰🇭",
  contact: {
    phone: "+855 87 575 678",
    email: "longpiseth5555@gmail.com",
    address: "Phum Damnak, Sangkat Phnom Penh Thmie, Khan Sen Sok"
  },
  personal: {
    dateOfBirth: "November 24, 2002",
    nationality: "Cambodian",
    gender: "Male"
  },
  education: {
    university: "Royal University of Phnom Penh",
    degree: "Bachelor of Computer Science",
    year: "2021-2025"
  },
  strengths: [
    "Flexible & Adaptable", "Knowledge Sharing", "Leadership", 
    "Teamwork", "Problem Solving", "Communication"
  ],
  philosophy: "Flexibility breeds innovation, collaboration creates excellence"
};
</pre>
            </div>

            <div class="quote">
                💫 Core Values & Approach: I am a flexible person who loves to share knowledge, with strong leadership and teamwork skills. I have experience managing both backend and frontend development in projects like KHOTIXS, and I excel in communication with teammates and stakeholders.
            </div>

            <div class="strengths-grid">
                <div class="strength-item pulse">🎯 Attention to Detail</div>
                <div class="strength-item pulse">💡 Problem Solving</div>
                <div class="strength-item pulse">👥 Leadership</div>
                <div class="strength-item pulse">💬 Communication</div>
            </div>
        </div>

        <!-- Tech Arsenal Section -->
        <div class="section">
            <h2>🎯 Tech Arsenal</h2>
            
            <h3>Languages & Frameworks</h3>
            <div class="tech-stack">
                <span class="tech-badge">☕ Java</span>
                <span class="tech-badge">📘 TypeScript</span>
                <span class="tech-badge">🟨 JavaScript</span>
                <span class="tech-badge">⚡ C++</span>
                <span class="tech-badge">🔵 .NET</span>
            </div>

            <h3>Frontend Technologies</h3>
            <div class="tech-stack">
                <span class="tech-badge">⚛️ React</span>
                <span class="tech-badge">▲ Next.js</span>
                <span class="tech-badge">🎨 TailwindCSS</span>
                <span class="tech-badge">🅱️ Bootstrap</span>
                <span class="tech-badge">🏗️ HTML5</span>
                <span class="tech-badge">🎨 CSS3</span>
            </div>

            <h3>Backend & Database</h3>
            <div class="tech-stack">
                <span class="tech-badge">🍃 Spring Boot</span>
                <span class="tech-badge">🌐 ASP.NET</span>
                <span class="tech-badge">🐘 PostgreSQL</span>
                <span class="tech-badge">🐬 MySQL</span>
                <span class="tech-badge">🍃 MongoDB</span>
                <span class="tech-badge">💾 SQL Server</span>
            </div>

            <h3>DevOps & Tools</h3>
            <div class="tech-stack">
                <span class="tech-badge">🐳 Docker</span>
                <span class="tech-badge">☸️ Kubernetes</span>
                <span class="tech-badge">🌐 NGINX</span>
                <span class="tech-badge">🔀 Git</span>
                <span class="tech-badge">🐧 Linux</span>
                <span class="tech-badge">🔍 ElasticSearch</span>
            </div>
        </div>

        <!-- Projects Section -->
        <div class="section">
            <h2>💼 Featured Projects & Experience</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-title">🎫 KHOTIXS</div>
                    <div class="project-desc">Event Management & Ticketing Platform</div>
                    <p><strong>Tech Stack:</strong> React • Spring Boot • ElasticSearch</p>
                    <p><strong>My Role:</strong></p>
                    <ul>
                        <li>🎨 UI/UX Design</li>
                        <li>📊 Project Analysis & Database Design</li>
                        <li>🔧 Full Stack Development</li>
                        <li>🔍 ElasticSearch Research & Implementation</li>
                        <li>📈 Data Collection & Analysis</li>
                    </ul>
                    <p><strong>Status:</strong> 🚀 Production Ready</p>
                </div>

                <div class="project-card">
                    <div class="project-title">🛒 KHMER MART</div>
                    <div class="project-desc">Dynamic Online Marketplace</div>
                    <p><strong>Tech Stack:</strong> React • Laravel • MySQL</p>
                    <p><strong>My Role:</strong></p>
                    <ul>
                        <li>🎨 UI/UX Design</li>
                        <li>🔌 API Implementation</li>
                        <li>📚 Project Documentation</li>
                    </ul>
                    <p><strong>Status:</strong> 🎯 Feature Complete</p>
                </div>

                <div class="project-card">
                    <div class="project-title">📚 ISTAD LMS</div>
                    <div class="project-desc">Learning Management System</div>
                    <p><strong>Tech Stack:</strong> Next.js • PostgreSQL • REST API</p>
                    <p><strong>My Role:</strong></p>
                    <ul>
                        <li>🏗️ Project Analysis</li>
                        <li>🗄️ Database Analysis & Design</li>
                        <li>🔌 API Implementation</li>
                        <li>💻 Frontend Development</li>
                    </ul>
                    <p><strong>Status:</strong> ✅ Optimized & Deployed</p>
                </div>

                <div class="project-card">
                    <div class="project-title">📦 INVENTORY MANAGEMENT</div>
                    <div class="project-desc">Java Console Application</div>
                    <p><strong>Tech Stack:</strong> Java • Console Interface • File System</p>
                    <p><strong>My Role:</strong></p>
                    <ul>
                        <li>📊 Project Analysis</li>
                        <li>🗄️ Database Analysis</li>
                        <li>🔧 Core Development</li>
                    </ul>
                    <p><strong>Status:</strong> ✅ Completed</p>
                </div>
            </div>
        </div>

        <!-- Education Section -->
        <div class="section">
            <h2>🎓 Education & Professional Training</h2>
            
            <h3>🏛️ Academic Foundation</h3>
            <table class="education-table">
                <thead>
                    <tr>
                        <th>Institution</th>
                        <th>Program</th>
                        <th>Duration</th>
                        <th>Key Focus Areas</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Royal University of Phnom Penh</td>
                        <td>Bachelor of Computer Science</td>
                        <td>2021-2025</td>
                        <td>Core CS, Algorithms, System Design</td>
                    </tr>
                    <tr>
                        <td>Sreng Kim High School</td>
                        <td>BacII National Certificate</td>
                        <td>2017-2020</td>
                        <td>Academic Excellence</td>
                    </tr>
                </tbody>
            </table>

            <h3>💻 Professional Development</h3>
            <h4>ISTAD - Institute of Science and Technology Advanced Development</h4>
            <p><strong>🚀 Advanced Course</strong> (Aug 2024 - Jan 2025) - 770 hours</p>
            <ul>
                <li><strong>Spring Advanced:</strong> HATEOAS, Data JPA/MongoDB, OAuth2, Reactive Programming</li>
                <li><strong>Microservices Architecture:</strong> Decomposition Patterns, API Communication, Service Discovery</li>
                <li><strong>Modern Tech Stack:</strong> WebFlux, Apache Kafka, Keycloak, Spring Boot Actuators</li>
            </ul>

            <p><strong>📚 Basic Course</strong> (Feb 2024 - Aug 2024) - 900 hours</p>
            <ul>
                <li><strong>Full Stack Development:</strong> Java, React.js, Next.js, Spring Boot</li>
                <li><strong>Database Management:</strong> PostgreSQL, Advanced SQL, Data Modeling</li>
                <li><strong>DevOps Fundamentals:</strong> Docker, NGINX, CI/CD, Linux, Cloud Services</li>
            </ul>
        </div>

        <!-- Contact Section -->
        <div class="section">
            <h2>🌐 Connect With Me</h2>
            <div class="contact-links">
                <a href="mailto:longpiseth5555@gmail.com" class="contact-link">📧 Email</a>
                <a href="tel:+85587575678" class="contact-link">📱 Phone</a>
                <a href="https://linkedin.com/in/longpiseth" class="contact-link">💼 LinkedIn</a>
                <a href="https://t.me/longpiseth" class="contact-link">💬 Telegram</a>
            </div>
            <p style="text-align: center; margin-top: 20px;">
                <strong>📍 Address:</strong> Phum Damnak, Sangkat Phnom Penh Thmie, Khan Sen Sok, Phnom Penh, Cambodia<br>
                <strong>💼 Status:</strong> Open to Remote Opportunities, Collaborations, Full-time Positions
            </p>
        </div>

        <!-- Current Focus Section -->
        <div class="section">
            <h2>🎯 Current Focus & Interests</h2>
            <div class="code-block">
<pre>
const currentStatus = {
  🎓 completing: "Bachelor's in Computer Science (Final Year)",
  🔨 building: "Advanced Microservices Applications",
  🌱 learning: ["Advanced Spring Boot", "Cloud Architecture", "System Design"],
  🎯 goal2025: "Excel in Enterprise Software Development",
  💡 interests: ["IT Content Creation", "Technology Blogging"],
  🎵 hobbies: ["Music", "Continuous Learning", "Tech Exploration"],
  ☕ fuelledBy: "Curiosity and Collaborative Spirit"
};
</pre>
            </div>
        </div>

        <!-- Languages Section -->
        <div class="section">
            <h2>🗣️ Languages</h2>
            <table class="education-table">
                <thead>
                    <tr>
                        <th>Language</th>
                        <th>Proficiency</th>
                        <th>Skills</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>🇰🇭 Khmer</td>
                        <td>Native</td>
                        <td>Complete Fluency</td>
                    </tr>
                    <tr>
                        <td>🇺🇸 English</td>
                        <td>Advanced</td>
                        <td>Good Writing, Speaking, Listening, Reading</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <!-- Footer -->
        <div class="footer">
            <div class="quote" style="background: transparent; border: none; color: white;">
                "Flexibility in approach, excellence in execution, collaboration in spirit."
            </div>
            <p style="font-size: 1.2rem; margin: 20px 0;">🚀 Ready to contribute to innovative projects and grow with amazing teams!</p>
            <p><strong>Built with ❤️ by Long Piseth</strong></p>
        </div>
    </div>

    <script>
        // Typing animation
        const texts = [
            "Flexible problem solver with leadership skills",
            "Building innovative solutions with precision",
            "Passionate about sharing knowledge and collaboration"
        ];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingElement = document.getElementById('typingText');

        function typeText() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }

            if (!isDeleting && charIndex === currentText.length) {
                setTimeout(() => isDeleting = true, 2000);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
            }

            const speed = isDeleting ? 50 : 100;
            setTimeout(typeText, speed);
        }

        // Start typing animation
        typeText();

        // Theme toggle function (for manual override)
        function toggleTheme() {
            document.body.style.filter = document.body.style.filter === 'invert(1) hue-rotate(180deg)' ? '' : 'invert(1) hue-rotate(180deg)';
        }

        // Add smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add intersection observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('.section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(30px)';
            section.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(section);
        });
    </script>
</body>
</html>
