<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tejnarayan Sharma - Frontend Developer Portfolio</title>
    <style>
        /* Base styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #0a0a0a;
            color: #e0e0e0;
            line-height: 1.6;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: linear-gradient(145deg, #141414, #1a1a1a);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.8);
            border: 1px solid #2a2a2a;
        }

        /* Header */
        .header {
            text-align: center;
            padding: 30px 0;
            border-bottom: 2px solid #2a2a2a;
            margin-bottom: 30px;
        }

        .header h1 {
            font-size: 3.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, #00d4ff, #7b2ffc);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: 2px;
            margin-bottom: 10px;
        }

        .header .sub-title {
            font-size: 1.3rem;
            color: #a0a0a0;
            font-weight: 300;
        }

        .header .highlight {
            color: #00d4ff;
            font-weight: 600;
        }

        /* Profile Views */
        .profile-stats {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 15px;
            flex-wrap: wrap;
        }

        .profile-stats .stat {
            background: #1a1a1a;
            padding: 8px 20px;
            border-radius: 20px;
            border: 1px solid #2a2a2a;
            font-size: 0.9rem;
            color: #a0a0a0;
        }

        .profile-stats .stat span {
            color: #00d4ff;
            font-weight: 600;
        }

        /* About Me */
        .about-section {
            display: flex;
            align-items: center;
            gap: 40px;
            margin-bottom: 40px;
            padding: 20px;
            background: #121212;
            border-radius: 15px;
            border: 1px solid #2a2a2a;
            flex-wrap: wrap;
        }

        .about-text {
            flex: 2;
            min-width: 280px;
        }

        .about-text h2 {
            font-size: 1.8rem;
            color: #00d4ff;
            margin-bottom: 15px;
        }

        .about-text p {
            color: #b0b0b0;
            line-height: 1.8;
        }

        .about-image {
            flex: 1;
            min-width: 180px;
            text-align: center;
        }

        .about-image img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            border: 4px solid #00d4ff;
            object-fit: cover;
            box-shadow: 0 0 40px rgba(0, 212, 255, 0.2);
        }

        /* Section Titles */
        .section-title {
            font-size: 2rem;
            font-weight: 600;
            color: #00d4ff;
            margin: 40px 0 20px 0;
            padding-bottom: 10px;
            border-bottom: 2px solid #2a2a2a;
        }

        .section-title i {
            margin-right: 10px;
        }

        /* Skills */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .skill-category {
            background: #121212;
            padding: 20px;
            border-radius: 15px;
            border: 1px solid #2a2a2a;
            transition: transform 0.3s ease, border-color 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-5px);
            border-color: #00d4ff;
        }

        .skill-category h3 {
            color: #7b2ffc;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }

        .skill-tag {
            display: inline-block;
            background: #1a1a1a;
            color: #e0e0e0;
            padding: 5px 15px;
            border-radius: 20px;
            margin: 4px;
            font-size: 0.85rem;
            border: 1px solid #2a2a2a;
            transition: all 0.3s ease;
        }

        .skill-tag:hover {
            border-color: #00d4ff;
            color: #00d4ff;
            background: #1a1a1a;
        }

        .skill-tag.highlight {
            border-color: #00d4ff;
            color: #00d4ff;
        }

        /* Experience */
        .experience-card {
            background: #121212;
            padding: 25px;
            border-radius: 15px;
            border: 1px solid #2a2a2a;
            margin-bottom: 20px;
            transition: border-color 0.3s ease;
        }

        .experience-card:hover {
            border-color: #00d4ff;
        }

        .experience-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            flex-wrap: wrap;
            margin-bottom: 15px;
        }

        .experience-header .role {
            font-size: 1.3rem;
            font-weight: 600;
            color: #e0e0e0;
        }

        .experience-header .company {
            color: #7b2ffc;
            font-size: 1.1rem;
        }

        .experience-header .date {
            color: #888;
            font-size: 0.9rem;
            background: #1a1a1a;
            padding: 4px 15px;
            border-radius: 20px;
            border: 1px solid #2a2a2a;
        }

        .experience-body {
            padding-left: 10px;
        }

        .experience-body ul {
            list-style: none;
            padding-left: 0;
        }

        .experience-body ul li {
            padding: 8px 0;
            color: #b0b0b0;
            padding-left: 25px;
            position: relative;
        }

        .experience-body ul li::before {
            content: "▸";
            color: #00d4ff;
            position: absolute;
            left: 0;
            font-weight: bold;
        }

        .tech-used {
            margin-top: 12px;
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .tech-used .tech {
            background: #1a1a1a;
            color: #00d4ff;
            padding: 3px 12px;
            border-radius: 15px;
            font-size: 0.8rem;
            border: 1px solid #2a2a2a;
        }

        /* Projects */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .project-card {
            background: #121212;
            padding: 20px;
            border-radius: 15px;
            border: 1px solid #2a2a2a;
            transition: all 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            border-color: #7b2ffc;
            box-shadow: 0 10px 30px rgba(123, 47, 252, 0.1);
        }

        .project-card h4 {
            color: #00d4ff;
            font-size: 1.1rem;
            margin-bottom: 8px;
        }

        .project-card .tech-stack {
            color: #888;
            font-size: 0.85rem;
            margin-bottom: 10px;
        }

        .project-card p {
            color: #b0b0b0;
            font-size: 0.95rem;
        }

        /* Education */
        .education-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .edu-card {
            background: #121212;
            padding: 20px;
            border-radius: 15px;
            border: 1px solid #2a2a2a;
            transition: border-color 0.3s ease;
        }

        .edu-card:hover {
            border-color: #7b2ffc;
        }

        .edu-card h4 {
            color: #00d4ff;
            font-size: 1.1rem;
        }

        .edu-card .institute {
            color: #888;
            font-size: 0.9rem;
        }

        .edu-card .percentage {
            color: #7b2ffc;
            font-weight: 600;
            margin-top: 5px;
        }

        /* Accomplishments */
        .accomplishment-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .accomplishment-item {
            background: #121212;
            padding: 20px;
            border-radius: 15px;
            border: 1px solid #2a2a2a;
            display: flex;
            align-items: flex-start;
            gap: 15px;
            transition: all 0.3s ease;
        }

        .accomplishment-item:hover {
            border-color: #00d4ff;
            transform: translateX(5px);
        }

        .accomplishment-item .icon {
            font-size: 1.8rem;
            color: #00d4ff;
            flex-shrink: 0;
        }

        .accomplishment-item p {
            color: #b0b0b0;
            font-size: 0.95rem;
        }

        /* GitHub Stats */
        .github-stats {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }

        .github-stats img {
            border-radius: 10px;
            border: 1px solid #2a2a2a;
            max-width: 100%;
        }

        /* Social Links */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .social-links a {
            display: inline-block;
            padding: 10px 25px;
            border-radius: 30px;
            text-decoration: none;
            color: #e0e0e0;
            background: #1a1a1a;
            border: 1px solid #2a2a2a;
            transition: all 0.3s ease;
            font-size: 0.95rem;
        }

        .social-links a:hover {
            background: #00d4ff;
            color: #0a0a0a;
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 212, 255, 0.2);
        }

        .social-links a .icon {
            margin-right: 8px;
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 30px 0 10px 0;
            border-top: 1px solid #2a2a2a;
            margin-top: 30px;
            color: #666;
            font-size: 0.9rem;
        }

        .footer .heart {
            color: #ff6b6b;
        }

        .footer .highlight-text {
            color: #00d4ff;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .container {
                padding: 20px;
            }
            .header h1 {
                font-size: 2.5rem;
            }
            .about-section {
                flex-direction: column;
                text-align: center;
            }
            .experience-header {
                flex-direction: column;
                gap: 8px;
            }
            .profile-stats {
                gap: 10px;
            }
        }

        @media (max-width: 480px) {
            .header h1 {
                font-size: 1.8rem;
            }
            .section-title {
                font-size: 1.5rem;
            }
            .container {
                padding: 15px;
            }
        }
    </style>
