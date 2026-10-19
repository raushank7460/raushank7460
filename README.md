<!DOCTYPE html>
<html lang="en" class="dark scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Raushan Kumar | MERN Stack Developer & Backend Specialist</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        brand: {
                            orange: '#ff512f',
                            pink: '#dd2476',
                            dark: '#0f172a',
                            card: '#1e293b'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        code: ['Fira Code', 'monospace']
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;600&family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Custom CSS Styling & Animations -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0b0f19;
            color: #f8fafc;
            overflow-x: hidden;
        }
        .gradient-text {
            background: linear-gradient(135deg, #ff512f 0%, #dd2476 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .gradient-border {
            border: 2px solid transparent;
            background: linear-gradient(#1e293b, #1e293b) padding-box,
                        linear-gradient(135deg, #ff512f, #dd2476) border-box;
        }
        .glass-card {
            background: rgba(30, 41, 59, 0.7);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }
        .glass-card:hover {
            border-color: rgba(221, 36, 118, 0.4);
            box-shadow: 0 10px 30px -10px rgba(221, 36, 118, 0.2);
        }
        .glow-btn {
            background: linear-gradient(135deg, #ff512f 0%, #dd2476 100%);
            transition: all 0.3s ease;
        }
        .glow-btn:hover {
            opacity: 0.9;
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(221, 36, 118, 0.4);
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0f172a;
        }
        ::-webkit-scrollbar-thumb {
            background: #334155;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #dd2476;
        }
    </style>
</head>
<body class="bg-[#0b0f19] text-slate-100 selection:bg-pink-500 selection:text-white">

    <!-- Notification Toast -->
    <div id="toast" class="fixed bottom-5 right-5 z-50 transform translate-y-20 opacity-0 transition-all duration-300 glass-card px-6 py-4 rounded-xl shadow-2xl flex items-center space-x-3 border-l-4 border-pink-500">
        <i id="toast-icon" class="fa-solid fa-circle-check text-pink-500 text-xl"></i>
        <div>
            <h4 id="toast-title" class="font-bold text-sm">Success</h4>
            <p id="toast-message" class="text-xs text-slate-400">Action completed successfully.</p>
        </div>
    </div>

    <!-- Navigation Bar -->
    <nav class="fixed top-0 left-0 right-0 z-40 glass-card border-b border-slate-800/80 backdrop-blur-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <a href="#" class="flex items-center space-x-3 group">
                <div class="w-10 h-10 rounded-xl glow-btn flex items-center justify-center font-bold text-white text-lg shadow-lg group-hover:scale-105 transition-transform">
                    RK
                </div>
                <span class="font-bold text-xl tracking-tight gradient-text font-code">Raushan Kumar</span>
            </a>

            <!-- Desktop Nav Links -->
            <div class="hidden md:flex items-center space-x-8 font-medium text-sm">
                <a href="#about" class="text-slate-300 hover:text-pink-500 transition-colors">About</a>
                <a href="#skills" class="text-slate-300 hover:text-pink-500 transition-colors">Tech Stack</a>
                <a href="#projects" class="text-slate-300 hover:text-pink-500 transition-colors">Projects</a>
                <a href="#contact" class="text-slate-300 hover:text-pink-500 transition-colors">Contact</a>
            </div>

            <!-- Action Buttons -->
            <div class="hidden md:flex items-center space-x-4">
                <a href="mailto:raushank7460@gmail.com" class="px-5 py-2.5 rounded-xl glow-btn text-white font-medium text-sm flex items-center space-x-2">
                    <i class="fa-solid fa-paper-plane"></i>
                    <span>Let's Talk</span>
                </a>
            </div>

            <!-- Mobile Menu Toggle -->
            <button id="menu-btn" class="md:hidden text-slate-300 hover:text-white focus:outline-none p-2">
                <i class="fa-solid fa-bars text-2xl"></i>
            </button>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden glass-card border-t border-slate-800 px-6 py-6 space-y-4">
            <a href="#about" class="block text-slate-300 hover:text-pink-500 font-medium py-1">About</a>
            <a href="#skills" class="block text-slate-300 hover:text-pink-500 font-medium py-1">Tech Stack</a>
            <a href="#projects" class="block text-slate-300 hover:text-pink-500 font-medium py-1">Projects</a>
            <a href="#contact" class="block text-slate-300 hover:text-pink-500 font-medium py-1">Contact</a>
            <div class="pt-2">
                <a href="mailto:raushank7460@gmail.com" class="w-full py-3 rounded-xl glow-btn text-white font-medium text-sm flex items-center justify-center space-x-2">
                    <i class="fa-solid fa-paper-plane"></i>
                    <span>Let's Talk</span>
                </a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="relative pt-32 pb-20 md:pt-44 md:pb-32 overflow-hidden flex items-center justify-center">
        <!-- Background Glow Blobs -->
        <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-pink-600/20 rounded-full blur-3xl pointer-events-none"></div>
        <div class="absolute top-1/3 left-1/4 w-72 h-72 bg-orange-500/20 rounded-full blur-3xl pointer-events-none"></div>

        <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 text-center relative z-10">
            <!-- Open to Work Badge -->
            <div class="inline-flex items-center space-x-2 px-4 py-1.5 rounded-full glass-card border border-pink-500/30 text-xs sm:text-sm mb-6 animate-pulse">
                <span class="w-2.5 h-2.5 rounded-full bg-emerald-400"></span>
                <span class="font-medium text-slate-200">Open to SDE / Backend Developer Roles</span>
            </div>

            <h1 class="text-4xl sm:text-6xl md:text-7xl font-extrabold tracking-tight mb-4">
                Hi, I'm <span class="gradient-text">Raushan Kumar</span>
            </h1>

            <!-- Typing Subtitle -->
            <div class="h-16 sm:h-12 flex items-center justify-center mb-6">
                <p id="typing-text" class="font-code text-lg sm:text-2xl text-pink-400 font-semibold border-r-2 border-pink-500 pr-1 animate-pulse"></p>
            </div>

            <p class="max-w-2xl mx-auto text-slate-400 text-base sm:text-lg mb-10">
                B.Tech CSE student at GLA University (2027) crafting robust backend architectures, scalable REST APIs, and seamless full-stack web applications.
            </p>

            <!-- Social & Action Links -->
            <div class="flex flex-wrap items-center justify-center gap-4 mb-12">
                <a href="https://www.linkedin.com/in/raushan-kumar-449969421" target="_blank" class="px-5 py-3 rounded-xl glass-card hover:bg-slate-800 text-slate-200 font-medium text-sm flex items-center space-x-2 transition-all">
                    <i class="fa-brands fa-linkedin text-blue-400 text-lg"></i>
                    <span>LinkedIn</span>
                </a>
                <a href="https://leetcode.com/u/raushanx05/" target="_blank" class="px-5 py-3 rounded-xl glass-card hover:bg-slate-800 text-slate-200 font-medium text-sm flex items-center space-x-2 transition-all">
                    <i class="fa-solid fa-code text-amber-400 text-lg"></i>
                    <span>LeetCode (400+ Solved)</span>
                </a>
                <a href="mailto:raushank7460@gmail.com" class="px-5 py-3 rounded-xl glass-card hover:bg-slate-800 text-slate-200 font-medium text-sm flex items-center space-x-2 transition-all">
                    <i class="fa-solid fa-envelope text-red-400 text-lg"></i>
                    <span>Email Me</span>
                </a>
            </div>

            <!-- Quick Stats Grid -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 max-w-4xl mx-auto">
                <div class="glass-card p-5 rounded-2xl text-center">
                    <h3 class="text-3xl font-ext500 font-bold gradient-text mb-1">400+</h3>
                    <p class="text-xs text-slate-400 font-medium">LeetCode Problems</p>
                </div>
                <div class="glass-card p-5 rounded-2xl text-center">
                    <h3 class="text-3xl font-bold gradient-text mb-1">MERN</h3>
                    <p class="text-xs text-slate-400 font-medium">Stack Specialist</p>
                </div>
                <div class="glass-card p-5 rounded-2xl text-center">
                    <h3 class="text-3xl font-bold gradient-text mb-1">4+</h3>
                    <p class="text-xs text-slate-400 font-medium">Featured Projects</p>
                </div>
                <div class="glass-card p-5 rounded-2xl text-center">
                    <h3 class="text-3xl font-bold gradient-text mb-1">2027</h3>
                    <p class="text-xs text-slate-400 font-medium">GLA University CSE</p>
                </div>
            </div>
        </div>
    </header>

    <div class="w-full h-px bg-gradient-to-r from-transparent via-pink-500/50 to-transparent my-10"></div>

    <!-- About Me Section -->
    <section id="about" class="py-20 relative">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl sm:text-4xl font-extrabold mb-3">About <span class="gradient-text">Me</span></h2>
                <div class="w-20 h-1.5 glow-btn mx-auto rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-10 items-center">
                <div class="glass-card p-8 rounded-3xl relative overflow-hidden">
                    <div class="absolute top-0 right-0 w-40 h-40 bg-gradient-to-br from-orange-500/10 to-pink-500/10 rounded-bl-full pointer-events-none"></div>
                    <h3 class="text-2xl font-bold mb-4 flex items-center space-x-3">
                        <i class="fa-solid fa-terminal text-pink-500"></i>
                        <span>Backend Focused Developer</span>
                    </h3>
                    <p class="text-slate-300 leading-relaxed mb-6 text-base">
                        I'm a passionate B.Tech Computer Science & Engineering student currently studying at <strong class="text-white">GLA University (Batch of 2027)</strong>. My core expertise lies in designing scalable RESTful APIs, securing applications with JWT authentication, and architecting robust database schemas.
                    </p>
                    <p class="text-slate-300 leading-relaxed mb-6 text-base">
                        Alongside full-stack web development using the <strong class="text-white">MERN stack</strong>, I am a dedicated problem solver with over <strong class="text-pink-400">400+ problems solved</strong> on LeetCode utilizing Java. Currently, I'm expanding my skill set by learning enterprise backend development with <strong class="text-emerald-400">Spring Boot</strong>.
                    </p>
                    <div class="flex flex-wrap gap-3">
                        <span class="px-3 py-1.5 rounded-lg bg-slate-800 text-xs font-mono text-pink-400 border border-slate-700">Java & DSA</span>
                        <span class="px-3 py-1.5 rounded-lg bg-slate-800 text-xs font-mono text-pink-400 border border-slate-700">REST APIs</span>
                        <span class="px-3 py-1.5 rounded-lg bg-slate-800 text-xs font-mono text-pink-400 border border-slate-700">Database Design</span>
                        <span class="px-3 py-1.5 rounded-lg bg-slate-800 text-xs font-mono text-emerald-400 border border-slate-700">Spring Boot (Learning)</span>
                    </div>
                </div>

                <div class="space-y-6">
                    <div class="glass-card p-6 rounded-2xl flex items-start space-x-4">
                        <div class="w-12 h-12 rounded-xl bg-pink-500/10 flex items-center justify-center shrink-0 text-pink-500 text-xl">
                            <i class="fa-solid fa-graduation-cap"></i>
                        </div>
                        <div>
                            <h4 class="text-lg font-bold mb-1">Education</h4>
                            <p class="text-sm text-slate-300">B.Tech in Computer Science & Engineering</p>
                            <p class="text-xs text-pink-400 font-medium mt-1">GLA University • Expected 2027</p>
                        </div>
                    </div>

                    <div class="glass-card p-6 rounded-2xl flex items-start space-x-4">
                        <div class="w-12 h-12 rounded-xl bg-orange-500/10 flex items-center justify-center shrink-0 text-orange-500 text-xl">
                            <i class="fa-solid fa-bolt"></i>
                        </div>
                        <div>
                            <h4 class="text-lg font-bold mb-1">DSA & Problem Solving</h4>
                            <p class="text-sm text-slate-300">Solved 400+ algorithmic problems using Java.</p>
                            <p class="text-xs text-orange-400 font-medium mt-1">Focus on efficiency and data structures.</p>
                        </div>
                    </div>

                    <div class="glass-card p-6 rounded-2xl flex items-start space-x-4">
                        <div class="w-12 h-12 rounded-xl bg-purple-500/10 flex items-center justify-center shrink-0 text-purple-400 text-xl">
                            <i class="fa-solid fa-bullseye"></i>
                        </div>
                        <div>
                            <h4 class="text-lg font-bold mb-1">Current Objective</h4>
                            <p class="text-sm text-slate-300">Seeking SDE / Backend Developer internships or full-time roles.</p>
                            <p class="text-xs text-purple-400 font-medium mt-1">Ready to contribute to high-impact teams.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="w-full h-px bg-gradient-to-r from-transparent via-pink-500/50 to-transparent my-10"></div>

    <!-- Tech Stack Section -->
    <section id="skills" class="py-20 relative">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl sm:text-4xl font-extrabold mb-3">Tech <span class="gradient-text">Stack</span></h2>
                <div class="w-20 h-1.5 glow-btn mx-auto rounded-full"></div>
                <p class="text-slate-400 mt-4 text-sm sm:text-base">Technologies, tools, and cloud platforms I work with</p>
            </div>

            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-6">
                <!-- JavaScript -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=js" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="JavaScript">
                    <h4 class="font-bold text-sm">JavaScript</h4>
                    <span class="text-xs text-slate-400 mt-1">Language</span>
                </div>
                <!-- Java -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=java" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="Java">
                    <h4 class="font-bold text-sm">Java</h4>
                    <span class="text-xs text-slate-400 mt-1">DSA & Backend</span>
                </div>
                <!-- Python -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=py" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="Python">
                    <h4 class="font-bold text-sm">Python</h4>
                    <span class="text-xs text-slate-400 mt-1">Language</span>
                </div>
                <!-- React -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=react" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="React">
                    <h4 class="font-bold text-sm">React.js</h4>
                    <span class="text-xs text-slate-400 mt-1">Frontend</span>
                </div>
                <!-- Node.js -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=nodejs" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="Node.js">
                    <h4 class="font-bold text-sm">Node.js</h4>
                    <span class="text-xs text-slate-400 mt-1">Backend</span>
                </div>
                <!-- Express.js -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=express" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="Express">
                    <h4 class="font-bold text-sm">Express.js</h4>
                    <span class="text-xs text-slate-400 mt-1">Framework</span>
                </div>
                <!-- Spring Boot -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=spring" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="Spring Boot">
                    <h4 class="font-bold text-sm">Spring Boot</h4>
                    <span class="text-xs text-slate-400 mt-1">Learning</span>
                </div>
                <!-- MongoDB -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=mongodb" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="MongoDB">
                    <h4 class="font-bold text-sm">MongoDB</h4>
                    <span class="text-xs text-slate-400 mt-1">Database</span>
                </div>
                <!-- MySQL -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=mysql" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="MySQL">
                    <h4 class="font-bold text-sm">MySQL</h4>
                    <span class="text-xs text-slate-400 mt-1">Database</span>
                </div>
                <!-- Git & GitHub -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=github" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="GitHub">
                    <h4 class="font-bold text-sm">Git & GitHub</h4>
                    <span class="text-xs text-slate-400 mt-1">Version Control</span>
                </div>
                <!-- Postman -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=postman" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="Postman">
                    <h4 class="font-bold text-sm">Postman</h4>
                    <span class="text-xs text-slate-400 mt-1">API Testing</span>
                </div>
                <!-- Vercel -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=vercel" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="Vercel">
                    <h4 class="font-bold text-sm">Vercel</h4>
                    <span class="text-xs text-slate-400 mt-1">Deployment</span>
                </div>
                <!-- Render -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <div class="w-14 h-14 mb-3 rounded-xl bg-emerald-500/10 flex items-center justify-center text-emerald-400 text-2xl font-bold">R</div>
                    <h4 class="font-bold text-sm">Render</h4>
                    <span class="text-xs text-slate-400 mt-1">Cloud Hosting</span>
                </div>
                <!-- MongoDB Atlas -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <div class="w-14 h-14 mb-3 rounded-xl bg-emerald-500/10 flex items-center justify-center text-emerald-400 text-xl font-bold"><i class="fa-solid fa-database"></i></div>
                    <h4 class="font-bold text-sm">MongoDB Atlas</h4>
                    <span class="text-xs text-slate-400 mt-1">Cloud DB</span>
                </div>
                <!-- VS Code -->
                <div class="glass-card p-6 rounded-2xl flex flex-col items-center justify-center text-center group hover:-translate-y-2 transition-all">
                    <img src="https://skillicons.dev/icons?i=vscode" class="w-14 h-14 mb-3 group-hover:scale-110 transition-transform" alt="VS Code">
                    <h4 class="font-bold text-sm">VS Code</h4>
                    <span class="text-xs text-slate-400 mt-1">Editor</span>
                </div>
            </div>
        </div>
    </section>

    <div class="w-full h-px bg-gradient-to-r from-transparent via-pink-500/50 to-transparent my-10"></div>

    <!-- Featured Projects Section -->
    <section id="projects" class="py-20 relative">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl sm:text-4xl font-extrabold mb-3">Featured <span class="gradient-text">Projects</span></h2>
                <div class="w-20 h-1.5 glow-btn mx-auto rounded-full"></div>
                <p class="text-slate-400 mt-4 text-sm sm:text-base">Full-stack applications built with robust backend architectures</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Project 01: NEXUSSTORE -->
                <div class="glass-card rounded-3xl p-6 sm:p-8 flex flex-col justify-between group">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="font-code text-pink-400 text-sm font-bold">01 / E-Commerce & AI</span>
                            <div class="w-10 h-10 rounded-xl bg-pink-500/10 flex items-center justify-center text-pink-500">
                                <i class="fa-solid fa-bag-shopping"></i>
                            </div>
                        </div>
                        <h3 class="text-2xl font-bold mb-3 group-hover:text-pink-400 transition-colors">NEXUSSTORE</h3>
                        <p class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
                            An AI-powered e-commerce platform. Users can browse products, manage cart and orders, and interact with an integrated <strong class="text-white">AI shopping assistant</strong> that helps discover products and answers inquiries instantly.
                        </p>
                        <!-- Tech Badges -->
                        <div class="flex flex-wrap gap-2 mb-8">
                            <span class="px-2.5 py-1 rounded-md bg-emerald-500/10 text-emerald-400 text-xs font-medium border border-emerald-500/20">MongoDB</span>
                            <span class="px-2.5 py-1 rounded-md bg-slate-800 text-slate-300 text-xs font-medium border border-slate-700">Express</span>
                            <span class="px-2.5 py-1 rounded-md bg-cyan-500/10 text-cyan-400 text-xs font-medium border border-cyan-500/20">React</span>
                            <span class="px-2.5 py-1 rounded-md bg-green-500/10 text-green-400 text-xs font-medium border border-green-500/20">Node.js</span>
                            <span class="px-2.5 py-1 rounded-md bg-pink-500/10 text-pink-400 text-xs font-medium border border-pink-500/20">AI Assistant</span>
                        </div>
                    </div>
                    <!-- Links -->
                    <div class="flex items-center space-x-4 pt-4 border-t border-slate-800">
                        <a href="https://github.com/raushank7460" target="_blank" class="flex-1 py-2.5 px-4 rounded-xl bg-slate-800 hover:bg-slate-700 text-center font-medium text-sm flex items-center justify-center space-x-2 transition-all">
                            <i class="fa-brands fa-github"></i>
                            <span>GitHub Code</span>
                        </a>
                        <a href="#" onclick="showNotification('Live demo link opening for NEXUSSTORE', 'info'); return false;" class="flex-1 py-2.5 px-4 rounded-xl glow-btn text-white text-center font-medium text-sm flex items-center justify-center space-x-2">
                            <i class="fa-solid fa-external-link-alt"></i>
                            <span>Live Demo</span>
                        </a>
                    </div>
                </div>

                <!-- Project 02: SpendFlow -->
                <div class="glass-card rounded-3xl p-6 sm:p-8 flex flex-col justify-between group">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="font-code text-pink-400 text-sm font-bold">02 / Finance & Tracking</span>
                            <div class="w-10 h-10 rounded-xl bg-orange-500/10 flex items-center justify-center text-orange-400">
                                <i class="fa-solid fa-wallet"></i>
                            </div>
                        </div>
                        <h3 class="text-2xl font-bold mb-3 group-hover:text-pink-400 transition-colors">SpendFlow</h3>
                        <p class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
                            A comprehensive expense management app designed to track income and expenses, categorize spending habits, and view clear financial summaries of where money goes.
                        </p>
                        <!-- Tech Badges -->
                        <div class="flex flex-wrap gap-2 mb-8">
                            <span class="px-2.5 py-1 rounded-md bg-emerald-500/10 text-emerald-400 text-xs font-medium border border-emerald-500/20">MongoDB</span>
                            <span class="px-2.5 py-1 rounded-md bg-slate-800 text-slate-300 text-xs font-medium border border-slate-700">Express</span>
                            <span class="px-2.5 py-1 rounded-md bg-cyan-500/10 text-cyan-400 text-xs font-medium border border-cyan-500/20">React</span>
                            <span class="px-2.5 py-1 rounded-md bg-green-500/10 text-green-400 text-xs font-medium border border-green-500/20">Node.js</span>
                        </div>
                    </div>
                    <!-- Links -->
                    <div class="flex items-center space-x-4 pt-4 border-t border-slate-800">
                        <a href="https://github.com/raushank7460" target="_blank" class="flex-1 py-2.5 px-4 rounded-xl bg-slate-800 hover:bg-slate-700 text-center font-medium text-sm flex items-center justify-center space-x-2 transition-all">
                            <i class="fa-brands fa-github"></i>
                            <span>GitHub Code</span>
                        </a>
                        <a href="#" onclick="showNotification('Live demo link opening for SpendFlow', 'info'); return false;" class="flex-1 py-2.5 px-4 rounded-xl glow-btn text-white text-center font-medium text-sm flex items-center justify-center space-x-2">
                            <i class="fa-solid fa-external-link-alt"></i>
                            <span>Live Demo</span>
                        </a>
                    </div>
                </div>

                <!-- Project 03: EquiBalance -->
                <div class="glass-card rounded-3xl p-6 sm:p-8 flex flex-col justify-between group">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="font-code text-pink-400 text-sm font-bold">03 / Split Management</span>
                            <div class="w-10 h-10 rounded-xl bg-purple-500/10 flex items-center justify-center text-purple-400">
                                <i class="fa-solid fa-scale-balanced"></i>
                            </div>
                        </div>
                        <h3 class="text-2xl font-bold mb-3 group-hover:text-pink-400 transition-colors">EquiBalance</h3>
                        <p class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
                            A balance and split management application built to handle shared expenses among multiple participants, track debts, and keep every account seamlessly settled.
                        </p>
                        <!-- Tech Badges -->
                        <div class="flex flex-wrap gap-2 mb-8">
                            <span class="px-2.5 py-1 rounded-md bg-emerald-500/10 text-emerald-400 text-xs font-medium border border-emerald-500/20">MongoDB</span>
                            <span class="px-2.5 py-1 rounded-md bg-slate-800 text-slate-300 text-xs font-medium border border-slate-700">Express</span>
                            <span class="px-2.5 py-1 rounded-md bg-cyan-500/10 text-cyan-400 text-xs font-medium border border-cyan-500/20">React</span>
                            <span class="px-2.5 py-1 rounded-md bg-green-500/10 text-green-400 text-xs font-medium border border-green-500/20">Node.js</span>
                        </div>
                    </div>
                    <!-- Links -->
                    <div class="flex items-center space-x-4 pt-4 border-t border-slate-800">
                        <a href="https://github.com/raushank7460" target="_blank" class="flex-1 py-2.5 px-4 rounded-xl bg-slate-800 hover:bg-slate-700 text-center font-medium text-sm flex items-center justify-center space-x-2 transition-all">
                            <i class="fa-brands fa-github"></i>
                            <span>GitHub Code</span>
                        </a>
                        <a href="#" onclick="showNotification('Live demo link opening for EquiBalance', 'info'); return false;" class="flex-1 py-2.5 px-4 rounded-xl glow-btn text-white text-center font-medium text-sm flex items-center justify-center space-x-2">
                            <i class="fa-solid fa-external-link-alt"></i>
                            <span>Live Demo</span>
                        </a>
                    </div>
                </div>

                <!-- Project 04: TaskFlow -->
                <div class="glass-card rounded-3xl p-6 sm:p-8 flex flex-col justify-between group">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="font-code text-pink-400 text-sm font-bold">04 / Productivity & Tasks</span>
                            <div class="w-10 h-10 rounded-xl bg-blue-500/10 flex items-center justify-center text-blue-400">
                                <i class="fa-solid fa-list-check"></i>
                            </div>
                        </div>
                        <h3 class="text-2xl font-bold mb-3 group-hover:text-pink-400 transition-colors">TaskFlow</h3>
                        <p class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
                            An efficient task management application empowering users to create, organize, prioritize, and track tasks with secure JWT authentication and user-specific data isolation.
                        </p>
                        <!-- Tech Badges -->
                        <div class="flex flex-wrap gap-2 mb-8">
                            <span class="px-2.5 py-1 rounded-md bg-emerald-500/10 text-emerald-400 text-xs font-medium border border-emerald-500/20">MongoDB</span>
                            <span class="px-2.5 py-1 rounded-md bg-slate-800 text-slate-300 text-xs font-medium border border-slate-700">Express</span>
                            <span class="px-2.5 py-1 rounded-md bg-cyan-500/10 text-cyan-400 text-xs font-medium border border-cyan-500/20">React</span>
                            <span class="px-2.5 py-1 rounded-md bg-green-500/10 text-green-400 text-xs font-medium border border-green-500/20">Node.js</span>
                        </div>
                    </div>
                    <!-- Links -->
                    <div class="flex items-center space-x-4 pt-4 border-t border-slate-800">
                        <a href="https://github.com/raushank7460" target="_blank" class="flex-1 py-2.5 px-4 rounded-xl bg-slate-800 hover:bg-slate-700 text-center font-medium text-sm flex items-center justify-center space-x-2 transition-all">
                            <i class="fa-brands fa-github"></i>
                            <span>GitHub Code</span>
                        </a>
                        <a href="#" onclick="showNotification('Live demo link opening for TaskFlow', 'info'); return false;" class="flex-1 py-2.5 px-4 rounded-xl glow-btn text-white text-center font-medium text-sm flex items-center justify-center space-x-2">
                            <i class="fa-solid fa-external-link-alt"></i>
                            <span>Live Demo</span>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="w-full h-px bg-gradient-to-r from-transparent via-pink-500/50 to-transparent my-10"></div>

    <!-- Contact & Connect Section -->
    <section id="contact" class="py-20 relative">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl sm:text-4xl font-extrabold mb-3">Let's <span class="gradient-text">Connect</span></h2>
                <div class="w-20 h-1.5 glow-btn mx-auto rounded-full"></div>
                <p class="text-slate-400 mt-4 text-sm sm:text-base">Open to SDE / Backend Developer opportunities. Drop me a message!</p>
            </div>

            <div class="glass-card rounded-3xl p-8 sm:p-12 relative overflow-hidden">
                <div class="absolute -bottom-10 -right-10 w-60 h-60 bg-pink-500/10 rounded-full blur-3xl pointer-events-none"></div>
                
                <form id="contact-form" onsubmit="handleContactSubmit(event)" class="space-y-6 relative z-10">
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                        <div>
                            <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-2">Your Name</label>
                            <input type="text" id="sender-name" required placeholder="John Doe" class="w-full px-4 py-3 rounded-xl bg-slate-900/80 border border-slate-700 focus:border-pink-500 focus:outline-none text-slate-200 text-sm transition-colors">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-2">Your Email</label>
                            <input type="email" id="sender-email" required placeholder="john@example.com" class="w-full px-4 py-3 rounded-xl bg-slate-900/80 border border-slate-700 focus:border-pink-500 focus:outline-none text-slate-200 text-sm transition-colors">
                        </div>
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-2">Message</label>
                        <textarea id="sender-message" rows="5" required placeholder="Hello Raushan, I have an SDE opportunity for you..." class="w-full px-4 py-3 rounded-xl bg-slate-900/80 border border-slate-700 focus:border-pink-500 focus:outline-none text-slate-200 text-sm transition-colors"></textarea>
                    </div>
                    <div class="flex items-center justify-between flex-wrap gap-4">
                        <div class="text-xs text-slate-400 flex items-center space-x-2">
                            <i class="fa-solid fa-envelope text-pink-500"></i>
                            <span>Direct: <a href="mailto:raushank7460@gmail.com" class="text-pink-400 hover:underline">raushank7460@gmail.com</a></span>
                        </div>
                        <button type="submit" class="px-8 py-3.5 rounded-xl glow-btn text-white font-semibold text-sm flex items-center space-x-2 shadow-lg">
                            <i class="fa-solid fa-paper-plane"></i>
                            <span>Send Message</span>
                        </button>
                    </div>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="border-t border-slate-800 py-12 bg-slate-950/60 text-center">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-center space-x-4 mb-6">
                <a href="https://www.linkedin.com/in/raushan-kumar-449969421" target="_blank" class="w-10 h-10 rounded-xl glass-card flex items-center justify-center text-slate-300 hover:text-pink-500 transition-colors">
                    <i class="fa-brands fa-linkedin text-lg"></i>
                </a>
                <a href="https://leetcode.com/u/raushanx05/" target="_blank" class="w-10 h-10 rounded-xl glass-card flex items-center justify-center text-slate-300 hover:text-pink-500 transition-colors">
                    <i class="fa-solid fa-code text-lg"></i>
                </a>
                <a href="mailto:raushank7460@gmail.com" class="w-10 h-10 rounded-xl glass-card flex items-center justify-center text-slate-300 hover:text-pink-500 transition-colors">
                    <i class="fa-solid fa-envelope text-lg"></i>
                </a>
            </div>
            <p class="text-slate-400 text-sm mb-2">Designed & Built with ❤️ by <strong class="text-white">Raushan Kumar</strong></p>
            <p class="text-xs text-slate-600">B.Tech CSE • GLA University (2027) • Backend Focused MERN Developer</p>
        </div>
    </footer>

    <!-- Script Logic -->
    <script>
        // Mobile Menu Toggle
        const menuBtn = document.getElementById('menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Close mobile menu on clicking links
        mobileMenu.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Typing Effect
        const words = [
            "Building full-stack apps with MERN 🚀",
            "REST APIs | JWT Auth | MongoDB 🔥",
            "400+ DSA problems solved 💪",
            "Open to SDE / Backend roles ✨"
        ];
        let i = 0;
        let timer;

        function typingEffect() {
            let word = words[i].split("");
            var loopTyping = function() {
                if (word.length > 0) {
                    document.getElementById('typing-text').innerHTML += word.shift();
                } else {
                    setTimeout(deletingEffect, 2000);
                    return false;
                }
                timer = setTimeout(loopTyping, 80);
            };
            loopTyping();
        }

        function deletingEffect() {
            let word = words[i].split("");
            var loopDeleting = function() {
                if (word.length > 0) {
                    word.pop();
                    document.getElementById('typing-text').innerHTML = word.join("");
                } else {
                    if (words.length > (i + 1)) {
                        i++;
                    } else {
                        i = 0;
                    }
                    setTimeout(typingEffect, 500);
                    return false;
                }
                timer = setTimeout(loopDeleting, 40);
            };
            loopDeleting();
        }

        typingEffect();

        // Notification Toast System
        function showNotification(message, type = 'success') {
            const toast = document.getElementById('toast');
            const title = document.getElementById('toast-title');
            const msg = document.getElementById('toast-message');
            const icon = document.getElementById('toast-icon');

            msg.textContent = message;
            if (type === 'success') {
                title.textContent = 'Success!';
                icon.className = 'fa-solid fa-circle-check text-pink-500 text-xl';
            } else {
                title.textContent = 'Info';
                icon.className = 'fa-solid fa-circle-info text-cyan-400 text-xl';
            }

            toast.classList.remove('translate-y-20', 'opacity-0');
            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 3500);
        }

        // Contact Form Submission Handler
        function handleContactSubmit(event) {
            event.preventDefault();
            const name = document.getElementById('sender-name').value;
            const email = document.getElementById('sender-email').value;
            const message = document.getElementById('sender-message').value;

            // Open mail client or simulate success
            window.location.href = `mailto:raushank7460@gmail.com?subject=Contact from ${encodeURIComponent(name)} (${encodeURIComponent(email)})&body=${encodeURIComponent(message)}`;
            
            showNotification('Opening your mail client to send message!', 'success');
            document.getElementById('contact-form').reset();
        }
    </script>
</body>
</html>
