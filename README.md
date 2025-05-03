1st webpage code:-
------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ResuCraftify - AI-Powered Resume Builder</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            overflow-x: hidden;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #6e8efb 0%, #4a6cf7 100%);
        }
        
        .floating {
            animation: floating 3s ease-in-out infinite;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(74, 108, 247, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(74, 108, 247, 0); }
            100% { box-shadow: 0 0 0 0 rgba(74, 108, 247, 0); }
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .feature-card {
            transition: all 0.3s ease;
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: #4a6cf7;
            transition: width 0.3s ease;
        }
        
        .nav-link:hover:after {
            width: 100%;
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Header/Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-sm">
        <div class="container mx-auto px-6 py-4">
            <div class="flex items-center justify-between">
                <!-- Logo -->
                <div class="flex items-center">
                    <div class="w-10 h-10 rounded-full gradient-bg flex items-center justify-center text-white font-bold text-xl mr-3">
                        RC
                    </div>
                    <span class="text-2xl font-bold text-gray-800">Resu<span class="text-blue-600">Craftify</span></span>
                </div>
                
                <!-- Desktop Navigation -->
                <nav class="hidden md:flex space-x-8">
                    <a href="#" class="nav-link text-gray-700 font-medium hover:text-blue-600">Home</a>
                    <a href="#" class="nav-link text-gray-700 font-medium hover:text-blue-600">About</a>
                    <a href="#" class="nav-link text-gray-700 font-medium hover:text-blue-600">Documents</a>
                    <a href="#" class="nav-link text-gray-700 font-medium hover:text-blue-600">Team</a>
                    <a href="#" class="nav-link text-gray-700 font-medium hover:text-blue-600">Blog</a>
                </nav>
                
                <!-- Login Button -->
                <div class="hidden md:block">
                    <a href="#" class="px-6 py-2 rounded-full border border-blue-600 text-blue-600 font-medium hover:bg-blue-600 hover:text-white transition duration-300">
                        Login
                    </a>
                </div>
                
                <!-- Mobile Menu Button -->
                <button class="md:hidden focus:outline-none" id="mobile-menu-button">
                    <svg class="w-6 h-6 text-gray-700" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
            </div>
            
            <!-- Mobile Menu -->
            <div class="md:hidden hidden mt-4" id="mobile-menu">
                <div class="flex flex-col space-y-3">
                    <a href="#" class="block px-3 py-2 rounded-md text-gray-700 font-medium hover:bg-blue-50 hover:text-blue-600">Home</a>
                    <a href="#" class="block px-3 py-2 rounded-md text-gray-700 font-medium hover:bg-blue-50 hover:text-blue-600">About</a>
                    <a href="#" class="block px-3 py-2 rounded-md text-gray-700 font-medium hover:bg-blue-50 hover:text-blue-600">Documents</a>
                    <a href="#" class="block px-3 py-2 rounded-md text-gray-700 font-medium hover:bg-blue-50 hover:text-blue-600">Team</a>
                    <a href="#" class="block px-3 py-2 rounded-md text-gray-700 font-medium hover:bg-blue-50 hover:text-blue-600">Blog</a>
                    <a href="#" class="block px-3 py-2 rounded-md text-blue-600 font-medium hover:bg-blue-50">Login</a>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="gradient-bg text-white">
        <div class="container mx-auto px-6 py-20 md:py-32">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-12 md:mb-0">
                    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
                        Create the Perfect Resume in Minutes
                    </h1>
                    <p class="text-xl md:text-2xl text-blue-100 mb-8">
                        AI-powered resume builder that helps you stand out from the crowd and land your dream job.
                    </p>
                    <div class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4">
                        <button class="px-8 py-4 bg-white text-blue-600 font-bold rounded-full hover:bg-gray-100 transition duration-300 pulse">
                            Create Resume <i class="fas fa-arrow-right ml-2"></i>
                        </button>
                        <button class="px-8 py-4 border border-white text-white font-bold rounded-full hover:bg-white hover:bg-opacity-10 transition duration-300">
                            Watch Demo <i class="fas fa-play-circle ml-2"></i>
                        </button>
                    </div>
                    <div class="mt-8 flex items-center">
                        <div class="flex -space-x-2">
                            <img src="https://randomuser.me/api/portraits/women/12.jpg" class="w-10 h-10 rounded-full border-2 border-white">
                            <img src="https://randomuser.me/api/portraits/men/32.jpg" class="w-10 h-10 rounded-full border-2 border-white">
                            <img src="https://randomuser.me/api/portraits/women/45.jpg" class="w-10 h-10 rounded-full border-2 border-white">
                        </div>
                        <div class="ml-4">
                            <p class="text-blue-100">Trusted by <span class="font-bold">10,000+</span> professionals</p>
                        </div>
                    </div>
                </div>
                <div class="md:w-1/2 flex justify-center">
                    <div class="relative">
                        <img src="https://resumaker.ai/wp-content/uploads/2023/03/resume-example-1.png" alt="Resume Example" class="rounded-lg shadow-2xl w-full max-w-md floating">
                        <div class="absolute -bottom-6 -left-6 bg-white p-4 rounded-lg shadow-lg hidden md:block">
                            <div class="flex items-center">
                                <div class="w-10 h-10 rounded-full bg-blue-100 flex items-center justify-center text-blue-600 mr-3">
                                    <i class="fas fa-magic"></i>
                                </div>
                                <div>
                                    <p class="text-sm font-medium text-gray-800">AI-Powered</p>
                                    <p class="text-xs text-gray-500">Smart suggestions</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="py-20 bg-white">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">Why Choose ResuCraftify?</h2>
                <p class="text-lg text-gray-600 max-w-2xl mx-auto">
                    Our platform combines cutting-edge AI technology with professional resume design to help you create the perfect resume.
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Feature 1 -->
                <div class="feature-card bg-white p-8 rounded-xl shadow-md border border-gray-100">
                    <div class="w-14 h-14 gradient-bg rounded-lg flex items-center justify-center text-white mb-6">
                        <i class="fas fa-robot text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">AI-Powered Suggestions</h3>
                    <p class="text-gray-600">
                        Get real-time suggestions to improve your resume content based on your target job and industry standards.
                    </p>
                </div>
                
                <!-- Feature 2 -->
                <div class="feature-card bg-white p-8 rounded-xl shadow-md border border-gray-100">
                    <div class="w-14 h-14 gradient-bg rounded-lg flex items-center justify-center text-white mb-6">
                        <i class="fas fa-palette text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Professional Templates</h3>
                    <p class="text-gray-600">
                        Choose from dozens of professionally designed templates that are ATS-friendly and visually appealing.
                    </p>
                </div>
                
                <!-- Feature 3 -->
                <div class="feature-card bg-white p-8 rounded-xl shadow-md border border-gray-100">
                    <div class="w-14 h-14 gradient-bg rounded-lg flex items-center justify-center text-white mb-6">
                        <i class="fas fa-file-alt text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Multiple Formats</h3>
                    <p class="text-gray-600">
                        Download your resume in PDF, Word, or plain text format with just one click.
                    </p>
                </div>
                
                <!-- Feature 4 -->
                <div class="feature-card bg-white p-8 rounded-xl shadow-md border border-gray-100">
                    <div class="w-14 h-14 gradient-bg rounded-lg flex items-center justify-center text-white mb-6">
                        <i class="fas fa-chart-line text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Performance Tracking</h3>
                    <p class="text-gray-600">
                        Track how your resume performs with recruiters and get insights to make it even better.
                    </p>
                </div>
                
                <!-- Feature 5 -->
                <div class="feature-card bg-white p-8 rounded-xl shadow-md border border-gray-100">
                    <div class="w-14 h-14 gradient-bg rounded-lg flex items-center justify-center text-white mb-6">
                        <i class="fas fa-user-edit text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Easy Customization</h3>
                    <p class="text-gray-600">
                        Drag-and-drop editor makes it simple to customize every aspect of your resume.
                    </p>
                </div>
                
                <!-- Feature 6 -->
                <div class="feature-card bg-white p-8 rounded-xl shadow-md border border-gray-100">
                    <div class="w-14 h-14 gradient-bg rounded-lg flex items-center justify-center text-white mb-6">
                        <i class="fas fa-lock text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Secure Storage</h3>
                    <p class="text-gray-600">
                        Your data is securely stored in the cloud so you can access and update your resume anytime.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-20 bg-gray-50">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">Success Stories</h2>
                <p class="text-lg text-gray-600 max-w-2xl mx-auto">
                    Hear from professionals who landed their dream jobs with ResuCraftify.
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Testimonial 1 -->
                <div class="bg-white p-8 rounded-xl shadow-sm border border-gray-100">
                    <div class="flex items-center mb-6">
                        <img src="https://randomuser.me/api/portraits/women/32.jpg" class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold text-gray-800">Sarah Johnson</h4>
                            <p class="text-sm text-gray-500">Product Manager at Google</p>
                        </div>
                    </div>
                    <p class="text-gray-600 mb-4">
                        "ResuCraftify helped me craft a resume that stood out from hundreds of applicants. The AI suggestions were incredibly helpful in highlighting my most relevant experience."
                    </p>
                    <div class="flex text-yellow-400">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                </div>
                
                <!-- Testimonial 2 -->
                <div class="bg-white p-8 rounded-xl shadow-sm border border-gray-100">
                    <div class="flex items-center mb-6">
                        <img src="https://randomuser.me/api/portraits/men/45.jpg" class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold text-gray-800">Michael Chen</h4>
                            <p class="text-sm text-gray-500">Software Engineer at Facebook</p>
                        </div>
                    </div>
                    <p class="text-gray-600 mb-4">
                        "As a developer, I never knew how to properly format my resume. ResuCraftify's templates and guidance helped me create a professional-looking resume in under 30 minutes."
                    </p>
                    <div class="flex text-yellow-400">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                </div>
                
                <!-- Testimonial 3 -->
                <div class="bg-white p-8 rounded-xl shadow-sm border border-gray-100">
                    <div class="flex items-center mb-6">
                        <img src="https://randomuser.me/api/portraits/women/68.jpg" class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold text-gray-800">Emily Rodriguez</h4>
                            <p class="text-sm text-gray-500">Marketing Director at Airbnb</p>
                        </div>
                    </div>
                    <p class="text-gray-600 mb-4">
                        "The AI-powered content suggestions were game-changing. It helped me quantify my achievements in a way that resonated with recruiters. Got 3 interview requests within a week!"
                    </p>
                    <div class="flex text-yellow-400">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="py-20 gradient-bg text-white">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-3xl md:text-4xl font-bold mb-6">Ready to Craft Your Perfect Resume?</h2>
            <p class="text-xl text-blue-100 max-w-2xl mx-auto mb-8">
                Join thousands of professionals who have accelerated their job search with ResuCraftify.
            </p>
            <button class="px-10 py-4 bg-white text-blue-600 font-bold rounded-full hover:bg-gray-100 transition duration-300 mb-8 pulse">
                Get Started Now <i class="fas fa-arrow-right ml-2"></i>
            </button>
            <p class="text-blue-100">
                No credit card required. Free plan available.
            </p>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="container mx-auto px-6">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <!-- Column 1 -->
                <div>
                    <div class="flex items-center mb-4">
                        <div class="w-10 h-10 rounded-full gradient-bg flex items-center justify-center text-white font-bold text-xl mr-3">
                            RC
                        </div>
                        <span class="text-xl font-bold">Resu<span class="text-blue-400">Craftify</span></span>
                    </div>
                    <p class="text-gray-400 mb-4">
                        AI-powered resume builder to help you land your dream job.
                    </p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i class="fab fa-instagram"></i>
                        </a>
                    </div>
                </div>
                
                <!-- Column 2 -->
                <div>
                    <h4 class="text-lg font-bold mb-4">Product</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Features</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Pricing</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Templates</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Integrations</a></li>
                    </ul>
                </div>
                
                <!-- Column 3 -->
                <div>
                    <h4 class="text-lg font-bold mb-4">Resources</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Blog</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Help Center</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Resume Guide</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Career Advice</a></li>
                    </ul>
                </div>
                
                <!-- Column 4 -->
                <div>
                    <h4 class="text-lg font-bold mb-4">Company</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">About Us</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Careers</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Contact</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Press</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-400 mb-4 md:mb-0">
                    © 2023 ResuCraftify. All rights reserved.
                </p>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a>
                    <a href="#" class="text-gray-400 hover:text-white">Terms of Service</a>
                    <a href="#" class="text-gray-400 hover:text-white">Cookies</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.getElementById('mobile-menu-button').addEventListener('click', function() {
            const menu = document.getElementById('mobile-menu');
            if (menu.classList.contains('hidden')) {
                menu.classList.remove('hidden');
            } else {
                menu.classList.add('hidden');
            }
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    targetElement.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Animation on scroll
        function animateOnScroll() {
            const elements = document.querySelectorAll('.feature-card, .floating');
            
            elements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const screenPosition = window.innerHeight / 1.3;
                
                if (elementPosition < screenPosition) {
                    element.classList.add('animate__animated', 'animate__fadeInUp');
                }
            });
        }
        
        window.addEventListener('scroll', animateOnScroll);
        window.addEventListener('load', animateOnScroll);
    </script>
</body>
</html>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

2nd webpage code:-
------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login | ResuCraftify</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f8fafc;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #6e8efb 0%, #4a6cf7 100%);
        }
        
        .login-container {
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
        }
        
        .input-field {
            transition: all 0.3s ease;
            border: 1px solid #e2e8f0;
        }
        
        .input-field:focus {
            border-color: #4a6cf7;
            box-shadow: 0 0 0 3px rgba(74, 108, 247, 0.2);
        }
        
        .social-btn {
            transition: all 0.3s ease;
        }
        
        .social-btn:hover {
            transform: translateY(-2px);
        }
        
        .divider {
            display: flex;
            align-items: center;
            text-align: center;
            color: #94a3b8;
        }
        
        .divider::before, .divider::after {
            content: "";
            flex: 1;
            border-bottom: 1px solid #e2e8f0;
        }
        
        .divider::before {
            margin-right: 1rem;
        }
        
        .divider::after {
            margin-left: 1rem;
        }
    </style>
</head>
<body class="min-h-screen flex items-center justify-center p-4">
    <div class="login-container bg-white rounded-xl w-full max-w-md overflow-hidden">
        <!-- Header -->
        <div class="gradient-bg py-6 px-8 text-center">
            <div class="flex items-center justify-center mb-4">
                <div class="w-10 h-10 rounded-full bg-white flex items-center justify-center text-blue-600 font-bold text-xl mr-3">
                    RC
                </div>
                <span class="text-2xl font-bold text-white">Resu<span class="text-blue-100">Craftify</span></span>
            </div>
            <h1 class="text-2xl font-bold text-white">Welcome Back</h1>
            <p class="text-blue-100 mt-1">Sign in to continue to your account</p>
        </div>
        
        <!-- Login Form -->
        <div class="px-8 py-8">
            <!-- Social Login Buttons -->
            <div class="flex space-x-4 mb-6">
                <button class="social-btn flex-1 flex items-center justify-center py-2 px-4 border border-gray-200 rounded-lg hover:bg-gray-50">
                    <i class="fab fa-google text-red-500 mr-2"></i>
                    <span class="text-sm font-medium text-gray-700">Google</span>
                </button>
                <button class="social-btn flex-1 flex items-center justify-center py-2 px-4 border border-gray-200 rounded-lg hover:bg-gray-50">
                    <i class="fab fa-facebook-f text-blue-600 mr-2"></i>
                    <span class="text-sm font-medium text-gray-700">Facebook</span>
                </button>
            </div>
            
            <!-- Divider -->
            <div class="divider text-sm my-6">OR</div>
            
            <!-- Email/Password Form -->
            <form>
                <div class="mb-4">
                    <label for="email" class="block text-sm font-medium text-gray-700 mb-1">Email Address</label>
                    <div class="relative">
                        <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
                            <i class="fas fa-envelope text-gray-400"></i>
                        </div>
                        <input 
                            type="email" 
                            id="email" 
                            class="input-field w-full pl-10 pr-3 py-3 rounded-lg focus:outline-none" 
                            placeholder="you@example.com"
                            required
                        >
                    </div>
                </div>
                
                <div class="mb-4">
                    <label for="password" class="block text-sm font-medium text-gray-700 mb-1">Password</label>
                    <div class="relative">
                        <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
                            <i class="fas fa-lock text-gray-400"></i>
                        </div>
                        <input 
                            type="password" 
                            id="password" 
                            class="input-field w-full pl-10 pr-3 py-3 rounded-lg focus:outline-none" 
                            placeholder="••••••••"
                            required
                        >
                        <button type="button" class="absolute right-3 top-3 text-gray-400 hover:text-gray-600">
                            <i class="fas fa-eye"></i>
                        </button>
                    </div>
                </div>
                
                <div class="flex items-center justify-between mb-6">
                    <div class="flex items-center">
                        <input 
                            type="checkbox" 
                            id="remember" 
                            class="h-4 w-4 text-blue-600 focus:ring-blue-500 border-gray-300 rounded"
                        >
                        <label for="remember" class="ml-2 block text-sm text-gray-700">Stay signed in</label>
                    </div>
                    <a href="#" class="text-sm text-blue-600 hover:text-blue-500 font-medium">Forgot password?</a>
                </div>
                
                <button 
                    type="submit" 
                    class="gradient-bg w-full py-3 px-4 rounded-lg text-white font-medium hover:opacity-90 transition duration-300 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2"
                >
                    Sign In
                </button>
            </form>
            
            <div class="mt-6 text-center">
                <p class="text-sm text-gray-600">
                    Don't have an account? 
                    <a href="#" class="text-blue-600 hover:text-blue-500 font-medium">Sign up</a>
                </p>
            </div>
        </div>
    </div>

    <script>
        // Toggle password visibility
        document.querySelector('button[aria-label="toggle password visibility"]').addEventListener('click', function() {
            const passwordInput = document.getElementById('password');
            const icon = this.querySelector('i');
            
            if (passwordInput.type === 'password') {
                passwordInput.type = 'text';
                icon.classList.remove('fa-eye');
                icon.classList.add('fa-eye-slash');
            } else {
                passwordInput.type = 'password';
                icon.classList.remove('fa-eye
</html>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

3rd webpage code:-
------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About | ResuCraftify</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f8fafc;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #6e8efb 0%, #4a6cf7 100%);
        }
        
        .section-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .section-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 12px;
            margin-bottom: 1.5rem;
        }
        
        .tech-badge {
            display: inline-flex;
            align-items: center;
            padding: 0.35rem 0.8rem;
            border-radius: 9999px;
            font-size: 0.85rem;
            margin-right: 0.5rem;
            margin-bottom: 0.5rem;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="bg-white shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <div class="flex-shrink-0 flex items-center">
                        <div class="w-10 h-10 rounded-full gradient-bg flex items-center justify-center text-white font-bold text-xl mr-3">
                            RC
                        </div>
                        <span class="text-xl font-bold text-gray-800">Resu<span class="text-blue-600">Craftify</span></span>
                    </div>
                </div>
                <div class="hidden md:ml-6 md:flex md:items-center md:space-x-8">
                    <a href="#" class="text-gray-500 hover:text-gray-700 px-3 py-2 text-sm font-medium">Home</a>
                    <a href="#" class="text-blue-600 border-b-2 border-blue-600 px-3 py-2 text-sm font-medium">About</a>
                    <a href="#" class="text-gray-500 hover:text-gray-700 px-3 py-2 text-sm font-medium">Features</a>
                    <a href="#" class="text-gray-500 hover:text-gray-700 px-3 py-2 text-sm font-medium">Contact</a>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <div class="gradient-bg text-white py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <h1 class="text-4xl font-bold mb-4">About ResuCraftify</h1>
                <p class="text-xl text-blue-100 max-w-3xl mx-auto">
                    Revolutionizing resume building with AI-powered tools to help you craft the perfect resume for your dream job.
                </p>
            </div>
        </div>
    </div>

    <!-- Main Content -->
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
        <!-- Project Purpose -->
        <div class="section-card bg-white rounded-xl shadow-sm p-8 mb-12">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pr-8">
                    <img src="https://images.unsplash.com/photo-1579389083078-4e7018379f7e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                         alt="AI Resume Building" 
                         class="rounded-lg shadow-md w-full h-auto">
                </div>
                <div class="md:w-1/2">
                    <div class="feature-icon gradient-bg text-white">
                        <i class="fas fa-bullseye text-2xl"></i>
                    </div>
                    <h2 class="text-2xl font-bold text-gray-800 mb-4">Project Purpose</h2>
                    <p class="text-gray-600 mb-4">
                        ResuCraftify was born from the recognition that job seekers often struggle to create resumes that effectively showcase their skills and experience. Traditional resume builders offer templates but lack intelligent guidance.
                    </p>
                    <p class="text-gray-600">
                        Our mission is to leverage artificial intelligence to analyze job descriptions, suggest optimal content organization, and provide real-time feedback to help users create resumes that stand out to both human recruiters and applicant tracking systems.
                    </p>
                </div>
            </div>
        </div>

        <!-- Key Features -->
        <div class="mb-12">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-12">Key Features</h2>
            <div class="grid md:grid-cols-3 gap-8">
                <!-- Feature 1 -->
                <div class="section-card bg-white rounded-xl shadow-sm p-8 text-center">
                    <div class="feature-icon gradient-bg text-white mx-auto">
                        <i class="fas fa-robot text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">AI-Powered Suggestions</h3>
                    <p class="text-gray-600">
                        Our AI analyzes your input and suggests powerful action verbs, quantifiable achievements, and industry-specific keywords to strengthen your resume.
                    </p>
                </div>
                
                <!-- Feature 2 -->
                <div class="section-card bg-white rounded-xl shadow-sm p-8 text-center">
                    <div class="feature-icon gradient-bg text-white mx-auto">
                        <i class="fas fa-file-alt text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">ATS Optimization</h3>
                    <p class="text-gray-600">
                        Automatically formats your resume to pass through Applicant Tracking Systems while maintaining a visually appealing design for human reviewers.
                    </p>
                </div>
                
                <!-- Feature 3 -->
                <div class="section-card bg-white rounded-xl shadow-sm p-8 text-center">
                    <div class="feature-icon gradient-bg text-white mx-auto">
                        <i class="fas fa-chart-line text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Performance Analytics</h3>
                    <p class="text-gray-600">
                        Get instant feedback on your resume's strength with our scoring system that evaluates content, structure, and keyword optimization.
                    </p>
                </div>
            </div>
        </div>

        <!-- Technical Implementation -->
        <div class="section-card bg-white rounded-xl shadow-sm p-8 mb-12">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0">
                    <div class="feature-icon gradient-bg text-white">
                        <i class="fas fa-code text-2xl"></i>
                    </div>
                    <h2 class="text-2xl font-bold text-gray-800 mb-4">Technical Implementation</h2>
                    <p class="text-gray-600 mb-6">
                        ResuCraftify combines modern web technologies with advanced natural language processing to deliver a seamless user experience.
                    </p>
                    
                    <div class="mb-6">
                        <h3 class="text-lg font-semibold text-gray-800 mb-3">Technologies Used</h3>
                        <div>
                            <span class="tech-badge bg-blue-100 text-blue-800"><i class="fab fa-react mr-1"></i> React</span>
                            <span class="tech-badge bg-green-100 text-green-800"><i class="fab fa-node-js mr-1"></i> Node.js</span>
                            <span class="tech-badge bg-yellow-100 text-yellow-800"><i class="fab fa-js mr-1"></i> JavaScript</span>
                            <span class="tech-badge bg-purple-100 text-purple-800"><i class="fas fa-database mr-1"></i> MongoDB</span>
                            <span class="tech-badge bg-red-100 text-red-800"><i class="fas fa-brain mr-1"></i> TensorFlow.js</span>
                            <span class="tech-badge bg-indigo-100 text-indigo-800"><i class="fab fa-python mr-1"></i> Python NLP</span>
                        </div>
                    </div>
                </div>
                <div class="md:w-1/2 md:pl-8">
                    <img src="https://images.unsplash.com/photo-1558494949-ef010cbdcc31?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                         alt="Code development" 
                         class="rounded-lg shadow-md w-full h-auto">
                </div>
            </div>
        </div>

        <!-- Learning Outcomes -->
        <div class="section-card bg-white rounded-xl shadow-sm p-8 mb-12">
            <h2 class="text-2xl font-bold text-gray-800 mb-6">Learning Outcomes</h2>
            <div class="grid md:grid-cols-2 gap-6">
                <div class="flex items-start">
                    <div class="gradient-bg text-white p-3 rounded-lg mr-4">
                        <i class="fas fa-lightbulb"></i>
                    </div>
                    <div>
                        <h3 class="text-lg font-semibold text-gray-800 mb-2">Natural Language Processing</h3>
                        <p class="text-gray-600">
                            Gained practical experience implementing NLP techniques for text analysis, keyword extraction, and content optimization.
                        </p>
                    </div>
                </div>
                <div class="flex items-start">
                    <div class="gradient-bg text-white p-3 rounded-lg mr-4">
                        <i class="fas fa-users"></i>
                    </div>
                    <div>
                        <h3 class="text-lg font-semibold text-gray-800 mb-2">User-Centric Design</h3>
                        <p class="text-gray-600">
                            Learned to balance complex technical functionality with intuitive UI/UX design principles.
                        </p>
                    </div>
                </div>
                <div class="flex items-start">
                    <div class="gradient-bg text-white p-3 rounded-lg mr-4">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <div>
                        <h3 class="text-lg font-semibold text-gray-800 mb-2">Data Security</h3>
                        <p class="text-gray-600">
                            Implemented robust security measures to protect sensitive user data while maintaining system performance.
                        </p>
                    </div>
                </div>
                <div class="flex items-start">
                    <div class="gradient-bg text-white p-3 rounded-lg mr-4">
                        <i class="fas fa-project-diagram"></i>
                    </div>
                    <div>
                        <h3 class="text-lg font-semibold text-gray-800 mb-2">System Architecture</h3>
                        <p class="text-gray-600">
                            Developed skills in designing scalable architecture that integrates multiple technologies seamlessly.
                        </p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Future Developments -->
        <div class="section-card bg-white rounded-xl shadow-sm p-8 mb-12">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pr-8">
                    <img src="https://images.unsplash.com/photo-1507679799987-c73779587ccf?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                         alt="Future planning" 
                         class="rounded-lg shadow-md w-full h-auto">
                </div>
                <div class="md:w-1/2">
                    <div class="feature-icon gradient-bg text-white">
                        <i class="fas fa-rocket text-2xl"></i>
                    </div>
                    <h2 class="text-2xl font-bold text-gray-800 mb-4">Future Developments</h2>
                    <ul class="space-y-3 text-gray-600">
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-blue-500 mt-1 mr-2"></i>
                            <span>Integration with LinkedIn for automated profile-to-resume conversion</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-blue-500 mt-1 mr-2"></i>
                            <span>Expanded industry-specific templates and keyword libraries</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-blue-500 mt-1 mr-2"></i>
                            <span>AI-powered interview preparation tools based on resume content</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-blue-500 mt-1 mr-2"></i>
                            <span>Collaborative editing features for career coaches and mentors</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-blue-500 mt-1 mr-2"></i>
                            <span>Mobile app with offline capabilities and camera-based document scanning</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Acknowledgments -->
        <div class="section-card bg-white rounded-xl shadow-sm p-8">
            <h2 class="text-2xl font-bold text-gray-800 mb-6">Acknowledgments</h2>
            <p class="text-gray-600 mb-6">
                ResuCraftify was made possible through the contributions of many individuals and the support of various open-source communities.
            </p>
            <div class="grid md:grid-cols-3 gap-6">
                <div class="bg-blue-50 p-6 rounded-lg">
                    <h3 class="font-semibold text-blue-800 mb-3">Open Source Libraries</h3>
                    <p class="text-gray-600 text-sm">
                        We're grateful for the developers behind React, TensorFlow.js, and the many other open-source projects that form our technological foundation.
                    </p>
                </div>
                <div class="bg-purple-50 p-6 rounded-lg">
                    <h3 class="font-semibold text-purple-800 mb-3">Design Resources</h3>
                    <p class="text-gray-600 text-sm">
                        Special thanks to Tailwind CSS, Font Awesome, and Unsplash for providing the design tools and assets that bring our interface to life.
                    </p>
                </div>
                <div class="bg-green-50 p-6 rounded-lg">
                    <h3 class="font-semibold text-green-800 mb-3">User Testers</h3>
                    <p class="text-gray-600 text-sm">
                        Our beta testers provided invaluable feedback that shaped the user experience and helped identify critical improvements.
                    </p>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-50 border-t border-gray-200 py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="flex items-center mb-4 md:mb-0">
                    <div class="w-10 h-10 rounded-full gradient-bg flex items-center justify-center text-white font-bold text-xl mr-3">
                        RC
                    </div>
                    <span class="text-lg font-bold text-gray-800">Resu<span class="text-blue-600">Craftify</span></span>
                </div>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-400 hover:text-gray-500">
                        <i class="fab fa-twitter"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-gray-500">
                        <i class="fab fa-github"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-gray-500">
                        <i class="fab fa-linkedin"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-gray-500">
                        <i class="fab fa-facebook"></i>
                    </a>
                </div>
            </div>
            <div class="mt-8 text-center text-gray-400 text-sm">
                <p>© 2023 ResuCraftify. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

4th webpage code:-
------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ResuCraftify - Build Your Perfect Resume</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .fade-in {
            animation: fadeIn 0.5s ease-in-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .progress-bar {
            transition: width 0.5s ease-in-out;
        }
        
        .section-card {
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            transition: all 0.3s ease;
        }
        
        .section-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
        
        .input-highlight {
            transition: all 0.3s ease;
        }
        
        .input-highlight:focus {
            border-color: #4f46e5;
            box-shadow: 0 0 0 3px rgba(79, 70, 229, 0.2);
        }
    </style>
</head>
<body class="bg-gray-50 min-h-screen">
    <div class="container mx-auto px-4 py-8 max-w-4xl">
        <!-- Header Section -->
        <header class="text-center mb-10 fade-in">
            <h1 class="text-4xl font-bold text-indigo-700 mb-3">Start Building Your Resume</h1>
            <p class="text-lg text-gray-600">Let's craft a resume that highlights your unique skills and experiences!</p>
            <div class="mt-6">
                <div class="w-full bg-gray-200 rounded-full h-2.5">
                    <div id="progress-bar" class="progress-bar bg-indigo-600 h-2.5 rounded-full" style="width: 16%"></div>
                </div>
                <p id="progress-text" class="text-sm text-gray-500 mt-2">Step 1 of 6 - Basic Information</p>
            </div>
        </header>

        <!-- Form Container -->
        <div class="bg-white rounded-xl shadow-md overflow-hidden p-6 mb-8">
            <!-- Multi-step form -->
            <form id="resume-form">
                <!-- Step 1: Basic Information -->
                <div id="step-1" class="form-step active fade-in">
                    <div class="flex items-center mb-6">
                        <div class="bg-indigo-100 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                            <span class="text-indigo-700 font-bold">1</span>
                        </div>
                        <h2 class="text-2xl font-semibold text-gray-800">Basic Information</h2>
                    </div>
                    
                    <div class="space-y-5">
                        <div class="section-card bg-gray-50 p-5 rounded-lg">
                            <label for="full-name" class="block text-sm font-medium text-gray-700 mb-1">Full Name</label>
                            <input type="text" id="full-name" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. John Doe">
                            <p class="mt-1 text-xs text-gray-500">This will be the headline of your resume</p>
                        </div>
                        
                        <div class="section-card bg-gray-50 p-5 rounded-lg">
                            <label for="email" class="block text-sm font-medium text-gray-700 mb-1">Email Address</label>
                            <input type="email" id="email" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. john.doe@example.com">
                        </div>
                        
                        <div class="section-card bg-gray-50 p-5 rounded-lg">
                            <label for="phone" class="block text-sm font-medium text-gray-700 mb-1">Phone Number</label>
                            <input type="tel" id="phone" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. (123) 456-7890">
                        </div>
                        
                        <div class="section-card bg-gray-50 p-5 rounded-lg">
                            <label for="linkedin" class="block text-sm font-medium text-gray-700 mb-1">LinkedIn Profile (Optional)</label>
                            <input type="url" id="linkedin" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. linkedin.com/in/johndoe">
                        </div>
                        
                        <div class="section-card bg-gray-50 p-5 rounded-lg">
                            <label for="portfolio" class="block text-sm font-medium text-gray-700 mb-1">Portfolio Website (Optional)</label>
                            <input type="url" id="portfolio" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. johndoe.dev">
                        </div>
                    </div>
                </div>

                <!-- Step 2: Work Experience -->
                <div id="step-2" class="form-step hidden">
                    <div class="flex items-center mb-6">
                        <div class="bg-indigo-100 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                            <span class="text-indigo-700 font-bold">2</span>
                        </div>
                        <h2 class="text-2xl font-semibold text-gray-800">Work Experience</h2>
                    </div>
                    
                    <div id="experience-container">
                        <div class="experience-section section-card bg-gray-50 p-5 rounded-lg mb-5">
                            <div class="flex justify-between items-center mb-3">
                                <h3 class="font-medium text-gray-800">Experience #1</h3>
                                <button type="button" class="text-red-500 hover:text-red-700 text-sm" onclick="removeExperience(this)">
                                    <i class="fas fa-trash-alt mr-1"></i> Remove
                                </button>
                            </div>
                            
                            <div class="space-y-4">
                                <div>
                                    <label for="job-title" class="block text-sm font-medium text-gray-700 mb-1">Job Title</label>
                                    <input type="text" name="job-title[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. Software Engineer">
                                </div>
                                
                                <div>
                                    <label for="company" class="block text-sm font-medium text-gray-700 mb-1">Company Name</label>
                                    <input type="text" name="company[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. Tech Solutions Inc.">
                                </div>
                                
                                <div class="grid grid-cols-2 gap-4">
                                    <div>
                                        <label for="start-date" class="block text-sm font-medium text-gray-700 mb-1">Start Date</label>
                                        <input type="month" name="start-date[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200">
                                    </div>
                                    <div>
                                        <label for="end-date" class="block text-sm font-medium text-gray-700 mb-1">End Date</label>
                                        <input type="month" name="end-date[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200">
                                        <div class="flex items-center mt-2">
                                            <input type="checkbox" name="current-job[]" id="current-job" class="h-4 w-4 text-indigo-600 focus:ring-indigo-500 border-gray-300 rounded">
                                            <label for="current-job" class="ml-2 block text-sm text-gray-700">I currently work here</label>
                                        </div>
                                    </div>
                                </div>
                                
                                <div>
                                    <label for="job-description" class="block text-sm font-medium text-gray-700 mb-1">Job Description</label>
                                    <textarea name="job-description[]" rows="3" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="Describe your responsibilities and achievements..."></textarea>
                                    <p class="mt-1 text-xs text-gray-500">Use bullet points for better readability (e.g., • Developed new features...)</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <button type="button" onclick="addExperience()" class="mt-3 flex items-center text-indigo-600 hover:text-indigo-800">
                        <i class="fas fa-plus-circle mr-2"></i> Add Another Experience
                    </button>
                </div>

                <!-- Step 3: Education -->
                <div id="step-3" class="form-step hidden">
                    <div class="flex items-center mb-6">
                        <div class="bg-indigo-100 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                            <span class="text-indigo-700 font-bold">3</span>
                        </div>
                        <h2 class="text-2xl font-semibold text-gray-800">Education</h2>
                    </div>
                    
                    <div id="education-container">
                        <div class="education-section section-card bg-gray-50 p-5 rounded-lg mb-5">
                            <div class="flex justify-between items-center mb-3">
                                <h3 class="font-medium text-gray-800">Education #1</h3>
                                <button type="button" class="text-red-500 hover:text-red-700 text-sm" onclick="removeEducation(this)">
                                    <i class="fas fa-trash-alt mr-1"></i> Remove
                                </button>
                            </div>
                            
                            <div class="space-y-4">
                                <div>
                                    <label for="degree" class="block text-sm font-medium text-gray-700 mb-1">Degree/Certificate</label>
                                    <input type="text" name="degree[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. Bachelor of Science in Computer Science">
                                </div>
                                
                                <div>
                                    <label for="institution" class="block text-sm font-medium text-gray-700 mb-1">Institution</label>
                                    <input type="text" name="institution[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. University of Technology">
                                </div>
                                
                                <div class="grid grid-cols-2 gap-4">
                                    <div>
                                        <label for="education-start-date" class="block text-sm font-medium text-gray-700 mb-1">Start Date</label>
                                        <input type="month" name="education-start-date[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200">
                                    </div>
                                    <div>
                                        <label for="education-end-date" class="block text-sm font-medium text-gray-700 mb-1">End Date (or Expected)</label>
                                        <input type="month" name="education-end-date[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200">
                                        <div class="flex items-center mt-2">
                                            <input type="checkbox" name="current-education[]" id="current-education" class="h-4 w-4 text-indigo-600 focus:ring-indigo-500 border-gray-300 rounded">
                                            <label for="current-education" class="ml-2 block text-sm text-gray-700">Currently studying here</label>
                                        </div>
                                    </div>
                                </div>
                                
                                <div>
                                    <label for="education-description" class="block text-sm font-medium text-gray-700 mb-1">Description (Optional)</label>
                                    <textarea name="education-description[]" rows="2" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="Relevant coursework, honors, or achievements..."></textarea>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <button type="button" onclick="addEducation()" class="mt-3 flex items-center text-indigo-600 hover:text-indigo-800">
                        <i class="fas fa-plus-circle mr-2"></i> Add Another Education Entry
                    </button>
                </div>

                <!-- Step 4: Skills -->
                <div id="step-4" class="form-step hidden">
                    <div class="flex items-center mb-6">
                        <div class="bg-indigo-100 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                            <span class="text-indigo-700 font-bold">4</span>
                        </div>
                        <h2 class="text-2xl font-semibold text-gray-800">Skills</h2>
                    </div>
                    
                    <div class="section-card bg-gray-50 p-5 rounded-lg mb-5">
                        <div class="mb-4">
                            <label class="block text-sm font-medium text-gray-700 mb-2">Technical Skills</label>
                            <div id="technical-skills-container" class="flex flex-wrap gap-2 mb-3">
                                <!-- Skills will be added here -->
                            </div>
                            <div class="flex">
                                <input type="text" id="technical-skill-input" class="input-highlight flex-1 px-4 py-2 border border-gray-300 rounded-l-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. JavaScript, Python, Photoshop">
                                <button type="button" onclick="addSkill('technical')" class="bg-indigo-600 text-white px-4 py-2 rounded-r-md hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500">
                                    <i class="fas fa-plus"></i>
                                </button>
                            </div>
                            <p class="mt-1 text-xs text-gray-500">Add your technical skills one by one</p>
                        </div>
                        
                        <div class="mb-4">
                            <label class="block text-sm font-medium text-gray-700 mb-2">Soft Skills</label>
                            <div id="soft-skills-container" class="flex flex-wrap gap-2 mb-3">
                                <!-- Skills will be added here -->
                            </div>
                            <div class="flex">
                                <input type="text" id="soft-skill-input" class="input-highlight flex-1 px-4 py-2 border border-gray-300 rounded-l-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. Communication, Leadership, Teamwork">
                                <button type="button" onclick="addSkill('soft')" class="bg-indigo-600 text-white px-4 py-2 rounded-r-md hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500">
                                    <i class="fas fa-plus"></i>
                                </button>
                            </div>
                        </div>
                        
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Languages</label>
                            <div id="language-skills-container" class="flex flex-wrap gap-2 mb-3">
                                <!-- Languages will be added here -->
                            </div>
                            <div class="flex">
                                <input type="text" id="language-skill-input" class="input-highlight flex-1 px-4 py-2 border border-gray-300 rounded-l-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. English (Fluent), Spanish (Intermediate)">
                                <button type="button" onclick="addSkill('language')" class="bg-indigo-600 text-white px-4 py-2 rounded-r-md hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500">
                                    <i class="fas fa-plus"></i>
                                </button>
                            </div>
                            <p class="mt-1 text-xs text-gray-500">Include proficiency level in parentheses</p>
                        </div>
                    </div>
                    
                    <div class="section-card bg-gray-50 p-5 rounded-lg">
                        <label for="certifications" class="block text-sm font-medium text-gray-700 mb-2">Certifications (Optional)</label>
                        <textarea id="certifications" rows="3" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="List any relevant certifications you've earned..."></textarea>
                    </div>
                </div>

                <!-- Step 5: Summary -->
                <div id="step-5" class="form-step hidden">
                    <div class="flex items-center mb-6">
                        <div class="bg-indigo-100 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                            <span class="text-indigo-700 font-bold">5</span>
                        </div>
                        <h2 class="text-2xl font-semibold text-gray-800">Professional Summary</h2>
                    </div>
                    
                    <div class="section-card bg-gray-50 p-5 rounded-lg mb-5">
                        <label for="summary" class="block text-sm font-medium text-gray-700 mb-2">About You</label>
                        <textarea id="summary" rows="5" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="Write a brief summary of your professional background, skills, and career goals. Keep it concise (3-5 sentences)."></textarea>
                        <p class="mt-2 text-sm text-gray-600">Example: "Results-driven software engineer with 5+ years of experience in full-stack development. Specialized in JavaScript frameworks and cloud technologies. Passionate about creating efficient, scalable solutions that improve user experience. Strong collaborator with excellent problem-solving skills."</p>
                    </div>
                    
                    <div class="section-card bg-gray-50 p-5 rounded-lg">
                        <label class="block text-sm font-medium text-gray-700 mb-2">Career Objective (Optional)</label>
                        <textarea id="objective" rows="3" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="If you're early in your career, you might include a career objective..."></textarea>
                        <p class="mt-1 text-xs text-gray-500">Tip: Focus on what you can offer employers rather than what you want from them.</p>
                    </div>
                </div>

                <!-- Step 6: Additional Details -->
                <div id="step-6" class="form-step hidden">
                    <div class="flex items-center mb-6">
                        <div class="bg-indigo-100 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                            <span class="text-indigo-700 font-bold">6</span>
                        </div>
                        <h2 class="text-2xl font-semibold text-gray-800">Additional Details</h2>
                    </div>
                    
                    <div class="space-y-5">
                        <div class="section-card bg-gray-50 p-5 rounded-lg">
                            <label for="projects" class="block text-sm font-medium text-gray-700 mb-2">Projects (Optional)</label>
                            <textarea id="projects" rows="4" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="Describe any significant projects you've worked on..."></textarea>
                            <p class="mt-1 text-xs text-gray-500">Include project name, your role, technologies used, and outcomes if possible.</p>
                        </div>
                        
                        <div class="section-card bg-gray-50 p-5 rounded-lg">
                            <label for="volunteer" class="block text-sm font-medium text-gray-700 mb-2">Volunteer Work (Optional)</label>
                            <textarea id="volunteer" rows="3" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="List any relevant volunteer experience..."></textarea>
                        </div>
                        
                        <div class="section-card bg-gray-50 p-5 rounded-lg">
                            <label for="hobbies" class="block text-sm font-medium text-gray-700 mb-2">Hobbies & Interests (Optional)</label>
                            <textarea id="hobbies" rows="2" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="List hobbies that might be relevant to your profession..."></textarea>
                            <p class="mt-1 text-xs text-gray-500">Example for developer: "Open-source contributor, tech blogging, hackathon participant"</p>
                        </div>
                        
                        <div class="section-card bg-gray-50 p-5 rounded-lg">
                            <label class="block text-sm font-medium text-gray-700 mb-2">Resume Template</label>
                            <div class="grid grid-cols-3 gap-4">
                                <div>
                                    <input type="radio" id="template-1" name="template" value="classic" class="hidden peer" checked>
                                    <label for="template-1" class="inline-flex items-center justify-between p-2 w-full text-gray-500 bg-white rounded-lg border border-gray-200 cursor-pointer peer-checked:border-indigo-600 peer-checked:text-indigo-600 hover:text-gray-600 hover:bg-gray-50">
                                        <div class="block">
                                            <div class="w-full text-sm font-semibold">Classic</div>
                                            <div class="w-full text-xs">Clean & Professional</div>
                                        </div>
                                        <i class="fas fa-file-alt ml-2"></i>
                                    </label>
                                </div>
                                <div>
                                    <input type="radio" id="template-2" name="template" value="modern" class="hidden peer">
                                    <label for="template-2" class="inline-flex items-center justify-between p-2 w-full text-gray-500 bg-white rounded-lg border border-gray-200 cursor-pointer peer-checked:border-indigo-600 peer-checked:text-indigo-600 hover:text-gray-600 hover:bg-gray-50">
                                        <div class="block">
                                            <div class="w-full text-sm font-semibold">Modern</div>
                                            <div class="w-full text-xs">Creative & Bold</div>
                                        </div>
                                        <i class="fas fa-file-code ml-2"></i>
                                    </label>
                                </div>
                                <div>
                                    <input type="radio" id="template-3" name="template" value="minimal" class="hidden peer">
                                    <label for="template-3" class="inline-flex items-center justify-between p-2 w-full text-gray-500 bg-white rounded-lg border border-gray-200 cursor-pointer peer-checked:border-indigo-600 peer-checked:text-indigo-600 hover:text-gray-600 hover:bg-gray-50">
                                        <div class="block">
                                            <div class="w-full text-sm font-semibold">Minimal</div>
                                            <div class="w-full text-xs">Simple & Elegant</div>
                                        </div>
                                        <i class="fas fa-file ml-2"></i>
                                    </label>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </form>
        </div>

        <!-- Navigation Buttons -->
        <div class="flex justify-between mt-8">
            <button id="prev-btn" class="hidden px-6 py-2 bg-gray-200 text-gray-700 rounded-md hover:bg-gray-300 focus:outline-none focus:ring-2 focus:ring-gray-400">
                <i class="fas fa-arrow-left mr-2"></i> Previous
            </button>
            <button id="next-btn" class="ml-auto px-6 py-2 bg-indigo-600 text-white rounded-md hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500">
                Next <i class="fas fa-arrow-right ml-2"></i>
            </button>
            <button id="submit-btn" class="hidden ml-auto px-6 py-2 bg-green-600 text-white rounded-md hover:bg-green-700 focus:outline-none focus:ring-2 focus:ring-green-500">
                <i class="fas fa-check-circle mr-2"></i> Generate Resume
            </button>
        </div>
    </div>

    <script>
        // Current step tracking
        let currentStep = 1;
        const totalSteps = 6;
        
        // DOM elements
        const nextBtn = document.getElementById('next-btn');
        const prevBtn = document.getElementById('prev-btn');
        const submitBtn = document.getElementById('submit-btn');
        const progressBar = document.getElementById('progress-bar');
        const progressText = document.getElementById('progress-text');
        
        // Initialize the form
        document.addEventListener('DOMContentLoaded', function() {
            updateProgress();
            
            // Next button click handler
            nextBtn.addEventListener('click', function() {
                if (validateStep(currentStep)) {
                    navigateToStep(currentStep + 1);
                }
            });
            
            // Previous button click handler
            prevBtn.addEventListener('click', function() {
                navigateToStep(currentStep - 1);
            });
            
            // Submit button click handler
            submitBtn.addEventListener('click', function() {
                if (validateStep(currentStep)) {
                    alert('Resume generated successfully! This would typically redirect to a preview page.');
                    // Here you would typically submit the form via AJAX or redirect to a preview page
                }
            });
        });
        
        // Navigate between steps
        function navigateToStep(step) {
            // Hide current step
            document.getElementById(`step-${currentStep}`).classList.remove('active');
            document.getElementById(`step-${currentStep}`).classList.add('hidden');
            
            // Show new step
            document.getElementById(`step-${step}`).classList.remove('hidden');
            document.getElementById(`step-${step}`).classList.add('active', 'fade-in');
            
            // Update current step
            currentStep = step;
            updateProgress();
            
            // Update button visibility
            if (currentStep === 1) {
                prevBtn.classList.add('hidden');
            } else {
                prevBtn.classList.remove('hidden');
            }
            
            if (currentStep === totalSteps) {
                nextBtn.classList.add('hidden');
                submitBtn.classList.remove('hidden');
            } else {
                nextBtn.classList.remove('hidden');
                submitBtn.classList.add('hidden');
            }
        }
        
        // Update progress bar and text
        function updateProgress() {
            const progressPercentage = (currentStep / totalSteps) * 100;
            progressBar.style.width = `${progressPercentage}%`;
            
            let stepText = '';
            switch(currentStep) {
                case 1:
                    stepText = 'Basic Information';
                    break;
                case 2:
                    stepText = 'Work Experience';
                    break;
                case 3:
                    stepText = 'Education';
                    break;
                case 4:
                    stepText = 'Skills';
                    break;
                case 5:
                    stepText = 'Professional Summary';
                    break;
                case 6:
                    stepText = 'Additional Details';
                    break;
            }
            
            progressText.textContent = `Step ${currentStep} of ${totalSteps} - ${stepText}`;
        }
        
        // Validate current step before proceeding
        function validateStep(step) {
            let isValid = true;
            
            switch(step) {
                case 1:
                    const fullName = document.getElementById('full-name').value.trim();
                    const email = document.getElementById('email').value.trim();
                    
                    if (!fullName) {
                        alert('Please enter your full name');
                        isValid = false;
                    } else if (!email) {
                        alert('Please enter your email address');
                        isValid = false;
                    } else if (!validateEmail(email)) {
                        alert('Please enter a valid email address');
                        isValid = false;
                    }
                    break;
                    
                case 2:
                    const jobTitles = document.getElementsByName('job-title[]');
                    if (jobTitles.length > 0 && !jobTitles[0].value.trim()) {
                        alert('Please enter at least one work experience');
                        isValid = false;
                    }
                    break;
                    
                case 3:
                    const degrees = document.getElementsByName('degree[]');
                    if (degrees.length > 0 && !degrees[0].value.trim()) {
                        alert('Please enter at least one education entry');
                        isValid = false;
                    }
                    break;
                    
                case 5:
                    const summary = document.getElementById('summary').value.trim();
                    if (!summary) {
                        alert('Please write a professional summary');
                        isValid = false;
                    }
                    break;
            }
            
            return isValid;
        }
        
        // Email validation helper
        function validateEmail(email) {
            const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return re.test(email);
        }
        
        // Experience section management
        function addExperience() {
            const container = document.getElementById('experience-container');
            const count = container.getElementsByClassName('experience-section').length + 1;
            
            const newExperience = document.createElement('div');
            newExperience.className = 'experience-section section-card bg-gray-50 p-5 rounded-lg mb-5 fade-in';
            newExperience.innerHTML = `
                <div class="flex justify-between items-center mb-3">
                    <h3 class="font-medium text-gray-800">Experience #${count}</h3>
                    <button type="button" class="text-red-500 hover:text-red-700 text-sm" onclick="removeExperience(this)">
                        <i class="fas fa-trash-alt mr-1"></i> Remove
                    </button>
                </div>
                
                <div class="space-y-4">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Job Title</label>
                        <input type="text" name="job-title[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. Software Engineer">
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Company Name</label>
                        <input type="text" name="company[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. Tech Solutions Inc.">
                    </div>
                    
                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Start Date</label>
                            <input type="month" name="start-date[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200">
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">End Date</label>
                            <input type="month" name="end-date[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200">
                            <div class="flex items-center mt-2">
                                <input type="checkbox" name="current-job[]" class="h-4 w-4 text-indigo-600 focus:ring-indigo-500 border-gray-300 rounded">
                                <label class="ml-2 block text-sm text-gray-700">I currently work here</label>
                            </div>
                        </div>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Job Description</label>
                        <textarea name="job-description[]" rows="3" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="Describe your responsibilities and achievements..."></textarea>
                    </div>
                </div>
            `;
            
            container.appendChild(newExperience);
            scrollToBottom();
        }
        
        function removeExperience(button) {
            const section = button.closest('.experience-section');
            if (document.getElementsByClassName('experience-section').length > 1) {
                section.classList.add('hidden');
                setTimeout(() => section.remove(), 300);
            } else {
                alert('You need to have at least one experience entry');
            }
        }
        
        // Education section management
        function addEducation() {
            const container = document.getElementById('education-container');
            const count = container.getElementsByClassName('education-section').length + 1;
            
            const newEducation = document.createElement('div');
            newEducation.className = 'education-section section-card bg-gray-50 p-5 rounded-lg mb-5 fade-in';
            newEducation.innerHTML = `
                <div class="flex justify-between items-center mb-3">
                    <h3 class="font-medium text-gray-800">Education #${count}</h3>
                    <button type="button" class="text-red-500 hover:text-red-700 text-sm" onclick="removeEducation(this)">
                        <i class="fas fa-trash-alt mr-1"></i> Remove
                    </button>
                </div>
                
                <div class="space-y-4">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Degree/Certificate</label>
                        <input type="text" name="degree[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. Bachelor of Science in Computer Science">
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Institution</label>
                        <input type="text" name="institution[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="e.g. University of Technology">
                    </div>
                    
                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Start Date</label>
                            <input type="month" name="education-start-date[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200">
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">End Date (or Expected)</label>
                            <input type="month" name="education-end-date[]" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200">
                            <div class="flex items-center mt-2">
                                <input type="checkbox" name="current-education[]" class="h-4 w-4 text-indigo-600 focus:ring-indigo-500 border-gray-300 rounded">
                                <label class="ml-2 block text-sm text-gray-700">Currently studying here</label>
                            </div>
                        </div>
                    </div>
                    
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Description (Optional)</label>
                        <textarea name="education-description[]" rows="2" class="input-highlight w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-200" placeholder="Relevant coursework, honors, or achievements..."></textarea>
                    </div>
                </div>
            `;
            
            container.appendChild(newEducation);
            scrollToBottom();
        }
        
        function removeEducation(button) {
            const section = button.closest('.education-section');
            if (document.getElementsByClassName('education-section').length > 1) {
                section.classList.add('hidden');
                setTimeout(() => section.remove(), 300);
            } else {
                alert('You need to have at least one education entry');
            }
        }
        
        // Skills management
        function addSkill(type) {
            const inputId = `${type}-skill-input`;
            const containerId = `${type}-skills-container`;
            
            const input = document.getElementById(inputId);
            const skill = input.value.trim();
            
            if (skill) {
                const container = document.getElementById(containerId);
                const skillElement = document.createElement('div');
                skillElement.className = 'skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm flex items-center fade-in';
                skillElement.innerHTML = `
                    ${skill}
                    <button type="button" onclick="removeSkill(this)" class="ml-2 text-indigo-500 hover:text-indigo-700">
                        <i class="fas fa-times"></i>
                    </button>
                    <input type="hidden" name="${type}-skills[]" value="${skill}">
                `;
                
                container.appendChild(skillElement);
                input.value = '';
            }
        }
        
        function removeSkill(button) {
            const skillTag = button.closest('.skill-tag');
            skillTag.classList.add('hidden');
            setTimeout(() => skillTag.remove(), 300);
        }
        
        // Helper function to scroll to bottom when adding new sections
        function scrollToBottom() {
            window.scrollTo({
                top: document.body.scrollHeight,
                behavior: 'smooth'
            });
        }
    </script>
</body>
</html>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

5th webpage code:-
------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ResuCraftify - Resume Preview</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&family=Playfair+Display:wght@400;500;700&display=swap');
        
        body {
            font-family: 'Roboto', sans-serif;
        }
        
        .resume-header {
            font-family: 'Playfair Display', serif;
        }
        
        .section-title {
            font-family: 'Playfair Display', serif;
        }
        
        .resume-paper {
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        .fade-in {
            animation: fadeIn 0.5s ease-in-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .skill-tag {
            transition: all 0.3s ease;
        }
        
        .skill-tag:hover {
            transform: translateY(-2px);
        }
        
        @media print {
            .no-print {
                display: none !important;
            }
            
            body {
                background: white !important;
            }
            
            .resume-paper {
                box-shadow: none !important;
                margin: 0 !important;
                padding: 0 !important;
            }
        }
    </style>
</head>
<body class="bg-gray-100">
    <div class="container mx-auto px-4 py-8 max-w-6xl">
        <!-- Header with actions -->
        <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-8 no-print">
            <div>
                <h1 class="text-3xl font-bold text-indigo-700 mb-2">Your Resume Preview</h1>
                <p class="text-gray-600">Review and finalize your professional resume</p>
            </div>
            
            <div class="mt-4 md:mt-0 flex flex-wrap gap-3">
                <button onclick="window.print()" class="px-4 py-2 bg-white border border-gray-300 text-gray-700 rounded-md hover:bg-gray-50 flex items-center">
                    <i class="fas fa-print mr-2"></i> Print
                </button>
                <button class="px-4 py-2 bg-indigo-600 text-white rounded-md hover:bg-indigo-700 flex items-center">
                    <i class="fas fa-file-pdf mr-2"></i> Download PDF
                </button>
                <button class="px-4 py-2 bg-green-600 text-white rounded-md hover:bg-green-700 flex items-center">
                    <i class="fas fa-envelope mr-2"></i> Email Resume
                </button>
                <a href="#" class="px-4 py-2 bg-gray-800 text-white rounded-md hover:bg-gray-900 flex items-center">
                    <i class="fas fa-edit mr-2"></i> Edit Resume
                </a>
            </div>
        </div>
        
        <!-- Resume Container -->
        <div class="flex flex-col lg:flex-row gap-8">
            <!-- Resume Preview -->
            <div class="flex-1">
                <div class="resume-paper bg-white rounded-lg p-8 mb-6 fade-in">
                    <!-- Header Section -->
                    <div class="resume-header border-b-2 border-indigo-100 pb-6 mb-6">
                        <h1 class="text-4xl font-bold text-gray-800 mb-1">John Doe</h1>
                        <h2 class="text-2xl text-indigo-600 font-medium mb-4">Senior Software Engineer</h2>
                        
                        <div class="flex flex-wrap gap-x-8 gap-y-2 text-gray-700">
                            <div class="flex items-center">
                                <i class="fas fa-envelope text-indigo-500 mr-2"></i>
                                <span>john.doe@example.com</span>
                            </div>
                            <div class="flex items-center">
                                <i class="fas fa-phone text-indigo-500 mr-2"></i>
                                <span>(123) 456-7890</span>
                            </div>
                            <div class="flex items-center">
                                <i class="fab fa-linkedin text-indigo-500 mr-2"></i>
                                <span>linkedin.com/in/johndoe</span>
                            </div>
                            <div class="flex items-center">
                                <i class="fas fa-globe text-indigo-500 mr-2"></i>
                                <span>johndoe.dev</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Summary Section -->
                    <div class="mb-6">
                        <h3 class="section-title text-xl font-bold text-gray-800 mb-3 flex items-center">
                            <span class="bg-indigo-600 w-5 h-1 mr-2"></span>
                            Professional Summary
                        </h3>
                        <p class="text-gray-700 leading-relaxed">
                            Results-driven software engineer with 8+ years of experience in full-stack development. 
                            Specialized in JavaScript frameworks and cloud technologies. Passionate about creating 
                            efficient, scalable solutions that improve user experience. Strong collaborator with 
                            excellent problem-solving skills and a track record of delivering high-quality software 
                            on time.
                        </p>
                    </div>
                    
                    <!-- Experience Section -->
                    <div class="mb-6">
                        <h3 class="section-title text-xl font-bold text-gray-800 mb-3 flex items-center">
                            <span class="bg-indigo-600 w-5 h-1 mr-2"></span>
                            Work Experience
                        </h3>
                        
                        <div class="space-y-6">
                            <!-- Experience 1 -->
                            <div>
                                <div class="flex flex-col sm:flex-row sm:justify-between mb-1">
                                    <h4 class="font-bold text-gray-800">Senior Software Engineer</h4>
                                    <div class="text-indigo-600">Jan 2020 - Present</div>
                                </div>
                                <div class="flex justify-between text-gray-600 mb-2">
                                    <div>Tech Solutions Inc., San Francisco, CA</div>
                                </div>
                                <ul class="list-disc list-inside text-gray-700 space-y-1 pl-2">
                                    <li>Led a team of 5 developers to build a new customer portal using React and Node.js</li>
                                    <li>Improved application performance by 40% through code optimization and caching</li>
                                    <li>Implemented CI/CD pipeline reducing deployment time by 60%</li>
                                    <li>Mentored junior developers and conducted code reviews</li>
                                </ul>
                            </div>
                            
                            <!-- Experience 2 -->
                            <div>
                                <div class="flex flex-col sm:flex-row sm:justify-between mb-1">
                                    <h4 class="font-bold text-gray-800">Software Engineer</h4>
                                    <div class="text-indigo-600">Mar 2017 - Dec 2019</div>
                                </div>
                                <div class="flex justify-between text-gray-600 mb-2">
                                    <div>Digital Innovations LLC, Austin, TX</div>
                                </div>
                                <ul class="list-disc list-inside text-gray-700 space-y-1 pl-2">
                                    <li>Developed RESTful APIs using Express.js and MongoDB</li>
                                    <li>Created responsive front-end components with React and Redux</li>
                                    <li>Collaborated with UX designers to improve user experience</li>
                                    <li>Participated in Agile development process with bi-weekly sprints</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Skills Section -->
                    <div class="mb-6">
                        <h3 class="section-title text-xl font-bold text-gray-800 mb-3 flex items-center">
                            <span class="bg-indigo-600 w-5 h-1 mr-2"></span>
                            Skills
                        </h3>
                        
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                            <div>
                                <h4 class="font-medium text-gray-800 mb-2">Technical Skills</h4>
                                <div class="flex flex-wrap gap-2">
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">JavaScript</span>
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">React</span>
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Node.js</span>
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">TypeScript</span>
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">AWS</span>
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Docker</span>
                                </div>
                            </div>
                            
                            <div>
                                <h4 class="font-medium text-gray-800 mb-2">Soft Skills</h4>
                                <div class="flex flex-wrap gap-2">
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Leadership</span>
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Teamwork</span>
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Problem Solving</span>
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Communication</span>
                                </div>
                            </div>
                            
                            <div>
                                <h4 class="font-medium text-gray-800 mb-2">Languages</h4>
                                <div class="flex flex-wrap gap-2">
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">English (Fluent)</span>
                                    <span class="skill-tag bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Spanish (Intermediate)</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Education Section -->
                    <div>
                        <h3 class="section-title text-xl font-bold text-gray-800 mb-3 flex items-center">
                            <span class="bg-indigo-600 w-5 h-1 mr-2"></span>
                            Education
                        </h3>
                        
                        <div class="space-y-4">
                            <div>
                                <div class="flex flex-col sm:flex-row sm:justify-between mb-1">
                                    <h4 class="font-bold text-gray-800">Master of Science in Computer Science</h4>
                                    <div class="text-indigo-600">2015 - 2017</div>
                                </div>
                                <div class="text-gray-600">Stanford University, Stanford, CA</div>
                                <p class="text-gray-700 mt-1">GPA: 3.8/4.0</p>
                            </div>
                            
                            <div>
                                <div class="flex flex-col sm:flex-row sm:justify-between mb-1">
                                    <h4 class="font-bold text-gray-800">Bachelor of Science in Software Engineering</h4>
                                    <div class="text-indigo-600">2011 - 2015</div>
                                </div>
                                <div class="text-gray-600">University of Texas, Austin, TX</div>
                                <p class="text-gray-700 mt-1">Minor in Mathematics</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Template Selection -->
                <div class="bg-white rounded-lg p-6 mb-6 no-print">
                    <h3 class="text-xl font-bold text-gray-800 mb-4">Choose a Different Template</h3>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                        <div class="border rounded-lg overflow-hidden cursor-pointer hover:border-indigo-400 transition-all">
                            <div class="h-40 bg-indigo-50 flex items-center justify-center">
                                <div class="text-center p-4">
                                    <i class="fas fa-file-alt text-4xl text-indigo-600 mb-2"></i>
                                    <h4 class="font-bold">Classic</h4>
                                </div>
                            </div>
                        </div>
                        <div class="border rounded-lg overflow-hidden cursor-pointer hover:border-indigo-400 transition-all">
                            <div class="h-40 bg-indigo-50 flex items-center justify-center">
                                <div class="text-center p-4">
                                    <i class="fas fa-file-code text-4xl text-indigo-600 mb-2"></i>
                                    <h4 class="font-bold">Modern</h4>
                                </div>
                            </div>
                        </div>
                        <div class="border rounded-lg overflow-hidden cursor-pointer hover:border-indigo-400 transition-all">
                            <div class="h-40 bg-indigo-50 flex items-center justify-center">
                                <div class="text-center p-4">
                                    <i class="fas fa-file text-4xl text-indigo-600 mb-2"></i>
                                    <h4 class="font-bold">Minimal</h4>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Editing Panel -->
            <div class="lg:w-80 no-print">
                <div class="bg-white rounded-lg p-6 sticky top-6">
                    <h3 class="text-xl font-bold text-gray-800 mb-4">Finalize Your Resume</h3>
                    
                    <div class="space-y-4">
                        <div>
                            <h4 class="font-medium text-gray-800 mb-2">Download Options</h4>
                            <div class="space-y-2">
                                <button class="w-full px-4 py-2 bg-indigo-600 text-white rounded-md hover:bg-indigo-700 flex items-center justify-center">
                                    <i class="fas fa-file-pdf mr-2"></i> PDF (Recommended)
                                </button>
                                <button class="w-full px-4 py-2 border border-gray-300 text-gray-700 rounded-md hover:bg-gray-50 flex items-center justify-center">
                                    <i class="fas fa-file-word mr-2"></i> Word Document
                                </button>
                                <button class="w-full px-4 py-2 border border-gray-300 text-gray-700 rounded-md hover:bg-gray-50 flex items-center justify-center">
                                    <i class="fas fa-file-alt mr-2"></i> Plain Text
                                </button>
                            </div>
                        </div>
                        
                        <div>
                            <h4 class="font-medium text-gray-800 mb-2">Share Options</h4>
                            <div class="space-y-2">
                                <button class="w-full px-4 py-2 bg-blue-600 text-white rounded-md hover:bg-blue-700 flex items-center justify-center">
                                    <i class="fab fa-linkedin mr-2"></i> Share to LinkedIn
                                </button>
                                <button class="w-full px-4 py-2 bg-green-600 text-white rounded-md hover:bg-green-700 flex items-center justify-center">
                                    <i class="fas fa-envelope mr-2"></i> Email to Recruiter
                                </button>
                            </div>
                        </div>
                        
                        <div class="pt-4 border-t border-gray-200">
                            <h4 class="font-medium text-gray-800 mb-2">Final Tips</h4>
                            <ul class="list-disc list-inside text-sm text-gray-600 space-y-1">
                                <li>Review for typos and grammatical errors</li>
                                <li>Keep it to 1-2 pages maximum</li>
                                <li>Use action verbs to describe achievements</li>
                                <li>Quantify results when possible</li>
                                <li>Save multiple versions for different job types</li>
                            </ul>
                        </div>
                        
                        <div class="pt-4 border-t border-gray-200">
                            <button class="w-full px-4 py-2 bg-indigo-600 text-white rounded-md hover:bg-indigo-700 flex items-center justify-center">
                                <i class="fas fa-edit mr-2"></i> Edit Resume
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Print functionality
        function setupPrintButton() {
            const printButton = document.querySelector('[onclick="window.print()"]');
            printButton.addEventListener('click', function() {
                window.print();
            });
        }
        
        // Initialize
        document.addEventListener('DOMContentLoaded', function() {
            setupPrintButton();
            
            // Template selection
            const templates = document.querySelectorAll('.lg\\:w-80 .border.rounded-lg');
            templates.forEach(template => {
                template.addEventListener('click', function() {
                    templates.forEach(t => t.classList.remove('border-indigo-500', 'ring-2', 'ring-indigo-200'));
                    this.classList.add('border-indigo-500', 'ring-2', 'ring-indigo-200');
                    
                    // Here you would typically change the template via AJAX
                    alert('Template changed! In a real app, this would update the resume template.');
                });
            });
        });
    </script>
</body>
</html>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

6th webpage code:-
------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ResuCraftify - Career Insights & AI Resume Tips</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap');
        
        body {
            font-family: 'Montserrat', sans-serif;
        }
        
        .header-font {
            font-family: 'Playfair Display', serif;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #3b82f6 0%, #6366f1 100%);
        }
        
        .article-card {
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }
        
        .article-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
        }
        
        .trending-badge {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(239, 68, 68, 0.7);
            }
            70% {
                box-shadow: 0 0 0 10px rgba(239, 68, 68, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(239, 68, 68, 0);
            }
        }
        
        .category-tag {
            transition: all 0.2s ease;
        }
        
        .category-tag:hover {
            transform: scale(1.05);
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Navigation -->
    <nav class="bg-white shadow-sm">
        <div class="container mx-auto px-4 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-blue-600 flex items-center">
                <i class="fas fa-pen-fancy mr-2"></i> ResuCraftify
            </a>
            <div class="hidden md:flex space-x-8">
                <a href="#" class="text-gray-600 hover:text-blue-600">Home</a>
                <a href="#" class="text-blue-600 font-medium">Blog</a>
                <a href="#" class="text-gray-600 hover:text-blue-600">Resume Builder</a>
                <a href="#" class="text-gray-600 hover:text-blue-600">Templates</a>
                <a href="#" class="text-gray-600 hover:text-blue-600">About</a>
            </div>
            <div class="flex items-center space-x-4">
                <button class="md:hidden text-gray-600">
                    <i class="fas fa-bars text-xl"></i>
                </button>
                <button class="hidden md:block bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition">
                    Get Started
                </button>
            </div>
        </div>
    </nav>
    
    <!-- Hero Section -->
    <div class="gradient-bg text-white">
        <div class="container mx-auto px-4 py-16 md:py-24">
            <div class="max-w-3xl mx-auto text-center">
                <h1 class="header-font text-4xl md:text-5xl font-bold mb-4">Career Insights & AI Resume Tips</h1>
                <p class="text-xl mb-8 opacity-90">Discover the latest trends in resume writing, AI tools, and career advancement strategies from industry experts.</p>
                <div class="relative max-w-md mx-auto">
                    <input type="text" placeholder="Search articles..." class="w-full py-3 px-5 rounded-full text-gray-800 focus:outline-none focus:ring-2 focus:ring-blue-400">
                    <button class="absolute right-2 top-1/2 transform -translate-y-1/2 bg-blue-600 text-white p-2 rounded-full hover:bg-blue-700">
                        <i class="fas fa-search"></i>
                    </button>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Main Content -->
    <div class="container mx-auto px-4 py-12">
        <div class="flex flex-col lg:flex-row gap-8">
            <!-- Articles Section -->
            <div class="lg:w-2/3">
                <!-- Categories -->
                <div class="flex flex-wrap gap-3 mb-8">
                    <a href="#" class="category-tag bg-blue-600 text-white px-4 py-1 rounded-full text-sm font-medium">All Topics</a>
                    <a href="#" class="category-tag bg-white border border-gray-300 text-gray-700 px-4 py-1 rounded-full text-sm font-medium hover:bg-gray-100">AI Tools</a>
                    <a href="#" class="category-tag bg-white border border-gray-300 text-gray-700 px-4 py-1 rounded-full text-sm font-medium hover:bg-gray-100">Resume Writing</a>
                    <a href="#" class="category-tag bg-white border border-gray-300 text-gray-700 px-4 py-1 rounded-full text-sm font-medium hover:bg-gray-100">Career Advice</a>
                    <a href="#" class="category-tag bg-white border border-gray-300 text-gray-700 px-4 py-1 rounded-full text-sm font-medium hover:bg-gray-100">ATS Optimization</a>
                    <a href="#" class="category-tag bg-white border border-gray-300 text-gray-700 px-4 py-1 rounded-full text-sm font-medium hover:bg-gray-100">Interview Tips</a>
                </div>
                
                <!-- Featured Article -->
                <div class="article-card bg-white rounded-xl overflow-hidden mb-8">
                    <div class="md:flex">
                        <div class="md:w-1/2">
                            <img src="https://images.unsplash.com/photo-1620712943543-bcc4688e7485?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="AI Resume Writing" class="w-full h-full object-cover">
                        </div>
                        <div class="p-6 md:w-1/2">
                            <div class="flex items-center mb-3">
                                <span class="trending-badge bg-red-500 text-white text-xs font-bold px-3 py-1 rounded-full mr-3">TRENDING</span>
                                <span class="text-sm text-gray-500">June 15, 2023</span>
                            </div>
                            <h2 class="header-font text-2xl font-bold mb-3">How AI is Revolutionizing Resume Writing in 2023</h2>
                            <p class="text-gray-600 mb-4">Discover the latest AI-powered tools that are transforming how professionals craft resumes that stand out to both hiring managers and applicant tracking systems.</p>
                            <div class="flex items-center justify-between">
                                <div class="flex items-center">
                                    <img src="https://randomuser.me/api/portraits/women/32.jpg" alt="Author" class="w-8 h-8 rounded-full mr-2">
                                    <span class="text-sm font-medium">Sarah Johnson</span>
                                </div>
                                <a href="#" class="text-blue-600 font-medium hover:text-blue-800 flex items-center">
                                    Read More <i class="fas fa-arrow-right ml-2"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Articles Grid -->
                <div class="grid md:grid-cols-2 gap-6">
                    <!-- Article 1 -->
                    <div class="article-card bg-white rounded-xl overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="ATS Resume" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <div class="flex items-center mb-3">
                                <span class="bg-blue-100 text-blue-800 text-xs font-bold px-3 py-1 rounded-full mr-3">NEW</span>
                                <span class="text-sm text-gray-500">June 10, 2023</span>
                            </div>
                            <h2 class="header-font text-xl font-bold mb-3">The Ultimate Guide to ATS-Optimized Resumes</h2>
                            <p class="text-gray-600 mb-4">Learn the secrets to formatting your resume so it passes through applicant tracking systems and gets seen by human recruiters.</p>
                            <a href="#" class="text-blue-600 font-medium hover:text-blue-800 flex items-center">
                                Read More <i class="fas fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                    
                    <!-- Article 2 -->
                    <div class="article-card bg-white rounded-xl overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1521791055366-0d553872125f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Career Change" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <div class="flex items-center mb-3">
                                <span class="text-sm text-gray-500">May 28, 2023</span>
                            </div>
                            <h2 class="header-font text-xl font-bold mb-3">How to Successfully Change Careers in 2023</h2>
                            <p class="text-gray-600 mb-4">Step-by-step guide to transitioning to a new industry, including how to reframe your experience and network effectively.</p>
                            <a href="#" class="text-blue-600 font-medium hover:text-blue-800 flex items-center">
                                Read More <i class="fas fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                    
                    <!-- Article 3 -->
                    <div class="article-card bg-white rounded-xl overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1624953587687-daf255b6b80a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="AI Interview" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <div class="flex items-center mb-3">
                                <span class="trending-badge bg-red-500 text-white text-xs font-bold px-3 py-1 rounded-full mr-3">TRENDING</span>
                                <span class="text-sm text-gray-500">May 20, 2023</span>
                            </div>
                            <h2 class="header-font text-xl font-bold mb-3">Preparing for AI-Powered Job Interviews</h2>
                            <p class="text-gray-600 mb-4">Many companies now use AI to screen candidates. Here's how to prepare for and succeed in these next-generation interviews.</p>
                            <a href="#" class="text-blue-600 font-medium hover:text-blue-800 flex items-center">
                                Read More <i class="fas fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                    
                    <!-- Article 4 -->
                    <div class="article-card bg-white rounded-xl overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Remote Work" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <div class="flex items-center mb-3">
                                <span class="text-sm text-gray-500">May 15, 2023</span>
                            </div>
                            <h2 class="header-font text-xl font-bold mb-3">Crafting the Perfect Remote Work Resume</h2>
                            <p class="text-gray-600 mb-4">Highlight the skills and experiences that matter most for remote positions with these targeted resume strategies.</p>
                            <a href="#" class="text-blue-600 font-medium hover:text-blue-800 flex items-center">
                                Read More <i class="fas fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                    
                    <!-- Article 5 -->
                    <div class="article-card bg-white rounded-xl overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1579389083078-4e7018379f7e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Tech Resume" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <div class="flex items-center mb-3">
                                <span class="bg-blue-100 text-blue-800 text-xs font-bold px-3 py-1 rounded-full mr-3">NEW</span>
                                <span class="text-sm text-gray-500">May 5, 2023</span>
                            </div>
                            <h2 class="header-font text-xl font-bold mb-3">Tech Resume Templates That Get Noticed</h2>
                            <p class="text-gray-600 mb-4">Specialized templates for software developers, data scientists, and other tech professionals looking to stand out.</p>
                            <a href="#" class="text-blue-600 font-medium hover:text-blue-800 flex items-center">
                                Read More <i class="fas fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                    
                    <!-- Article 6 -->
                    <div class="article-card bg-white rounded-xl overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1454165804606-c3aa57cac86a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="LinkedIn Profile" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <div class="flex items-center mb-3">
                                <span class="text-sm text-gray-500">April 28, 2023</span>
                            </div>
                            <h2 class="header-font text-xl font-bold mb-3">Syncing Your Resume and LinkedIn Profile</h2>
                            <p class="text-gray-600 mb-4">How to create consistency between your resume and LinkedIn profile to present a cohesive professional brand.</p>
                            <a href="#" class="text-blue-600 font-medium hover:text-blue-800 flex items-center">
                                Read More <i class="fas fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Pagination -->
                <div class="flex justify-center mt-12">
                    <nav class="flex items-center space-x-2">
                        <a href="#" class="px-4 py-2 border border-gray-300 rounded-lg text-gray-600 hover:bg-gray-100">
                            <i class="fas fa-chevron-left"></i>
                        </a>
                        <a href="#" class="px-4 py-2 bg-blue-600 text-white rounded-lg font-medium">1</a>
                        <a href="#" class="px-4 py-2 border border-gray-300 rounded-lg text-gray-600 hover:bg-gray-100">2</a>
                        <a href="#" class="px-4 py-2 border border-gray-300 rounded-lg text-gray-600 hover:bg-gray-100">3</a>
                        <span class="px-2 text-gray-500">...</span>
                        <a href="#" class="px-4 py-2 border border-gray-300 rounded-lg text-gray-600 hover:bg-gray-100">8</a>
                        <a href="#" class="px-4 py-2 border border-gray-300 rounded-lg text-gray-600 hover:bg-gray-100">
                            <i class="fas fa-chevron-right"></i>
                        </a>
                    </nav>
                </div>
            </div>
            
            <!-- Sidebar -->
            <div class="lg:w-1/3">
                <!-- About Widget -->
                <div class="bg-white rounded-xl p-6 mb-6 shadow-sm">
                    <h3 class="header-font text-xl font-bold mb-4 flex items-center">
                        <i class="fas fa-info-circle mr-2 text-blue-600"></i> About This Blog
                    </h3>
                    <p class="text-gray-600 mb-4">ResuCraftify's career blog provides expert advice on resume writing, job search strategies, and leveraging AI tools to advance your career.</p>
                    <div class="flex space-x-3">
                        <a href="#" class="text-blue-600 hover:text-blue-800">
                            <i class="fab fa-twitter text-xl"></i>
                        </a>
                        <a href="#" class="text-blue-600 hover:text-blue-800">
                            <i class="fab fa-linkedin text-xl"></i>
                        </a>
                        <a href="#" class="text-blue-600 hover:text-blue-800">
                            <i class="fab fa-facebook text-xl"></i>
                        </a>
                    </div>
                </div>
                
                <!-- Popular Articles -->
                <div class="bg-white rounded-xl p-6 mb-6 shadow-sm">
                    <h3 class="header-font text-xl font-bold mb-4 flex items-center">
                        <i class="fas fa-fire mr-2 text-red-500"></i> Popular Articles
                    </h3>
                    <div class="space-y-4">
                        <a href="#" class="flex group">
                            <div class="w-16 h-16 flex-shrink-0">
                                <img src="https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=200&q=80" alt="Resume Mistakes" class="w-full h-full object-cover rounded-lg">
                            </div>
                            <div class="ml-3">
                                <h4 class="font-medium group-hover:text-blue-600">5 Common Resume Mistakes That Cost You Interviews</h4>
                                <p class="text-sm text-gray-500">April 15, 2023</p>
                            </div>
                        </a>
                        <a href="#" class="flex group">
                            <div class="w-16 h-16 flex-shrink-0">
                                <img src="https://images.unsplash.com/photo-1563986768609-322da13575f3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=200&q=80" alt="AI Cover Letters" class="w-full h-full object-cover rounded-lg">
                            </div>
                            <div class="ml-3">
                                <h4 class="font-medium group-hover:text-blue-600">Using AI to Write Personalized Cover Letters</h4>
                                <p class="text-sm text-gray-500">March 28, 2023</p>
                            </div>
                        </a>
                        <a href="#" class="flex group">
                            <div class="w-16 h-16 flex-shrink-0">
                                <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=200&q=80" alt="Career Gap" class="w-full h-full object-cover rounded-lg">
                            </div>
                            <div class="ml-3">
                                <h4 class="font-medium group-hover:text-blue-600">How to Explain Employment Gaps on Your Resume</h4>
                                <p class="text-sm text-gray-500">March 10, 2023</p>
                            </div>
                        </a>
                    </div>
                </div>
                
                <!-- Newsletter -->
                <div class="bg-white rounded-xl p-6 shadow-sm">
                    <h3 class="header-font text-xl font-bold mb-4 flex items-center">
                        <i class="fas fa-envelope mr-2 text-blue-600"></i> Newsletter
                    </h3>
                    <p class="text-gray-600 mb-4">Get weekly career tips and resume advice straight to your inbox.</p>
                    <form>
                        <input type="email" placeholder="Your email address" class="w-full px-4 py-3 mb-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-400">
                        <button type="submit" class="w-full bg-blue-600 text-white py-3 rounded-lg font-medium hover:bg-blue-700 transition">
                            Subscribe Now
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <h3 class="header-font text-xl font-bold mb-4 flex items-center">
                        <i class="fas fa-pen-fancy mr-2"></i> ResuCraftify
                    </h3>
                    <p class="text-gray-400">Helping professionals create resumes that get results through expert advice and AI-powered tools.</p>
                </div>
                <div>
                    <h4 class="font-bold text-lg mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Home</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Resume Builder</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Templates</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Blog</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Pricing</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-bold text-lg mb-4">Resources</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Career Blog</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Resume Guide</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Cover Letter Tips</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Interview Prep</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">FAQ</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-bold text-lg mb-4">Contact</h4>
                    <ul class="space-y-2">
                        <li class="flex items-center">
                            <i class="fas fa-map-marker-alt mr-2 text-gray-400"></i>
                            <span class="text-gray-400">123 Career St, San Francisco</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-phone mr-2 text-gray-400"></i>
                            <span class="text-gray-400">(415) 555-0192</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope mr-2 text-gray-400"></i>
                            <span class="text-gray-400">hello@resucraftify.com</span>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-8 pt-8 text-center text-gray-400">
                <p>© 2023 ResuCraftify. All rights reserved.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Simple script for mobile menu toggle (would be expanded in a real implementation)
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('.md\\:hidden');
            // In a real implementation, this would toggle a mobile menu
            mobileMenuButton.addEventListener('click', function() {
                alert('Mobile menu would open here in a full implementation');
            });
            
            // Add animation to trending badges
            const trendingBadges = document.querySelectorAll('.trending-badge');
            trendingBadges.forEach(badge => {
                badge.style.animationDelay = `${Math.random() * 2}s`;
            });
        });
    </script>
</body>
</html>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

7th webpage code:-
------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meet the Team | ResuCraftify</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap');
        
        body {
            font-family: 'Montserrat', sans-serif;
        }
        
        .header-font {
            font-family: 'Playfair Display', serif;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #f97316 0%, #f59e0b 100%);
        }
        
        .team-card {
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }
        
        .team-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
        }
        
        .social-icon {
            transition: all 0.2s ease;
        }
        
        .social-icon:hover {
            transform: scale(1.2);
        }
        
        .expertise-tag {
            transition: all 0.2s ease;
        }
        
        .expertise-tag:hover {
            transform: translateY(-2px);
        }
        
        .team-photo {
            transition: all 0.3s ease;
        }
        
        .team-card:hover .team-photo {
            transform: scale(1.05);
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Navigation -->
    <nav class="bg-white shadow-sm">
        <div class="container mx-auto px-4 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-orange-600 flex items-center">
                <i class="fas fa-pen-fancy mr-2"></i> ResuCraftify
            </a>
            <div class="hidden md:flex space-x-8">
                <a href="#" class="text-gray-600 hover:text-orange-600">Home</a>
                <a href="#" class="text-gray-600 hover:text-orange-600">Blog</a>
                <a href="#" class="text-gray-600 hover:text-orange-600">Resume Builder</a>
                <a href="#" class="text-gray-600 hover:text-orange-600">Templates</a>
                <a href="#" class="text-orange-600 font-medium">About</a>
            </div>
            <div class="flex items-center space-x-4">
                <button class="md:hidden text-gray-600">
                    <i class="fas fa-bars text-xl"></i>
                </button>
                <button class="hidden md:block bg-orange-600 text-white px-4 py-2 rounded-lg hover:bg-orange-700 transition">
                    Get Started
                </button>
            </div>
        </div>
    </nav>
    
    <!-- Hero Section -->
    <div class="gradient-bg text-white">
        <div class="container mx-auto px-4 py-16 md:py-24">
            <div class="max-w-3xl mx-auto text-center">
                <h1 class="header-font text-4xl md:text-5xl font-bold mb-4">Meet the ResuCraftify Team</h1>
                <p class="text-xl mb-8 opacity-90">The passionate people behind the platform that's transforming how professionals craft their careers</p>
                <div class="flex justify-center space-x-4">
                    <a href="#developers" class="px-6 py-2 bg-white text-orange-600 rounded-full font-medium hover:bg-gray-100">Developers</a>
                    <a href="#mentors" class="px-6 py-2 border border-white rounded-full hover:bg-white hover:text-orange-600">Mentors</a>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Main Content -->
    <div class="container mx-auto px-4 py-12">
        <!-- Our Story -->
        <div class="max-w-4xl mx-auto text-center mb-16">
            <h2 class="header-font text-3xl font-bold mb-6">Our Story</h2>
            <p class="text-gray-600 text-lg mb-6">
                ResuCraftify began as a passion project between three friends who saw how difficult it was for professionals to create resumes that truly showcased their potential. What started as a simple tool has grown into a comprehensive platform combining AI technology with human expertise.
            </p>
            <p class="text-gray-600 text-lg">
                Today, our diverse team of developers, designers, and career experts work together to create innovative solutions that help people take control of their career narratives.
            </p>
        </div>
        
        <!-- Developers Section -->
        <div id="developers" class="mb-20">
            <h2 class="header-font text-3xl font-bold mb-8 text-center">Development Team</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Team Member 1 -->
                <div class="team-card bg-white rounded-xl overflow-hidden">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1560250097-0b93528c311a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Alex Chen" class="team-photo w-full h-full object-cover">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent to-transparent flex items-end p-6">
                            <div>
                                <h3 class="text-white text-2xl font-bold">Alex Chen</h3>
                                <p class="text-orange-300">Co-Founder & Lead Developer</p>
                            </div>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">AI Algorithms</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">Machine Learning</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">Python</span>
                        </div>
                        <p class="text-gray-600 mb-4">Alex architected our AI resume analysis system after seeing how applicant tracking systems filtered out qualified candidates. He's passionate about making technology work for job seekers.</p>
                        <div class="flex space-x-4">
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-linkedin text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-github text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-twitter text-xl"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Team Member 2 -->
                <div class="team-card bg-white rounded-xl overflow-hidden">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5cd?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Priya Patel" class="team-photo w-full h-full object-cover">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent to-transparent flex items-end p-6">
                            <div>
                                <h3 class="text-white text-2xl font-bold">Priya Patel</h3>
                                <p class="text-orange-300">Frontend Developer</p>
                            </div>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">React</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">UI/UX</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">JavaScript</span>
                        </div>
                        <p class="text-gray-600 mb-4">Priya crafts the beautiful, intuitive interfaces that make ResuCraftify a joy to use. She's obsessed with creating seamless user experiences that remove friction from resume building.</p>
                        <div class="flex space-x-4">
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-linkedin text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-dribbble text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-twitter text-xl"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Team Member 3 -->
                <div class="team-card bg-white rounded-xl overflow-hidden">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Jamal Wilson" class="team-photo w-full h-full object-cover">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent to-transparent flex items-end p-6">
                            <div>
                                <h3 class="text-white text-2xl font-bold">Jamal Wilson</h3>
                                <p class="text-orange-300">Backend Developer</p>
                            </div>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">Node.js</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">Database</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">API</span>
                        </div>
                        <p class="text-gray-600 mb-4">Jamal builds the robust systems that power our platform. With a background in HR tech, he understands exactly what data needs to flow where to create the best results.</p>
                        <div class="flex space-x-4">
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-linkedin text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-github text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-dev text-xl"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Team Member 4 -->
                <div class="team-card bg-white rounded-xl overflow-hidden">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Sophia Rodriguez" class="team-photo w-full h-full object-cover">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent to-transparent flex items-end p-6">
                            <div>
                                <h3 class="text-white text-2xl font-bold">Sophia Rodriguez</h3>
                                <p class="text-orange-300">UX Designer</p>
                            </div>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">User Research</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">Prototyping</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">Accessibility</span>
                        </div>
                        <p class="text-gray-600 mb-4">Sophia ensures our platform is intuitive and accessible to everyone. Her background in career counseling gives her unique insight into user needs during job searches.</p>
                        <div class="flex space-x-4">
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-linkedin text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-behance text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-medium text-xl"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Team Member 5 -->
                <div class="team-card bg-white rounded-xl overflow-hidden">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1544725176-7c40e5a71c5e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="David Kim" class="team-photo w-full h-full object-cover">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent to-transparent flex items-end p-6">
                            <div>
                                <h3 class="text-white text-2xl font-bold">David Kim</h3>
                                <p class="text-orange-300">Mobile Developer</p>
                            </div>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">Flutter</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">iOS</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">Android</span>
                        </div>
                        <p class="text-gray-600 mb-4">David leads our mobile development, ensuring ResuCraftify works flawlessly on any device. He's passionate about helping users craft resumes on-the-go.</p>
                        <div class="flex space-x-4">
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-linkedin text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-github text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-apple text-xl"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Team Member 6 -->
                <div class="team-card bg-white rounded-xl overflow-hidden">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Emma Zhang" class="team-photo w-full h-full object-cover">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent to-transparent flex items-end p-6">
                            <div>
                                <h3 class="text-white text-2xl font-bold">Emma Zhang</h3>
                                <p class="text-orange-300">QA Engineer</p>
                            </div>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">Testing</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">Automation</span>
                            <span class="expertise-tag bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-xs font-medium">Security</span>
                        </div>
                        <p class="text-gray-600 mb-4">Emma ensures every feature works perfectly before it reaches you. Her meticulous attention to detail means you can trust ResuCraftify with your important career documents.</p>
                        <div class="flex space-x-4">
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-linkedin text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fab fa-github text-xl"></i>
                            </a>
                            <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                                <i class="fas fa-bug text-xl"></i>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Mentors Section -->
        <div id="mentors" class="mb-12">
            <h2 class="header-font text-3xl font-bold mb-8 text-center">Our Career Mentors</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Mentor 1 -->
                <div class="team-card bg-white rounded-xl overflow-hidden text-center p-6">
                    <div class="w-32 h-32 mx-auto mb-4 rounded-full overflow-hidden border-4 border-orange-100">
                        <img src="https://images.unsplash.com/photo-1573497019940-1c28c88b4f3e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Dr. Rebecca Miller" class="w-full h-full object-cover">
                    </div>
                    <h3 class="text-xl font-bold mb-1">Dr. Rebecca Miller</h3>
                    <p class="text-orange-600 text-sm mb-3">Career Strategist</p>
                    <p class="text-gray-600 text-sm mb-4">Former Fortune 500 HR Director with 20+ years experience in executive hiring and career coaching.</p>
                    <div class="flex justify-center space-x-3">
                        <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                            <i class="fab fa-linkedin text-lg"></i>
                        </a>
                        <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                            <i class="fas fa-globe text-lg"></i>
                        </a>
                    </div>
                </div>
                
                <!-- Mentor 2 -->
                <div class="team-card bg-white rounded-xl overflow-hidden text-center p-6">
                    <div class="w-32 h-32 mx-auto mb-4 rounded-full overflow-hidden border-4 border-orange-100">
                        <img src="https://images.unsplash.com/photo-1560250097-0b93528c311a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Marcus Johnson" class="w-full h-full object-cover">
                    </div>
                    <h3 class="text-xl font-bold mb-1">Marcus Johnson</h3>
                    <p class="text-orange-600 text-sm mb-3">Tech Recruiter</p>
                    <p class="text-gray-600 text-sm mb-4">Specializes in helping tech professionals craft resumes that appeal to both hiring managers and ATS systems.</p>
                    <div class="flex justify-center space-x-3">
                        <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                            <i class="fab fa-linkedin text-lg"></i>
                        </a>
                        <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                            <i class="fab fa-twitter text-lg"></i>
                        </a>
                    </div>
                </div>
                
                <!-- Mentor 3 -->
                <div class="team-card bg-white rounded-xl overflow-hidden text-center p-6">
                    <div class="w-32 h-32 mx-auto mb-4 rounded-full overflow-hidden border-4 border-orange-100">
                        <img src="https://images.unsplash.com/photo-1542190891-2093d38760de?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Sarah Chen" class="w-full h-full object-cover">
                    </div>
                    <h3 class="text-xl font-bold mb-1">Sarah Chen</h3>
                    <p class="text-orange-600 text-sm mb-3">Career Transition Coach</p>
                    <p class="text-gray-600 text-sm mb-4">Helps professionals successfully pivot careers with targeted resume strategies and networking approaches.</p>
                    <div class="flex justify-center space-x-3">
                        <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                            <i class="fab fa-linkedin text-lg"></i>
                        </a>
                        <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                            <i class="fas fa-podcast text-lg"></i>
                        </a>
                    </div>
                </div>
                
                <!-- Mentor 4 -->
                <div class="team-card bg-white rounded-xl overflow-hidden text-center p-6">
                    <div class="w-32 h-32 mx-auto mb-4 rounded-full overflow-hidden border-4 border-orange-100">
                        <img src="https://images.unsplash.com/photo-1551836022-d5d88e9218df?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="James Wilson" class="w-full h-full object-cover">
                    </div>
                    <h3 class="text-xl font-bold mb-1">James Wilson</h3>
                    <p class="text-orange-600 text-sm mb-3">Executive Resume Writer</p>
                    <p class="text-gray-600 text-sm mb-4">Crafts compelling executive narratives that highlight leadership achievements and strategic impact.</p>
                    <div class="flex justify-center space-x-3">
                        <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                            <i class="fab fa-linkedin text-lg"></i>
                        </a>
                        <a href="#" class="social-icon text-gray-500 hover:text-orange-600">
                            <i class="fas fa-book text-lg"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Join Team CTA -->
        <div class="bg-orange-50 rounded-xl p-8 md:p-12 text-center max-w-4xl mx-auto">
            <h2 class="header-font text-3xl font-bold mb-4">Want to Join Our Team?</h2>
            <p class="text-gray-600 mb-6">We're always looking for talented, passionate people to help us build the future of career development tools.</p>
            <button class="bg-orange-600 text-white px-8 py-3 rounded-lg font-medium hover:bg-orange-700 transition">
                View Open Positions
            </button>
        </div>
    </div>
    
    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <h3 class="header-font text-xl font-bold mb-4 flex items-center">
                        <i class="fas fa-pen-fancy mr-2"></i> ResuCraftify
                    </h3>
                    <p class="text-gray-400">Helping professionals create resumes that get results through expert advice and AI-powered tools.</p>
                </div>
                <div>
                    <h4 class="font-bold text-lg mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Home</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Resume Builder</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Templates</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Blog</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Pricing</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-bold text-lg mb-4">Resources</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Career Blog</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Resume Guide</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Cover Letter Tips</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Interview Prep</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">FAQ</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-bold text-lg mb-4">Contact</h4>
                    <ul class="space-y-2">
                        <li class="flex items-center">
                            <i class="fas fa-map-marker-alt mr-2 text-gray-400"></i>
                            <span class="text-gray-400">123 Career St, San Francisco</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-phone mr-2 text-gray-400"></i>
                            <span class="text-gray-400">(415) 555-0192</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope mr-2 text-gray-400"></i>
                            <span class="text-gray-400">hello@resucraftify.com</span>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-8 pt-8 text-center text-gray-400">
                <p>© 2023 ResuCraftify. All rights reserved.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Simple script for mobile menu toggle (would be expanded in a real implementation)
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('.md\\:hidden');
            // In a real implementation, this would toggle a mobile menu
            mobileMenuButton.addEventListener('click', function() {
                alert('Mobile menu would open here in a full implementation');
            });
            
            // Add hover effects to team cards
            const teamCards = document.querySelectorAll('.team-card');
            teamCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.querySelector('.team-photo').style.transform = 'scale(1.05)';
                });
                card.addEventListener('mouseleave', function() {
                    this.querySelector('.team-photo').style.transform = 'scale(1)';
                });
            });
        });
    </script>
