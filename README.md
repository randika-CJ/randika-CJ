<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Randika Prabashwara - GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans', Helvetica, Arial, sans-serif;
            background: linear-gradient(135deg, #0d1117 0%, #161b22 100%);
            color: #c9d1d9;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(22, 27, 34, 0.8);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(48, 54, 61, 0.5);
        }

        .header {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, #58a6ff, #f78166);
            border-radius: 2px;
        }

        .name {
            font-size: 3.5rem;
            font-weight: 700;
            background: linear-gradient(45deg, #58a6ff, #f78166, #79c0ff);
            background-size: 200% 200%;
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient 3s ease infinite;
            margin-bottom: 10px;
        }

        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .greeting {
            font-size: 1.5rem;
            margin-bottom: 20px;
        }

        .title {
            font-size: 1.3rem;
            color: #7c3aed;
            font-weight: 600;
            margin-bottom: 15px;
        }

        .quote {
            font-style: italic;
            color: #8b949e;
            font-size: 1.1rem;
            margin-bottom: 30px;
            padding: 20px;
            background: rgba(13, 17, 23, 0.5);
            border-left: 4px solid #58a6ff;
            border-radius: 8px;
        }

        .section {
            margin-bottom: 40px;
        }

        .section-title {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-title span {
            font-size: 1.5rem;
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 15px;
            margin-bottom: 20px;
        }

        .about-item {
            background: rgba(13, 17, 23, 0.6);
            padding: 15px;
            border-radius: 10px;
            border-left: 4px solid #58a6ff;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .about-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(88, 166, 255, 0.1);
        }

        .tech-stack {
            margin-bottom: 30px;
        }

        .tech-category {
            margin-bottom: 20px;
        }

        .tech-category h4 {
            color: #f78166;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            align-items: center;
        }

        .badge {
            display: inline-flex;
            align-items: center;
            padding: 6px 12px;
            background: linear-gradient(135deg, #21262d, #30363d);
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 500;
            transition: all 0.3s ease;
            border: 1px solid rgba(48, 54, 61, 0.5);
            text-decoration: none;
            color: #c9d1d9;
        }

        .badge:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
            background: linear-gradient(135deg, #30363d, #21262d);
        }

        .badge.python { border-left: 4px solid #3776ab; }
        .badge.java { border-left: 4px solid #007396; }
        .badge.cpp { border-left: 4px solid #00599c; }
        .badge.javascript { border-left: 4px solid #f7df1e; }
        .badge.html { border-left: 4px solid #e34f26; }
        .badge.css { border-left: 4px solid #1572b6; }
        .badge.tensorflow { border-left: 4px solid #ff6f00; }
        .badge.pytorch { border-left: 4px solid #ee4c2c; }
        .badge.opencv { border-left: 4px solid #5c3ee8; }
        .badge.react { border-left: 4px solid #61dafb; }
        .badge.flask { border-left: 4px solid #000000; }
        .badge.mysql { border-left: 4px solid #4479a1; }
        .badge.mongodb { border-left: 4px solid #47a248; }
        .badge.aws { border-left: 4px solid #232f3e; }
        .badge.azure { border-left: 4px solid #0078d4; }

        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 25px;
        }

        .project-card {
            background: linear-gradient(135deg, rgba(13, 17, 23, 0.8), rgba(22, 27, 34, 0.9));
            border-radius: 15px;
            padding: 25px;
            border: 1px solid rgba(48, 54, 61, 0.5);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, #58a6ff, #f78166);
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(88, 166, 255, 0.15);
            border-color: #58a6ff;
        }

        .project-title {
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: #58a6ff;
        }

        .project-period {
            color: #8b949e;
            font-size: 0.9rem;
            margin-bottom: 15px;
        }

        .project-description {
            margin-bottom: 15px;
            line-height: 1.6;
        }

        .achievement {
            background: rgba(120, 219, 255, 0.1);
            padding: 10px;
            border-radius: 8px;
            margin: 10px 0;
            border-left: 3px solid #78dbff;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .stat-card {
            background: rgba(13, 17, 23, 0.8);
            border-radius: 12px;
            padding: 20px;
            border: 1px solid rgba(48, 54, 61, 0.5);
            text-align: center;
        }

        .stat-placeholder {
            width: 100%;
            height: 200px;
            background: linear-gradient(45deg, #21262d, #30363d);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #8b949e;
            font-style: italic;
            margin-bottom: 10px;
        }

        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
        }

        .achievement-item {
            background: rgba(13, 17, 23, 0.6);
            padding: 15px;
            border-radius: 10px;
            border-left: 4px solid #f78166;
            transition: transform 0.3s ease;
        }

        .achievement-item:hover {
            transform: translateX(5px);
        }

        .connect {
            text-align: center;
            margin-top: 40px;
            padding: 30px;
            background: rgba(13, 17, 23, 0.5);
            border-radius: 15px;
            border: 1px solid rgba(48, 54, 61, 0.5);
        }

        .connect-badges {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin: 20px 0;
        }

        .connect-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 20px;
            background: linear-gradient(135deg, #21262d, #30363d);
            border-radius: 25px;
            text-decoration: none;
            color: #c9d1d9;
            font-weight: 500;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .connect-badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        .connect-badge.linkedin:hover { border-color: #0077b5; box-shadow: 0 10px 20px rgba(0, 119, 181, 0.3); }
        .connect-badge.email:hover { border-color: #d14836; box-shadow: 0 10px 20px rgba(209, 72, 54, 0.3); }
        .connect-badge.github:hover { border-color: #181717; box-shadow: 0 10px 20px rgba(24, 23, 23, 0.3); }
        .connect-badge.phone:hover { border-color: #25d366; box-shadow: 0 10px 20px rgba(37, 211, 102, 0.3); }

        .footer-quote {
            text-align: center;
            font-style: italic;
            color: #8b949e;
            margin: 30px 0 20px;
            padding: 20px;
            border-top: 1px solid rgba(48, 54, 61, 0.5);
        }

        .currently-exploring {
            background: linear-gradient(135deg, rgba(120, 60, 237, 0.1), rgba(88, 166, 255, 0.1));
            padding: 20px;
            border-radius: 12px;
            border: 1px solid rgba(120, 60, 237, 0.3);
            margin: 20px 0;
        }

        @media (max-width: 768px) {
            .container { padding: 20px; }
            .name { font-size: 2.5rem; }
            .section-title { font-size: 1.5rem; }
            .about-grid { grid-template-columns: 1fr; }
            .projects { grid-template-columns: 1fr; }
            .stats-grid { grid-template-columns: 1fr; }
            .connect-badges { flex-direction: column; align-items: center; }
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <h1 class="name">👋 Randika Prabashwara</h1>
            <div class="title">Data Science Engineer | Machine Learning Enthusiast | Computer Vision Specialist</div>
            <div class="quote">
                "Energetic, risk-taking, and results-oriented rational thinker, passionate about yielding perfect results for any challenge."
            </div>
        </header>

        <section class="section">
            <h2 class="section-title"><span>🚀</span> About Me</h2>
            <div class="about-grid">
                <div class="about-item">🎓 <strong>B.Sc. Engineering (Honours)</strong> in Data Science & Engineering from University of Moratuwa (CGPA: 3.30/4.0)</div>
                <div class="about-item">💼 <strong>Data Science Engineer Intern</strong> at Brown and Company PLC</div>
                <div class="about-item">🔬 Currently working on <strong>Structure-Informed Super Resolution</strong> for Scientific Imaging</div>
                <div class="about-item">🏆 <strong>AMP®-Parkinson's Disease Progression Prediction</strong> - Kaggle Top 83%</div>
                <div class="about-item">🥇 <strong>Sri Lankan Mathematical Olympiad</strong> High Distinction (2011-2017)</div>
                <div class="about-item">📊 Published research: <em>"A Data-Driven Spatiotemporal Framework for Retail Analytics"</em> at ADScAI Summit 2025</div>
            </div>
        </section>

        <section class="section tech-stack">
            <h2 class="section-title"><span>🛠️</span> Tech Stack</h2>
            
            <div class="tech-category">
                <h4>Languages:</h4>
                <div class="badges">
                    <span class="badge python">🐍 Python</span>
                    <span class="badge java">☕ Java</span>
                    <span class="badge cpp">⚡ C++</span>
                    <span class="badge javascript">📜 JavaScript</span>
                    <span class="badge html">🌐 HTML5</span>
                    <span class="badge css">🎨 CSS3</span>
                </div>
            </div>

            <div class="tech-category">
                <h4>AI/ML:</h4>
                <div class="badges">
                    <span class="badge tensorflow">🔥 TensorFlow</span>
                    <span class="badge pytorch">⚡ PyTorch</span>
                    <span class="badge opencv">👁️ OpenCV</span>
                    <span class="badge">🧠 Keras</span>
                </div>
            </div>

            <div class="tech-category">
                <h4>Web Development:</h4>
                <div class="badges">
                    <span class="badge react">⚛️ React</span>
                    <span class="badge flask">🌶️ Flask</span>
                </div>
            </div>

            <div class="tech-category">
                <h4>Databases:</h4>
                <div class="badges">
                    <span class="badge mysql">🐬 MySQL</span>
                    <span class="badge mongodb">🍃 MongoDB</span>
                    <span class="badge">📊 HBase</span>
                </div>
            </div>

            <div class="tech-category">
                <h4>Big Data:</h4>
                <div class="badges">
                    <span class="badge">⚡ Apache Spark</span>
                    <span class="badge">🐘 Hadoop</span>
                </div>
            </div>

            <div class="tech-category">
                <h4>Cloud & Tools:</h4>
                <div class="badges">
                    <span class="badge aws">☁️ AWS</span>
                    <span class="badge azure">🔷 Microsoft Azure</span>
                    <span class="badge">📝 Git</span>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title"><span>🔥</span> Featured Projects</h2>
            <div class="projects">
                <div class="project-card">
                    <h3 class="project-title">🔬 Structure-Informed Super Resolution for Scientific Imaging</h3>
                    <div class="project-period">Final Year Project | Jun 2024 - Present</div>
                    <div class="project-description">
                        Developed state-of-the-art super-resolution framework for microscopy and nanoscience imaging with hierarchical multi-scale learning and adaptive feature fusion.
                    </div>
                    <div class="achievement">
                        <strong>Key Achievements:</strong><br>
                        • Achieved 3.5dB PSNR improvement, 20% increase in SSIM, 20% decrease in LPIPS<br>
                        • Outperformed EDSR, ESRGAN, SPSR, SwinIR, HMANet on benchmark datasets<br>
                        • Novel encoder-driven feature conditioning and Semantic Structural Loss function
                    </div>
                </div>

                <div class="project-card">
                    <h3 class="project-title">📊 Sales Insight Navigator</h3>
                    <div class="project-period">Mar 2024 - Jun 2024</div>
                    <div class="project-description">
                        Comprehensive sales analysis system with GPS tracking, behavioral analysis, and performance reporting that generates detailed insights into sales trends.
                    </div>
                    <div class="achievement">
                        <strong>Tech Stack:</strong> Python, MySQL, Flask, MS Fabric, MS Azure, OpenStreetMap
                    </div>
                </div>

                <div class="project-card">
                    <h3 class="project-title">🔍 OCR Systems</h3>
                    <div class="project-period">Dec 2023 - May 2025</div>
                    <div class="project-description">
                        <strong>Cheque OCR:</strong> Automated cheque processing with ML-enhanced text extraction<br>
                        <strong>License OCR:</strong> Driving license validation without segmentation dependencies
                    </div>
                    <div class="achievement">
                        <strong>Tech Stack:</strong> Python, OpenCV, TensorFlow, Keras
                    </div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title"><span>📈</span> GitHub Stats & Activity</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-placeholder">GitHub Stats<br>(316 contributions in the last year)</div>
                    <p>View live stats on GitHub profile</p>
                </div>
                <div class="stat-card">
                    <div class="stat-placeholder">Contribution Graph<br>(Active development across multiple repos)</div>
                    <p>Real-time contribution visualization</p>
                </div>
                <div class="stat-card">
                    <div class="stat-placeholder">Top Languages<br>(Python, JavaScript, C++, Java)</div>
                    <p>Most used programming languages</p>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title"><span>🏆</span> Achievements & Certifications</h2>
            <div class="achievements-grid">
                <div class="achievement-item">🥇 <strong>Best Result in Physical Science Stream</strong> - Prince of Wales College, Moratuwa</div>
                <div class="achievement-item">📚 <strong>AWS Academy Graduate</strong> - Data Engineering, ML for NLP, ML Foundation</div>
                <div class="achievement-item">🎓 <strong>Machine Learning Specialization</strong> - Stanford University</div>
                <div class="achievement-item">🔬 <strong>Operations Research</strong> - National Taiwan University</div>
                <div class="achievement-item">🧠 <strong>Mathematics for Machine Learning</strong> - DeepLearning.AI</div>
                <div class="achievement-item">🏥 <strong>AI for Medical Diagnosis</strong> - DeepLearning.AI</div>
            </div>
        </section>

        <div class="currently-exploring">
            <strong>💡 Currently exploring:</strong> Advanced Computer Vision techniques, Scientific Image Processing, and Big Data Analytics
        </div>

        <section class="connect">
            <h2 class="section-title"><span>📫</span> Let's Connect!</h2>
            <div class="connect-badges">
                <a href="https://linkedin.com/in/randika-prabashwara" class="connect-badge linkedin">
                    💼 LinkedIn
                </a>
                <a href="mailto:randikap.20@cse.mrt.ac.lk" class="connect-badge email">
                    📧 Email
                </a>
                <a href="https://github.com/randikapra" class="connect-badge github">
                    🐱 GitHub
                </a>
                <a href="tel:+94775747823" class="connect-badge phone">
                    📱 Phone
                </a>
            </div>
        </section>

        <div class="footer-quote">
            "Seeking opportunities to apply technical and analytical skills to address real-world complex problems and provide impactful solutions."
        </div>
    </div>
</body>
</html>