</head>
<body>

    <div class="container">

        <!-- ================= HEADER ================= -->
        <div class="header">
            <h1>👋 Tejnarayan Sharma</h1>
            <p class="sub-title">
                <span class="highlight">Frontend Developer</span> | React.js Specialist | 2+ Years Experience
            </p>

            <div class="profile-stats">
                <span class="stat">👁️ Profile Views: <span>1,234</span></span>
                <span class="stat">⭐ GitHub Stars: <span>25</span></span>
                <span class="stat">📦 Projects: <span>8+</span></span>
            </div>
        </div>

        <!-- ================= ABOUT ME ================= -->
        <div class="about-section">
            <div class="about-text">
                <h2>💡 About Me</h2>
                <p>
                    <strong>Results-driven Frontend Developer</strong> with <strong>2+ years</strong> of experience in 
                    building scalable and high-performance web applications using <strong>React.js</strong>. 
                    Skilled in developing responsive, user-centric interfaces with clean, maintainable, and reusable code.
                    Proficient in modern <strong>JavaScript (ES6+)</strong>, state management with <strong>Redux</strong>, 
                    and <strong>REST API</strong> integration.
                </p>
                <p style="margin-top: 10px;">
                    Passionate about continuous learning, performance optimization, and ensuring quality 
                    across the frontend development lifecycle.
                </p>
            </div>
            <div class="about-image">
                <img src="https://media.licdn.com/dms/image/v2/D5603AQEo4ejbObtMvg/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1714059905517?e=2147483647&v=beta&t=4U3tFDROR83XzZJ_7_qSpZ5Y9Y4x-2Ykq-m04fzz5mQ" alt="Tejnarayan Sharma" />
            </div>
        </div>

        <!-- ================= SKILLS ================= -->
        <h2 class="section-title">🛠️ Technical Skills</h2>

        <div class="skills-grid">
            <!-- Frontend -->
            <div class="skill-category">
                <h3>⚛️ Frontend Technologies</h3>
                <span class="skill-tag highlight">React.js</span>
                <span class="skill-tag">Redux</span>
                <span class="skill-tag">JavaScript (ES6+)</span>
                <span class="skill-tag">HTML5</span>
                <span class="skill-tag">CSS3</span>
                <span class="skill-tag">TypeScript</span>
            </div>

            <!-- UI & Libraries -->
            <div class="skill-category">
                <h3>🎨 UI & Libraries</h3>
                <span class="skill-tag">MUI (Material UI)</span>
                <span class="skill-tag">TanStack Table</span>
                <span class="skill-tag">Responsive Design</span>
                <span class="skill-tag">Tailwind CSS</span>
                <span class="skill-tag">Bootstrap</span>
            </div>

            <!-- API & Integration -->
            <div class="skill-category">
                <h3>🔗 API & Integration</h3>
                <span class="skill-tag">REST API Integration</span>
                <span class="skill-tag">Axios</span>
                <span class="skill-tag">Fetch API</span>
                <span class="skill-tag">Data Handling</span>
            </div>

            <!-- State & Architecture -->
            <div class="skill-category">
                <h3>🏗️ State & Architecture</h3>
                <span class="skill-tag">Redux</span>
                <span class="skill-tag">Component-Based Architecture</span>
                <span class="skill-tag">Reusable Components</span>
                <span class="skill-tag">Custom Hooks</span>
            </div>

            <!-- Performance -->
            <div class="skill-category">
                <h3>⚡ Performance & Optimization</h3>
                <span class="skill-tag">Code Optimization</span>
                <span class="skill-tag">Lazy Loading</span>
                <span class="skill-tag">Efficient Rendering</span>
                <span class="skill-tag">Memoization</span>
            </div>

            <!-- Database -->
            <div class="skill-category">
                <h3>🗄️ Database</h3>
                <span class="skill-tag">SQL</span>
                <span class="skill-tag highlight">MS SQL Server</span>
                <span class="skill-tag">MongoDB</span>
            </div>

            <!-- Backend -->
            <div class="skill-category">
                <h3>🔧 Backend (Basic)</h3>
                <span class="skill-tag">Node.js</span>
                <span class="skill-tag">Express.js</span>
                <span class="skill-tag">REST APIs</span>
            </div>

            <!-- Tools -->
            <div class="skill-category">
                <h3>🧰 Tools & Platforms</h3>
                <span class="skill-tag">Git</span>
                <span class="skill-tag">Docker</span>
                <span class="skill-tag">VS Code</span>
                <span class="skill-tag">WebLogic</span>
                <span class="skill-tag">Postman</span>
            </div>

            <!-- Domain -->
            <div class="skill-category">
                <h3>🏢 Domain Knowledge</h3>
                <span class="skill-tag">GRC Applications</span>
                <span class="skill-tag">ORM</span>
                <span class="skill-tag">TPRM</span>
            </div>

            <!-- Soft Skills -->
            <div class="skill-category">
                <h3>🤝 Soft Skills</h3>
                <span class="skill-tag">Team Collaboration</span>
                <span class="skill-tag">Problem Solving</span>
                <span class="skill-tag">Agile Methodologies</span>
                <span class="skill-tag">Communication</span>
                <span class="skill-tag">Time Management</span>
            </div>
        </div>

        <!-- ================= EXPERIENCE ================= -->
        <h2 class="section-title">💼 Work Experience</h2>

        <div class="experience-card">
            <div class="experience-header">
                <div>
                    <span class="role">Software Developer</span>
                    <span class="company"> | Claptek, Mumbai, India</span>
                </div>
                <span class="date">📅 08/2024 – Present</span>
            </div>

            <div class="experience-body">
                <ul>
                    <li>
                        <strong>Led frontend development</strong> of GRC web applications using <strong>React.js</strong>, 
                        delivering scalable and user-friendly interfaces for clients including <strong>HDFC, Bank of Baroda, and Yes Bank</strong>.
                    </li>
                    <li>
                        <strong>Developed and enhanced key applications:</strong>
                        <ul style="margin-top: 8px; margin-left: 20px; list-style: none;">
                            <li style="padding-left: 20px;">
                                <strong>🔹 A3 (Audit Management System):</strong> Built interactive UI to enable audit assessments, 
                                allowing users to evaluate checkpoints with statuses such as Pass, Fail, Spot Rectification (SR), 
                                and Not Applicable (NA). Focused on dynamic form handling and data-driven rendering.
                            </li>
                            <li style="padding-left: 20px; margin-top: 5px;">
                                <strong>🔹 AMS (Audit Management System):</strong> Contributed to an end-to-end audit lifecycle 
                                management platform with workflows, dashboards, and approval mechanisms, designed for 
                                enterprise-level GRC processes.
                            </li>
                        </ul>
                    </li>
                    <li>Built responsive and high-performance UI components, improving user experience and contributing to faster feature delivery.</li>
                    <li>Optimized application performance through efficient rendering and frontend best practices.</li>
                    <li>Integrated <strong>REST APIs</strong> and handled dynamic data rendering to support business-critical workflows.</li>
                    <li>Collaborated with cross-functional teams for requirement gathering, UI design, and seamless feature implementation.</li>
                    <li>Developed <strong>reusable components</strong> and maintained clean, scalable code architecture for long-term maintainability.</li>
                    <li>Performed debugging, bug fixing, and functional testing to ensure high-quality and stable releases.</li>
                    <li>Ensured timely delivery of projects while maintaining coding standards and best practices.</li>
                    <li>Involved in <strong>requirement gathering</strong> and project planning.</li>
                </ul>

                <div class="tech-used">
                    <span class="tech">React.js</span>
                    <span class="tech">Redux</span>
                    <span class="tech">Material-UI</span>
                    <span class="tech">JavaScript (ES6+)</span>
                    <span class="tech">REST APIs</span>
                    <span class="tech">MS SQL Server</span>
                    <span class="tech">Git</span>
                    <span class="tech">Docker</span>
                    <span class="tech">Node.js</span>
                    <span class="tech">Express.js</span>
                </div>
            </div>
        </div>

        <!-- ================= PROJECTS ================= -->
        <h2 class="section-title">🚀 Key Projects</h2>

        <div class="project-grid">
            <!-- Project 1 -->
            <div class="project-card">
                <h4>🔹 A3 - Audit Management System</h4>
                <div class="tech-stack">React.js · Redux · Material-UI · REST APIs · MS SQL</div>
                <p>
                    Built an interactive UI enabling audit assessments with dynamic form handling and data-driven rendering. 
                    Users can evaluate checkpoints with statuses: Pass, Fail, Spot Rectification (SR), and Not Applicable (NA).
                    Served to clients including <strong>HDFC, Bank of Baroda, and Yes Bank</strong>.
                </p>
            </div>

            <!-- Project 2 -->
            <div class="project-card">
                <h4>🔹 AMS - Enterprise Audit Management</h4>
                <div class="tech-stack">React.js · Redux · Material-UI · Node.js · Express · MS SQL</div>
                <p>
                    Contributed to an end-to-end audit lifecycle management platform with workflows, dashboards, and approval mechanisms.
                    Designed for enterprise-level GRC processes with focus on security and scalability.
                </p>
            </div>

            <!-- Project 3 -->
            <div class="project-card">
                <h4>🔹 GRC Dashboard Platform</h4>
                <div class="tech-stack">React.js · Redux · TanStack Table · MUI · REST APIs</div>
                <p>
                    Developed a comprehensive GRC dashboard with advanced data tables, filtering, and real-time updates.
                    Implemented role-based access control and interactive data visualization for compliance monitoring.
                </p>
            </div>
        </div>

        <!-- ================= EDUCATION ================= -->
        <h2 class="section-title">🎓 Education</h2>

        <div class="education-grid">
            <div class="edu-card">
                <h4>🎓 Bachelor of Science in Computer Science (B.Sc. CS)</h4>
                <p class="institute">Mumbai University</p>
                <p class="percentage">📊 Percentage: 69%</p>
            </div>

            <div class="edu-card">
                <h4>📚 Higher Secondary Certificate (Class XII)</h4>
                <p class="institute">Oriental College of Commerce and Science</p>
                <p class="percentage">📊 Percentage: 41%</p>
            </div>

            <div class="edu-card">
                <h4>📖 Secondary School Certificate (Class X)</h4>
                <p class="institute">Swami Vivekanand Vidyalaya</p>
                <p class="percentage">📊 Percentage: 68%</p>
            </div>
        </div>

        <!-- ================= ACCOMPLISHMENTS ================= -->
        <h2 class="section-title">🏆 Accomplishments</h2>

        <div class="accomplishment-list">
            <div class="accomplishment-item">
                <span class="icon">🏅</span>
                <p>
                    <strong>Team Leadership:</strong> Played a key role as a Frontend Developer in a team of <strong>15 members</strong>, 
                    contributing to the design and development of multiple enterprise-level web applications used by leading banking clients.
                </p>
            </div>

            <div class="accomplishment-item">
                <span class="icon">📦</span>
                <p>
                    <strong>Project Delivery:</strong> Successfully delivered <strong>3+ large-scale GRC-based applications</strong>, 
                    ensuring high performance, scalability, and seamless user experience across platforms.
                </p>
            </div>

            <div class="accomplishment-item">
                <span class="icon">⭐</span>
                <p>
                    <strong>Recognition:</strong> Recognized for consistently delivering quality UI solutions and meeting project deadlines 
                    in fast-paced, client-driven environments.
                </p>
            </div>
        </div>

        <!-- ================= GITHUB STATS ================= -->
        <h2 class="section-title">📊 GitHub Analytics</h2>

        <div class="github-stats">
            <img 
                src="https://github-readme-stats.vercel.app/api/top-langs?username=teznarayan-developer&show_icons=true&locale=en&layout=compact&theme=radical&hide=html,css" 
                alt="Top Languages" 
                width="400"
            />
            <img 
                src="https://github-readme-stats.vercel.app/api?username=teznarayan-developer&show_icons=true&locale=en&theme=radical&count_private=true" 
                alt="GitHub Stats" 
                width="450"
            />
        </div>

        <div style="text-align: center; margin: 20px 0;">
            <img 
                src="https://github-readme-streak-stats.herokuapp.com/?user=teznarayan-developer&theme=radical" 
                alt="GitHub Streak" 
                width="600"
                style="border-radius: 10px; border: 1px solid #2a2a2a; max-width: 100%;"
            />
        </div>

        <!-- ================= SOCIAL LINKS ================= -->
        <h2 class="section-title">🤝 Let's Connect</h2>

        <div class="social-links">
            <a href="mailto:rohitkks010@gmail.com">
                <span class="icon">📧</span> Email
            </a>
            <a href="https://www.linkedin.com/in/teznarayan-sharma-182079224" target="_blank">
                <span class="icon">💼</span> LinkedIn
            </a>
            <a href="https://github.com/teznarayan-developer" target="_blank">
                <span class="icon">🐙</span> GitHub
            </a>
            <a href="#" target="_blank">
                <span class="icon">🐦</span> Twitter
            </a>
            <a href="#" target="_blank">
                <span class="icon">📱</span> Portfolio
            </a>
        </div>

        <!-- ================= FOOTER ================= -->
        <div class="footer">
            <p>
                Made with <span class="heart">❤️</span> by 
                <span class="highlight-text">Tejnarayan Sharma</span> 
                | 2+ Years of Frontend Excellence 🚀
            </p>
            <p style="margin-top: 5px; font-size: 0.8rem; color: #555;">
                "Code with passion, build with purpose"
            </p>
        </div>

    </div>

</body>
</html>
