<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shabbir Hussain - Software Engineer</title>
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
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            margin-bottom: 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 60px;
            color: white;
            font-weight: bold;
        }

        .name {
            font-size: 3rem;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 10px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .title {
            font-size: 1.5rem;
            color: #7f8c8d;
            margin-bottom: 20px;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 10px 20px;
            background: rgba(102, 126, 234, 0.1);
            border-radius: 25px;
            text-decoration: none;
            color: #667eea;
            font-weight: 500;
            transition: all 0.3s ease;
            border: 1px solid rgba(102, 126, 234, 0.2);
        }

        .contact-item:hover {
            background: rgba(102, 126, 234, 0.2);
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.2);
        }

        .section {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .section-title {
            font-size: 2rem;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 20px;
            text-align: center;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 2px;
        }

        .summary-text {
            font-size: 1.1rem;
            line-height: 1.8;
            color: #555;
            text-align: justify;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .skill-category {
            background: rgba(102, 126, 234, 0.05);
            border-radius: 15px;
            padding: 20px;
            border-left: 5px solid #667eea;
        }

        .skill-category h3 {
            color: #667eea;
            font-size: 1.2rem;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .skill-tag {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
        }

        .experience-item, .project-item {
            background: rgba(102, 126, 234, 0.02);
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 25px;
            border-left: 5px solid #667eea;
            transition: all 0.3s ease;
        }

        .experience-item:hover, .project-item:hover {
            transform: translateX(5px);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.1);
        }

        .job-title {
            font-size: 1.3rem;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 5px;
        }

        .company-info {
            color: #667eea;
            font-weight: 600;
            margin-bottom: 15px;
            font-size: 1rem;
        }

        .project-title {
            font-size: 1.2rem;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 10px;
        }

        .project-tech {
            background: rgba(102, 126, 234, 0.1);
            color: #667eea;
            padding: 5px 10px;
            border-radius: 15px;
            font-size: 0.9rem;
            font-weight: 500;
            display: inline-block;
            margin-bottom: 15px;
        }

        .achievement-item {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(118, 75, 162, 0.1));
            border-radius: 15px;
            padding: 20px;
            margin-bottom: 15px;
            border-left: 5px solid #f39c12;
            position: relative;
        }

        .achievement-item::before {
            content: '🏆';
            position: absolute;
            left: -15px;
            top: 50%;
            transform: translateY(-50%);
            font-size: 1.5rem;
            background: white;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .education-info {
            background: rgba(102, 126, 234, 0.05);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
        }

        .degree {
            font-size: 1.3rem;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 10px;
        }

        .university {
            color: #667eea;
            font-weight: 600;
            font-size: 1.1rem;
        }

        .year {
            color: #7f8c8d;
            margin-top: 10px;
        }

        ul {
            list-style: none;
            padding-left: 0;
        }

        li {
            position: relative;
            padding-left: 25px;
            margin-bottom: 10px;
            color: #555;
            line-height: 1.6;
        }

        li::before {
            content: '▶';
            position: absolute;
            left: 0;
            color: #667eea;
            font-size: 0.8rem;
        }

        @media (max-width: 768px) {
            .container {
                padding: 10px;
            }
            
            .header {
                padding: 30px 20px;
            }
            
            .name {
                font-size: 2rem;
            }
            
            .contact-info {
                flex-direction: column;
                align-items: center;
            }
            
            .skills-grid {
                grid-template-columns: 1fr;
            }
        }

        .stats {
            display: flex;
            justify-content: space-around;
            margin-top: 30px;
            flex-wrap: wrap;
            gap: 20px;
        }

        .stat-item {
            text-align: center;
            background: rgba(102, 126, 234, 0.1);
            padding: 20px;
            border-radius: 15px;
            min-width: 150px;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: #667eea;
            display: block;
        }

        .stat-label {
            color: #7f8c8d;
            font-weight: 500;
            margin-top: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <div class="profile-img">SH</div>
            <h1 class="name">Shabbir Hussain</h1>
            <p class="title">Senior Software Engineer | Full-Stack Developer | AI Enthusiast</p>
            <div class="contact-info">
                <a href="mailto:pshabbir36@gmail.com" class="contact-item">
                    <span>📧</span> pshabbir36@gmail.com
                </a>
                <a href="tel:+918447149834" class="contact-item">
                    <span>📱</span> +91 8447149834
                </a>
                <a href="https://www.linkedin.com/in/hshabbir36" class="contact-item">
                    <span>🔗</span> LinkedIn
                </a>
                <a href="https://github.com/shabbir-hussain-git" class="contact-item">
                    <span>🐙</span> GitHub
                </a>
                <div class="contact-item">
                    <span>📍</span> Bengaluru, Karnataka
                </div>
            </div>
            <div class="stats">
                <div class="stat-item">
                    <span class="stat-number">6+</span>
                    <span class="stat-label">Years Experience</span>
                </div>
                <div class="stat-item">
                    <span class="stat-number">10M+</span>
                    <span class="stat-label">Users Served</span>
                </div>
                <div class="stat-item">
                    <span class="stat-number">50+</span>
                    <span class="stat-label">Hours Saved</span>
                </div>
            </div>
        </div>

        <!-- Professional Summary -->
        <div class="section">
            <h2 class="section-title">Professional Summary</h2>
            <p class="summary-text">
                Accomplished Software Engineer with 6+ years of experience in full-stack development, delivering robust applications for the fantasy sports, IoT, and fintech industries. Expertise in creating mobile solutions with both React Native and native iOS, alongside web development using Next.js and React. Coupled with a strong backend proficiency in Node.js and Java, recognized for leading a successful mobile app transition and building a secure trade finance platform.
            </p>
        </div>

        <!-- Technical Skills -->
        <div class="section">
            <h2 class="section-title">Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3>Frontend Development</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">React Native</span>
                        <span class="skill-tag">React</span>
                        <span class="skill-tag">Next.js</span>
                        <span class="skill-tag">TypeScript</span>
                        <span class="skill-tag">JavaScript</span>
                    </div>
                </div>
                <div class="skill-category">
                    <h3>Backend Development</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Node.js</span>
                        <span class="skill-tag">Java</span>
                        <span class="skill-tag">Java EE</span>
                        <span class="skill-tag">REST APIs</span>
                    </div>
                </div>
                <div class="skill-category">
                    <h3>IoT & Hardware Integration</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Bluetooth Low Energy</span>
                        <span class="skill-tag">Bluetooth Mesh</span>
                    </div>
                </div>
                <div class="skill-category">
                    <h3>Cloud & DevOps</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">AWS</span>
                        <span class="skill-tag">CI/CD</span>
                        <span class="skill-tag">Git</span>
                        <span class="skill-tag">Linux</span>
                    </div>
                </div>
                <div class="skill-category">
                    <h3>AI & Advanced Technologies</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Amazon Bedrock</span>
                        <span class="skill-tag">Claude 3</span>
                        <span class="skill-tag">Mobile-MCP</span>
                        <span class="skill-tag">Microservices</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Professional Experience -->
        <div class="section">
            <h2 class="section-title">Professional Experience</h2>
            
            <div class="experience-item">
                <div class="job-title">SDE-2 (Senior Software Engineer)</div>
                <div class="company-info">Games24x7 | Bengaluru | Nov 2023 - Present</div>
                <ul>
                    <li>Develop and maintain features for the My11Circle application serving over 10 million active users, ensuring high performance in a high-traffic environment</li>
                    <li>Spearheaded the revamp of live contest features by implementing "Winner Reactions" video functionality, resulting in a 5% revenue increase and 7% boost in user engagement</li>
                    <li>Led the successful upgrade of React Native framework from v0.71 to v0.76, improving app stability and reducing build times by 20%</li>
                    <li>Integrated Sentry SDK for proactive issue monitoring, leading to a 30% reduction in critical production crashes</li>
                    <li>Engineered "Team Compare and Team Review" feature enhancing strategic gameplay, increasing average session time by 3 minutes</li>
                    <li>Implemented customer support portal with integrated Zendesk chat, reducing ticket resolution time by 25%</li>
                </ul>
            </div>

            <div class="experience-item">
                <div class="job-title">Lead Full Stack Engineer</div>
                <div class="company-info">BondBlox | Hyderabad | Oct 2021 – Nov 2023</div>
                <ul>
                    <li>Led end-to-end development of BondBlox mobile app, successfully transitioning platform to React Native to unify codebase and accelerate feature deployment</li>
                    <li>Engineered and maintained robust, scalable backend services and APIs using Node.js and MySQL on AWS infrastructure for both web and mobile platforms</li>
                </ul>
            </div>

            <div class="experience-item">
                <div class="job-title">Senior Software Engineer</div>
                <div class="company-info">Newgen Software | Noida | Jan 2018 - Oct 2021</div>
                <ul>
                    <li>Led end-to-end development of a new Trade Finance platform from concept to launch, building frontend with Angular and backend with Java EE and Oracle database</li>
                    <li>Developed and deployed automation utilities that streamlined internal processes and improved operational efficiency</li>
                </ul>
            </div>
        </div>

        <!-- Key Projects -->
        <div class="section">
            <h2 class="section-title">Key Projects</h2>
            
            <div class="project-item">
                <div class="project-title">🤖 VerifAI - AI-Powered Mobile Testing Automation</div>
                <div class="project-tech">AWS Agentic AI Hackathon Winner | January 2025</div>
                <ul>
                    <li>Led development of AI-powered mobile testing automation system that reduced PR verification time by 83% (30-60 minutes to under 10 minutes)</li>
                    <li>Architected intelligent test generation using Amazon Bedrock (Claude 3) with automated Android emulator testing via natural language instructions</li>
                    <li>Built enterprise-grade Node.js/TypeScript backend with RESTful APIs, achieving 95%+ test coverage and saving 50+ developer hours monthly</li>
                    <li><strong>Technologies:</strong> Amazon Bedrock, Claude 3, Node.js, TypeScript, Mobile-MCP, GitHub Actions, Android SDK, Jest</li>
                </ul>
            </div>

            <div class="project-item">
                <div class="project-title">🔗 ProtcoSigma Controller - BLE Mesh Network App</div>
                <div class="project-tech">React Native | TypeScript | Redux</div>
                <ul>
                    <li>Architected sophisticated cross-platform application for professional-grade management and configuration of complex Bluetooth Mesh IoT networks</li>
                    <li>Engineered robust state management system with Redux Toolkit for complex network topologies and real-time device states, integrating Nordic nRF Mesh SDK</li>
                </ul>
            </div>

            <div class="project-item">
                <div class="project-title">🎮 Magic Controller</div>
                <div class="project-tech">React Native | Bluetooth Low Energy (BLE)</div>
                <ul>
                    <li>Developed offline-first mobile application for direct binding and real-time control of smart devices, managing state, color, and intensity</li>
                    <li>Implemented advanced device grouping feature leveraging BLE broadcasting for synchronized commands to multiple devices</li>
                </ul>
            </div>

            <div class="project-item">
                <div class="project-title">⚡ FastLottie</div>
                <div class="project-tech">React Native | RNFS | AsyncStorage</div>
                <ul>
                    <li>Architected and published in-house React Native library resolving performance bottleneck through local caching mechanism for Lottie animations</li>
                    <li>Drastically reduced network dependency and load times with intelligent cache lifecycle management, improving application performance</li>
                </ul>
            </div>
        </div>

        <!-- Education -->
        <div class="section">
            <h2 class="section-title">Education</h2>
            <div class="education-info">
                <div class="degree">Bachelor of Technology (B.Tech.) in Computer Science</div>
                <div class="university">GL Bajaj Institute of Technology and Management</div>
                <div class="year">Greater Noida | 2014 – 2018</div>
            </div>
        </div>

        <!-- Achievements & Awards -->
        <div class="section">
            <h2 class="section-title">Achievements & Awards</h2>
            <div class="achievement-item">
                <strong>🏆 AWS Agentic AI Hackathon Winner</strong> - Led team to victory in prestigious AWS hackathon with innovative AI-powered mobile testing solution
            </div>
            <div class="achievement-item">
                <strong>🌟 Games24x7 Recognition Program</strong> - Awarded multiple recognitions including Rising Star, Extra Mile (4x), and Kudos (6x) for exceptional performance and contributions
            </div>
        </div>
    </div>
</body>
</html>