</body>
</html>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

8th webpage code:-
------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ResuCraftify - Footer</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .footer-divider {
            border-color: rgba(255,255,255,0.1);
        }
        .subscribe-input {
            background: rgba(255,255,255,0.05);
            transition: all 0.3s ease;
        }
        .subscribe-input:focus {
            background: rgba(255,255,255,0.1);
            outline: none;
        }
        .social-icon {
            transition: all 0.3s ease;
        }
        .social-icon:hover {
            transform: translateY(-2px);
            color: #f97316;
        }
        .footer-link {
            position: relative;
        }
        .footer-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 1px;
            bottom: 0;
            left: 0;
            background-color: #f97316;
            transition: width 0.3s ease;
        }
        .footer-link:hover:after {
            width: 100%;
        }
    </style>
</head>
<body>
    <!-- Footer Section -->
    <footer class="bg-gray-900 text-gray-300 pt-16 pb-8">
        <div class="container mx-auto px-6">
            <!-- Main Footer Content -->
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-12">
                <!-- Brand Column -->
                <div class="md:col-span-1">
                    <div class="flex items-center mb-4">
                        <i class="fas fa-pen-fancy text-2xl text-orange-500 mr-2"></i>
                        <span class="text-xl font-bold text-white">ResuCraftify</span>
                    </div>
                    <p class="mb-4 text-gray-400">Crafting career success stories through powerful resumes and professional guidance.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="social-icon text-gray-400 hover:text-white">
                            <i class="fab fa-linkedin-in text-lg"></i>
                        </a>
                        <a href="#" class="social-icon text-gray-400 hover:text-white">
                            <i class="fab fa-twitter text-lg"></i>
                        </a>
                        <a href="#" class="social-icon text-gray-400 hover:text-white">
                            <i class="fab fa-facebook-f text-lg"></i>
                        </a>
                        <a href="#" class="social-icon text-gray-400 hover:text-white">
                            <i class="fab fa-instagram text-lg"></i>
                        </a>
                    </div>
                </div>

                <!-- Quick Links -->
                <div>
                    <h4 class="text-white font-semibold mb-4 text-lg">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="footer-link text-gray-400 hover:text-white pb-1">Home</a></li>
                        <li><a href="#" class="footer-link text-gray-400 hover:text-white pb-1">About Us</a></li>
                        <li><a href="#" class="footer-link text-gray-400 hover:text-white pb-1">Resume Builder</a></li>
                        <li><a href="#" class="footer-link text-gray-400 hover:text-white pb-1">Cover Letters</a></li>
                        <li><a href="#" class="footer-link text-gray-400 hover:text-white pb-1">Templates</a></li>
                    </ul>
                </div>

                <!-- Company -->
                <div>
                    <h4 class="text-white font-semibold mb-4 text-lg">Company</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="footer-link text-gray-400 hover:text-white pb-1">Our Team</a></li>
                        <li><a href="#" class="footer-link text-gray-400 hover:text-white pb-1">Careers</a></li>
                        <li><a href="#" class="footer-link text-gray-400 hover:text-white pb-1">Blog</a></li>
                        <li><a href="#" class="footer-link text-gray-400 hover:text-white pb-1">Press</a></li>
                        <li><a href="#" class="footer-link text-gray-400 hover:text-white pb-1">Partners</a></li>
                    </ul>
                </div>

                <!-- Contact & Subscribe -->
                <div>
                    <h4 class="text-white font-semibold mb-4 text-lg">Stay Updated</h4>
                    <div class="mb-6">
                        <div class="flex items-center mb-2">
                            <i class="fas fa-map-marker-alt text-orange-500 mr-3"></i>
                            <span class="text-gray-400">123 Career Lane, San Francisco, CA</span>
                        </div>
                        <div class="flex items-center mb-2">
                            <i class="fas fa-envelope text-orange-500 mr-3"></i>
                            <span class="text-gray-400">hello@resucraftify.com</span>
                        </div>
                        <div class="flex items-center">
                            <i class="fas fa-phone-alt text-orange-500 mr-3"></i>
                            <span class="text-gray-400">(415) 555-0192</span>
                        </div>
                    </div>
                    
                    <div class="relative">
                        <input type="email" placeholder="Your email" class="subscribe-input w-full px-4 py-3 rounded-lg text-white placeholder-gray-500 border border-gray-700 focus:border-orange-500">
                        <button class="absolute right-2 top-1/2 transform -translate-y-1/2 bg-orange-500 text-white p-1 rounded-md hover:bg-orange-600">
                            <i class="fas fa-paper-plane"></i>
                        </button>
                    </div>
                    <p class="text-xs text-gray-500 mt-2">Subscribe for tips and updates</p>
                </div>
            </div>

            <!-- Divider -->
            <div class="footer-divider border-t border-gray-800 mb-8"></div>

            <!-- Bottom Footer -->
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="text-sm text-gray-500 mb-4 md:mb-0">
                    © 2023 ResuCraftify. All rights reserved.
                </div>
                <div class="flex space-x-6">
                    <a href="#" class="text-sm text-gray-400 hover:text-white">Privacy Policy</a>
                    <a href="#" class="text-sm text-gray-400 hover:text-white">Terms of Service</a>
                    <a href="#" class="text-sm text-gray-400 hover:text-white">Cookie Policy</a>
                    <a href="#" class="text-sm text-gray-400 hover:text-white">Feedback</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Simple script for the subscribe button (would be expanded in a real implementation)
        document.addEventListener('DOMContentLoaded', function() {
            const subscribeBtn = document.querySelector('.fa-paper-plane').parentElement;
            subscribeBtn.addEventListener('click', function() {
                const emailInput = document.querySelector('input[type="email"]');
                if(emailInput.value.includes('@')) {
                    alert('Thanks for subscribing! Career tips coming your way soon.');
                    emailInput.value = '';
                } else {
                    alert('Please enter a valid email address');
                }
            });
        });
    </script>
</body>
</html>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
