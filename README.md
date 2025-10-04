
<!--
**AbhishekSapkal002/AbhishekSapkal002** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abhishek V. Sapkal - GitHub Portfolio</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background: #0d1117;
            color: #c9d1d9;
            line-height: 1.6;
            position: relative;
            overflow-x: hidden;
        }
        
        /* Animated Background */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 50%, rgba(88, 166, 255, 0.05) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(137, 87, 229, 0.05) 0%, transparent 50%),
                radial-gradient(circle at 40% 90%, rgba(63, 185, 80, 0.03) 0%, transparent 50%);
            z-index: -1;
            animation: bgShift 20s ease infinite;
        }
        
        @keyframes bgShift {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.7; }
        }
        
        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 24px;
        }
        
        /* Header */
        header {
            background: rgba(22, 27, 34, 0.95);
            border-bottom: 1px solid #21262d;
            padding: 16px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(10px);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 20px;
            font-weight: 600;
            color: #58a6ff;
        }
        
        .logo-icon {
            width: 32px;
            height: 32px;
            background: linear-gradient(135deg, #58a6ff, #1f6feb);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            animation: rotate 10s linear infinite;
        }
        
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        nav ul {
            display: flex;
            gap: 24px;
            list-style: none;
        }
        
        nav a {
            color: #c9d1d9;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.2s;
            padding: 6px 12px;
            border-radius: 6px;
        }
        
        nav a:hover {
            color: #58a6ff;
            background: rgba(88, 166, 255, 0.1);
        }
        
        /* Profile Section */
        .profile-section {
            padding: 80px 0;
            display: grid;
            grid-template-columns: 300px 1fr;
            gap: 40px;
            animation: fadeIn 0.6s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .profile-card {
            background: #161b22;
            border: 1px solid #21262d;
            border-radius: 12px;
            padding: 24px;
            height: fit-content;
            position: sticky;
            top: 90px;
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.3);
        }
        
        .avatar-container {
            position: relative;
            width: 100%;
            margin-bottom: 16px;
        }
        
        .avatar {
            width: 100%;
            aspect-ratio: 1;
            background: linear-gradient(135deg, #58a6ff, #1f6feb, #8957e5);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
            border: 4px solid #21262d;
            animation: pulse-border 3s ease-in-out infinite;
            position: relative;
            overflow: hidden;
        }
        
        .avatar::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.1), transparent);
            animation: shine 3s infinite;
        }
        
        @keyframes shine {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }
        
        @keyframes pulse-border {
            0%, 100% { border-color: #21262d; }
            50% { border-color: #58a6ff; }
        }
        
        .status-indicator {
            position: absolute;
            bottom: 20px;
            right: 20px;
            width: 24px;
            height: 24px;
            background: #3fb950;
            border: 3px solid #161b22;
            border-radius: 50%;
            animation: pulse-status 2s infinite;
            box-shadow: 0 0 10px #3fb950;
        }
        
        @keyframes pulse-status {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.6; transform: scale(0.95); }
        }
        
        .profile-name {
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 4px;
            color: #ffffff;
        }
        
        .profile-username {
            font-size: 20px;
            color: #8b949e;
            margin-bottom: 16px;
        }
        
        .profile-bio {
            margin-bottom: 16px;
            font-size: 14px;
            line-height: 1.5;
        }
        
        .profile-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
            margin-bottom: 16px;
        }
        
        .badge {
            padding: 4px 10px;
            background: linear-gradient(135deg, #1f6feb, #8957e5);
            border-radius: 12px;
            font-size: 11px;
            font-weight: 600;
            color: white;
            animation: float 3s ease-in-out infinite;
        }
        
        .badge:nth-child(2) { animation-delay: 0.5s; }
        .badge:nth-child(3) { animation-delay: 1s; }
        .badge:nth-child(4) { animation-delay: 1.5s; }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-3px); }
        }
        
        .profile-stats {
            display: flex;
            gap: 16px;
            padding: 16px 0;
            border-top: 1px solid #21262d;
            border-bottom: 1px solid #21262d;
            margin: 16px 0;
        }
        
        .stat {
            text-align: center;
            flex: 1;
            transition: transform 0.3s;
        }
        
        .stat:hover {
            transform: translateY(-3px);
        }
        
        .stat-value {
            display: block;
            font-size: 20px;
            font-weight: 600;
            color: #58a6ff;
        }
        
        .stat-label {
            font-size: 12px;
            color: #8b949e;
        }
        
        .profile-details {
            display: flex;
            flex-direction: column;
            gap: 8px;
            font-size: 14px;
        }
        
        .detail-item {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 4px;
            border-radius: 4px;
            transition: all 0.2s;
        }
        
        .detail-item:hover {
            background: rgba(88, 166, 255, 0.1);
        }
        
        .detail-icon {
            width: 16px;
            text-align: center;
        }
        
        .social-links {
            display: flex;
            gap: 8px;
            margin-top: 16px;
        }
        
        .social-btn {
            flex: 1;
            padding: 10px;
            background: #21262d;
            border: 1px solid #30363d;
            border-radius: 6px;
            color: #c9d1d9;
            text-decoration: none;
            text-align: center;
            font-size: 14px;
            font-weight: 500;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .social-btn::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(88, 166, 255, 0.2);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            transition: width 0.4s, height 0.4s;
        }
        
        .social-btn:hover::before {
            width: 200px;
            height: 200px;
        }
        
        .social-btn:hover {
            background: #30363d;
            border-color: #58a6ff;
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(88, 166, 255, 0.3);
        }
        
        /* Main Content */
        .main-content {
            display: flex;
            flex-direction: column;
            gap: 24px;
        }
        
        .section-card {
            background: #161b22;
            border: 1px solid #21262d;
            border-radius: 12px;
            padding: 24px;
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
            transition: all 0.3s;
        }
        
        .section-card:hover {
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.4);
        }
        
        .section-header {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 20px;
            padding-bottom: 16px;
            border-bottom: 1px solid #21262d;
        }
        
        .section-icon {
            font-size: 24px;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-5px); }
        }
        
        .section-title {
            font-size: 20px;
            font-weight: 600;
            color: #ffffff;
        }
        
        /* Pinned Repos */
        .repos-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 16px;
        }
        
        .repo-card {
            background: #0d1117;
            border: 1px solid #21262d;
            border-radius: 8px;
            padding: 16px;
            transition: all 0.3s;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }
        
        .repo-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(88, 166, 255, 0.1), transparent);
            transition: left 0.5s;
        }
        
        .repo-card:hover::before {
            left: 100%;
        }
        
        .repo-card:hover {
            border-color: #58a6ff;
            transform: translateY(-4px);
            box-shadow: 0 8px 20px rgba(88, 166, 255, 0.2);
        }
        
        .repo-header {
            display: flex;
            align-items: start;
            gap: 8px;
            margin-bottom: 8px;
        }
        
        .repo-icon {
            color: #8b949e;
            font-size: 16px;
            margin-top: 2px;
        }
        
        .repo-name {
            font-size: 14px;
            font-weight: 600;
            color: #58a6ff;
            flex: 1;
            transition: color 0.2s;
        }
        
        .repo-card:hover .repo-name {
            color: #79c0ff;
        }
        
        .repo-visibility {
            padding: 2px 8px;
            background: #21262d;
            border: 1px solid #30363d;
            border-radius: 12px;
            font-size: 10px;
            color: #8b949e;
        }
        
        .repo-desc {
            font-size: 12px;
            color: #8b949e;
            margin-bottom: 12px;
            line-height: 1.5;
        }
        
        .repo-footer {
            display: flex;
            align-items: center;
            gap: 16px;
            font-size: 12px;
        }
        
        .repo-language {
            display: flex;
            align-items: center;
            gap: 4px;
        }
        
        .language-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            animation: glow 2s ease-in-out infinite;
        }
        
        @keyframes glow {
            0%, 100% { box-shadow: 0 0 5px currentColor; }
            50% { box-shadow: 0 0 10px currentColor; }
        }
        
        .python { background: #3572A5; }
        .javascript { background: #f1e05a; }
        .cpp { background: #f34b7d; }
        
        .repo-stats {
            display: flex;
            align-items: center;
            gap: 4px;
            color: #8b949e;
            transition: color 0.2s;
        }
        
        .repo-stats:hover {
            color: #58a6ff;
        }
        
        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 16px;
        }
        
        .skill-group {
            background: #0d1117;
            border: 1px solid #21262d;
            border-radius: 8px;
            padding: 16px;
            transition: all 0.3s;
        }
        
        .skill-group:hover {
            border-color: #58a6ff;
            transform: translateY(-3px);
            box-shadow: 0 4px 12px rgba(88, 166, 255, 0.2);
        }
        
        .skill-group-title {
            font-size: 14px;
            font-weight: 600;
            color: #58a6ff;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }
        
        .skill-tag {
            padding: 6px 12px;
            background: #21262d;
            border: 1px solid #30363d;
            border-radius: 20px;
            font-size: 12px;
            color: #c9d1d9;
            transition: all 0.2s;
            cursor: pointer;
        }
        
        .skill-tag:hover {
            background: linear-gradient(135deg, #1f6feb, #8957e5);
            border-color: #58a6ff;
            transform: scale(1.05);
            color: white;
        }
        
        /* Contribution Graph */
        .contribution-graph {
            padding: 16px;
            background: #0d1117;
            border: 1px solid #21262d;
            border-radius: 8px;
            overflow-x: auto;
        }
        
        .graph-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 12px;
        }
        
        .graph-title {
            font-size: 14px;
            font-weight: 600;
        }
        
        .graph-legend {
            display: flex;
            gap: 8px;
            align-items: center;
            font-size: 11px;
            color: #8b949e;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 4px;
        }
        
        .legend-box {
            width: 10px;
            height: 10px;
            border-radius: 2px;
        }
        
        .graph-grid {
            display: grid;
            grid-template-columns: repeat(52, 12px);
            gap: 3px;
        }
        
        .contribution-day {
            width: 12px;
            height: 12px;
            background: #161b22;
            border-radius: 2px;
            border: 1px solid #21262d;
            transition: all 0.2s;
            cursor: pointer;
        }
        
        .contribution-day:hover {
            border-color: #58a6ff;
            transform: scale(1.2);
        }
        
        .contribution-day.level-1 { background: #0e4429; }
        .contribution-day.level-2 { background: #006d32; }
        .contribution-day.level-3 { background: #26a641; }
        .contribution-day.level-4 { background: #39d353; }
        
        /* Timeline */
        .timeline {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .timeline-item {
            position: relative;
            padding-left: 32px;
            border-left: 2px solid #21262d;
            padding-bottom: 20px;
            animation: slideIn 0.5s ease;
        }
        
        @keyframes slideIn {
            from { opacity: 0; transform: translateX(-20px); }
            to { opacity: 1; transform: translateX(0); }
        }
        
        .timeline-item:last-child {
            padding-bottom: 0;
        }
        
        .timeline-dot {
            position: absolute;
            left: -7px;
            top: 4px;
            width: 12px;
            height: 12px;
            background: #58a6ff;
            border-radius: 50%;
            border: 2px solid #0d1117;
            animation: pulse-dot 2s infinite;
        }
        
        @keyframes pulse-dot {
            0%, 100% { box-shadow: 0 0 0 0 rgba(88, 166, 255, 0.4); }
            50% { box-shadow: 0 0 0 8px rgba(88, 166, 255, 0); }
        }
        
        .timeline-content {
            background: #0d1117;
            border: 1px solid #21262d;
            border-radius: 8px;
            padding: 16px;
            transition: all 0.3s;
        }
        
        .timeline-content:hover {
            border-color: #58a6ff;
            transform: translateX(5px);
            box-shadow: 0 4px 12px rgba(88, 166, 255, 0.2);
        }
        
        .timeline-title {
            font-size: 16px;
            font-weight: 600;
            color: #ffffff;
            margin-bottom: 4px;
        }
        
        .timeline-subtitle {
            font-size: 14px;
            color: #58a6ff;
            margin-bottom: 8px;
        }
        
        .timeline-meta {
            font-size: 12px;
            color: #8b949e;
        }
        
        /* Achievement Badges */
        .achievements {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 12px;
            margin-top: 16px;
        }
        
        .achievement-badge {
            background: #0d1117;
            border: 1px solid #21262d;
            border-radius: 8px;
            padding: 16px;
            text-align: center;
            transition: all 0.3s;
            cursor: pointer;
        }
        
        .achievement-badge:hover {
            border-color: #58a6ff;
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 16px rgba(88, 166, 255, 0.3);
        }
        
        .achievement-icon {
            font-size: 32px;
            margin-bottom: 8px;
            animation: wiggle 2s ease-in-out infinite;
        }
        
        @keyframes wiggle {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(-10deg); }
            75% { transform: rotate(10deg); }
        }
        
        .achievement-name {
            font-size: 12px;
            font-weight: 600;
            color: #c9d1d9;
        }
        
        /* Footer */
        footer {
            background: #161b22;
            border-top: 1px solid #21262d;
            padding: 40px 0;
            margin-top: 80px;
            text-align: center;
        }
        
        .footer-text {
            color: #8b949e;
            font-size: 14px;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            gap: 24px;
            margin-top: 16px;
        }
        
        .footer-links a {
            color: #58a6ff;
            text-decoration: none;
            font-size: 14px;
            transition: all 0.2s;
        }
        
        .footer-links a:hover {
            color: #79c0ff;
            text-decoration: underline;
        }
        
        @media (max-width: 1024px) {
            .profile-section {
                grid-template-columns: 1fr;
            }
            
            .profile-card {
                position: relative;
                top: 0;
            }
            
            .repos-grid {
                grid-template-columns: 1fr;
            }
            
            .skills-container {
                grid-template-columns: 1fr;
            }
            
            .achievements {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 768px) {
            nav ul {
                gap: 12px;
                font-size: 14px;
            }
            
            .profile-section {
                padding: 40px 0;
            }
            
            .achievements {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <div class="logo-icon">👨‍💻</div>
                    <span>abhishek-sapkal</span>
                </div>
                <nav>
                    <ul>
                        <li><a href="#overview">Overview</a></li>
                        <li><a href="#repositories">Repositories</a></li>
                        <li><a href="#skills">Skills</a></li>
                        <li><a href="#education">Education</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <div class="container">
        <div class="profile-section" id="overview">
            <aside class="profile-card">
                <div class="avatar-container">
                    <div class="avatar">👨‍💻</div>
                    <div class="status-indicator"></div>
                </div>
                
                <h1 class="profile-name">Abhishek V. Sapkal</h1>
                <p class="profile-username">@abhishek-sapkal</p>
                
                <p class="profile-bio">
                    Ambitious Computer Engineering undergraduate passionate about ML, Data Science, and building intelligent solutions.
                </p>
                
                <div class="profile-badges">
                    <span class="badge">ML Engineer</span>
                    <span class="badge">Data Scientist</span>
                    <span class="badge">Full Stack</span>
                    <span class="badge">Cybersecurity</span>
                </div>
                
                <div class="profile-stats">
                    <div class="stat">
                        <span class="stat-value">15</span>
                        <span class="stat-label">Repos</span>
                    </div>
                    <div class="stat">
                        <span class="stat-value">8.32</span>
                        <span class="stat-label">GPA</span>
                    </div>
                    <div class="stat">
                        <span class="stat-value">520</span>
                        <span class="stat-label">Commits</span>
                    </div>
                </div>
                
                <div class="profile-details">
                    <div class="detail-item">
                        <span class="detail-icon">🎓</span>
                        <span>BE Computer Engineering</span>
                    </div>
                    <div class="detail-item">
                        <span class="detail-icon">🏢</span>
                        <span>Zeal College of Engineering</span>
                    </div>
                    <div class="detail-item">
                        <span class="detail-icon">📍</span>
                        <span>Pune, India</span>
                    </div>
                    <div class="detail-item">
                        <span class="detail-icon">📧</span>
                        <span>abhisheksapkal002@gmail.com</span>
                    </div>
                </div>
                
                <div class="social-links">
                    <a href="https://www.linkedin.com/in/abhishek-sapkal-b11881263" class="social-btn" target="_blank">LinkedIn</a>
                    <a href="mailto:abhisheksapkal002@gmail.com" class="social-btn">Email</a>
                </div>
            </aside>

            <main class="main-content">
                <div class="section-card" id="repositories">
                    <div class="section-header">
                        <span class="section-icon">📌</span>
                        <h2 class="section-title">Pinned Repositories</h2>
                    </div>
                    
                    <div class="repos-grid">
                        <div class="repo-card">
                            <div class="repo-header">
                                <span class="repo-icon">📁</span>
                                <div class="repo-name">Argumentor-AI-Coach</div>
                                <span class="repo-visibility">Public</span>
                            </div>
                            <p class="repo-desc">An AI platform analyzing speech for real-time public speaking feedback using NLP and speech recognition.</p>
                            <div class="repo-footer">
                                <div class="repo-language">
                                    <span class="language-dot python"></span>
                                    <span>Python</span>
                                </div>
                                <div class="repo-stats">
                                    <span>⭐</span>
                                    <span>12</span>
                                </div>
                                <div class="repo-stats">
                                    <span>🔱</span>
                                    <span>3</span>
                                </div>
                            </div>
                        </div>
                        
                        <div class="repo-card">
                            <div class="repo-header">
                                <span class="repo-icon">📁</span>
                                <div class="repo-name">Sign-Bridge-Translator</div>
                                <span class="repo-visibility">Public</span>
                            </div>
                            <p class="repo-desc">Deep learning application translating ASL gestures into text via webcam using computer vision.</p>
                            <div class="repo-footer">
                                <div class="repo-language">
                                    <span class="language-dot python"></span>
                                    <span>Python</span>
                                </div>
                                <div class="repo-stats">
                                    <span>⭐</span>
                                    <span>18</span>
                                </div>
                                <div class="repo-stats">
                                    <span>🔱</span>
                                    <span>5</span>
                                </div>
                            </div>
                        </div>
                        
                        <div class="repo-card">
                            <div class="repo-header">
                                <span class="repo-icon">📁</span>
                                <div class="repo-name">Credit-Risk-Evaluation</div>
                                <span class="repo-visibility">Public</span>
                            </div>
                            <p class="repo-desc">Machine learning model to predict creditworthiness and minimize financial risk using scikit-learn.</p>
                            <div class="repo-footer">
                                <div class="repo-language">
                                    <span class="language-dot python"></span>
                                    <span>Python</span>
                                </div>
                                <div class="repo-stats">
                                    <span>⭐</span>
                                    <span>15</span>
                                </div>
                                <div class="repo-stats">
                                    <span>🔱</span>
                                    <span>4</span>
                                </div>
                            </div>
                        </div>
                        
                        <div class="repo-card">
                            <div class="repo-header">
                                <span class="repo-icon">📁</span>
                                <div class="repo-name">Portfolio-Website</div>
                                <span class="repo-visibility">Public</span>
                            </div>
                            <p class="repo-desc">Personal portfolio website showcasing projects, skills, and professional experience.</p>
                            <div class="repo-footer">
                                <div class="repo-language">
                                    <span class="language-dot javascript"></span>
                                    <span>JavaScript</span>
                                </div>
                                <div class="repo-stats">
                                    <span>⭐</span>
                                    <span>8</span>
                                </div>
                                <div class="repo-stats">
                                    <span>🔱</span>
                                    <span>2</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="section-card">
                    <div class="section-header">
                        <span class="section-icon">🏆</span>
                        <h2 class="section-title">Achievements</h2>
                    </div>
                    <div class="achievements">
                        <div class="achievement-badge">
                            <div class="achievement-icon">🎓</div>
                            <div class="achievement-name">Google Certified</div>
                        </div>
                        <div class="achievement-badge">
                            <div class="achievement-icon">🌟</div>
                            <div class="achievement-name">Stanford Alumni</div>
                        </div>
                        <div class="achievement-badge">
                            <div class="achievement-icon">💻</div>
                            <div class="achievement-name">ML Expert</div>
                        </div>
                        <div class="achievement-badge">
                            <div class="achievement-icon">🔒</div>
                            <div class="achievement-name">Security Pro</div>
                        </div>
                    </div>
                </div>

                <div class="section-card">
                    <div class="section-header">
                        <span class="section-icon">📊</span>
                        <h2 class="section-title">Contribution Activity</h2>
                    </div>
                    <div class="contribution-graph">
                        <div class="graph-header">
                            <div class="graph-title">520 contributions in the last year</div>
                            <div class="graph-legend">
                                <span>Less</span>
                                <div class="legend-item">
                                    <div class="legend-box" style="background: #161b22;"></div>
                                </div>
                                <div class="legend-item">
                                    <div class="legend-box" style="background: #0e4429;"></div>
                                </div>
                                <div class="legend-item">
                                    <div class="legend-box" style="background: #006d32;"></div>
                                </div>
                                <div class="legend-item">
                                    <div class="legend-box" style="background: #26a641;"></div>
                                </div>
                                <div class="legend-item">
                                    <div class="legend-box" style="background: #39d353;"></div>
                                </div>
                                <span>More</span>
                            </div>
                        </div>
                        <div class="graph-grid" id="contributionGrid"></div>
                    </div>
                </div>

                <div class="section-card" id="skills">
                    <div class="section-header">
                        <span class="section-icon">💻</span>
                        <h2 class="section-title">Technical Skills</h2>
                    </div>
                    
                    <div class="skills-container">
                        <div class="skill-group">
                            <div class="skill-group-title">
                                <span>⚡</span>
                                Languages
                            </div>
                            <div class="skill-tags">
                                <span class="skill-tag">Python</span>
                                <span class="skill-tag">C++</span>
                                <span class="skill-tag">SQL</span>
                                <span class="skill-tag">JavaScript</span>
                                <span class="skill-tag">HTML</span>
                                <span class="skill-tag">CSS</span>
                            </div>
                        </div>
                        
                        <div class="skill-group">
                            <div class="skill-group-title">
                                <span>🤖</span>
                                Data Science & ML
                            </div>
                            <div class="skill-tags">
                                <span class="skill-tag">Scikit-learn</span>
                                <span class="skill-tag">Pandas</span>
                                <span class="skill-tag">NumPy</span>
                                <span class="skill-tag">Matplotlib</span>
                                <span class="skill-tag">TensorFlow</span>
                            </div>
                        </div>
                        
                        <div class="skill-group">
                            <div class="skill-group-title">
                                <span>🛠️</span>
                                Frameworks & Tools
                            </div>
                            <div class="skill-tags">
                                <span class="skill-tag">Django</span>
                                <span class="skill-tag">MySQL</span>
                                <span class="skill-tag">MongoDB</span>
                                <span class="skill-tag">Git</span>
                                <span class="skill-tag">Docker</span>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="section-card" id="education">
                    <div class="section-header">
                        <span class="section-icon">🎓</span>
                        <h2 class="section-title">Education & Certifications</h2>
                    </div>
                    
                    <div class="timeline">
                        <div class="timeline-item">
                            <div class="timeline-dot"></div>
                            <div class="timeline-content">
                                <div class="timeline-title">BE Computer Engineering</div>
                                <div class="timeline-subtitle">Zeal College of Engineering and Research</div>
                                <div class="timeline-meta">2022 - 2026 • GPA: 8.32/10.0 • Pune, India</div>
                            </div>
                        </div>
                        
                        <div class="timeline-item">
                            <div class="timeline-dot"></div>
                            <div class="timeline-content">
                                <div class="timeline-title">Google Cybersecurity Professional Certificate</div>
                                <div class="timeline-subtitle">Google</div>
                                <div class="timeline-meta">2024 • Professional Certification</div>
                            </div>
                        </div>
                        
                        <div class="timeline-item">
                            <div class="timeline-dot"></div>
                            <div class="timeline-content">
                                <div class="timeline-title">Code in Place - Python Programming</div>
                                <div class="timeline-subtitle">Stanford University</div>
                                <div class="timeline-meta">2024 • Online Course</div>
                            </div>
                        </div>
                        
                        <div class="timeline-item">
                            <div class="timeline-dot"></div>
                            <div class="timeline-content">
                                <div class="timeline-title">Employability Skill Development</div>
                                <div class="timeline-subtitle">Zensar Technologies</div>
                                <div class="timeline-meta">2023 • Professional Training</div>
                            </div>
                        </div>
                    </div>
                </div>
            </main>
        </div>
    </div>

    <footer>
        <div class="container">
            <p class="footer-text">© 2024 Abhishek V. Sapkal. All rights reserved.</p>
            <div class="footer-links">
                <a href="https://www.linkedin.com/in/abhishek-sapkal-b11881263" target="_blank">LinkedIn</a>
                <a href="mailto:abhisheksapkal002@gmail.com">Email</a>
                <a href="#">GitHub</a>
            </div>
        </div>
    </footer>

    <script>
        // Generate contribution graph
        const graphGrid = document.getElementById('contributionGrid');
        for (let i = 0; i < 364; i++) {
            const level = Math.floor(Math.random() * 5);
            const div = document.createElement('div');
            div.className = `contribution-day${level > 0 ? ' level-' + level : ''}`;
            graphGrid.appendChild(div);
        }
    </script>
</body>
</html>
