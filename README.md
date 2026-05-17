<html lang="en"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AGMTV Sri Lanka - Grand Opening</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome -->
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet">
    <!-- Tailwind Configuration -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#1a56db',
                        secondary: '#ff6b00',
                        accent: '#ffd700',
                        dark: '#0f172a',
                        light: '#f8fafc'
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    animation: {
                        'bounce-slow': 'bounce 3s infinite',
                        'spin-slow': 'spin 3s linear infinite',
                    }
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .text-shadow {
                text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            }
            .text-gradient {
                background-clip: text;
                -webkit-background-clip: text;
                color: transparent;
                background-image: linear-gradient(to right, #1a56db, #ff6b00);
            }
            .bg-pattern {
                background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%239C92AC' fill-opacity='0.05'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
            }
        }
    </style>
    <style>
        /* Custom animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .float-animation {
            animation: float 3s ease-in-out infinite;
        }
        
        /* Countdown timer */
        .countdown-item {
            position: relative;
        }
        
        .countdown-item:not(:last-child)::after {
            content: ':';
            position: absolute;
            right: -10px;
            top: 50%;
            transform: translateY(-50%);
            font-size: 2rem;
            font-weight: bold;
            color: #1a56db;
        }
        
        /* Gift box animation */
        .gift-box {
            transition: all 0.3s ease;
        }
        
        .gift-box:hover {
            transform: translateY(-5px) scale(1.05);
        }
        
        /* Celebration animation */
        .celebration {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: #f00;
            border-radius: 50%;
            animation: celebration-fall 3s ease-in-out infinite;
        }
        
        @keyframes celebration-fall {
            0% {
                transform: translateY(-100vh) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(100vh) rotate(360deg);
                opacity: 0;
            }
        }
    </style>
</head>
<body class="bg-light bg-pattern min-h-screen">
    <!-- Language Selector -->
    <div class="fixed top-4 right-4 z-50 bg-white rounded-full shadow-lg p-2 flex items-center space-x-2">
        <button id="lang-en" class="lang-btn p-2 rounded-full bg-primary text-white">EN</button>
    </div>

    <!-- Hero Section -->
    <header class="relative overflow-hidden">
        <!-- Background Pattern -->
        <div class="absolute inset-0 bg-gradient-to-br from-primary/10 to-secondary/10 z-0"></div>
        
        <!-- Celebration Effect -->
        <div id="celebration-container" class="absolute inset-0 overflow-hidden pointer-events-none"></div>
        
        <!-- Logo -->
        <div class="container mx-auto px-4 pt-8 pb-4 relative z-10">
            <div class="flex justify-center">
                <img src="https://p26-flow-imagex-sign.byteimg.com/tos-cn-i-a9rns2rl98/rc/pc/code_assistant/1434c061466149da9e2175b0b70c99d8~tplv-a9rns2rl98-image.image?lk3s=8e244e95&amp;rcl=20260518010702099E9EDA6B8F115287BC&amp;rrcfp=e75484ac&amp;x-expires=1779642423&amp;x-signature=3oKKHS2aFChJkPEanoHXNhzvFjc%3D" alt="AGMTV Logo" class="w-48 md:w-64 lg:w-72 object-contain drop-shadow-lg" style="border-width: medium; border-style: none; border-color: currentcolor; border-image: initial;">
            </div>
        </div>
        
        <div class="container mx-auto px-4 py-8 md:py-16 relative z-10">
            <div class="flex flex-col md:flex-row items-center justify-between">
                <div class="md:w-1/2 text-center md:text-left mb-8 md:mb-0">
                    <h1 class="text-4xl md:text-6xl font-bold mb-4 text-gradient">
                        <span class="lang" data-lang="en">Grand Opening</span>
                    </h1>
                    <h2 class="text-2xl md:text-3xl font-semibold mb-6 text-dark">
                        <span class="lang" data-lang="en">Matara District</span>
                    </h2>
                    <p class="text-lg mb-8 max-w-lg mx-auto md:mx-0">
                        <span class="lang" data-lang="en">Join us for the grand opening of AGMTV Sri Lanka's new office in Matara District. Celebrate with us and win exciting prizes!</span>
                    </p>
                    <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
                        <a href="#details" class="btn-primary bg-primary hover:bg-primary/90 text-white font-medium py-3 px-6 rounded-full transition-all transform hover:scale-105 shadow-lg">
                            <span class="lang" data-lang="en">Learn More</span>
                        </a>
                        <a href="#benefits" class="btn-secondary bg-secondary hover:bg-secondary/90 text-white font-medium py-3 px-6 rounded-full transition-all transform hover:scale-105 shadow-lg">
                            <span class="lang" data-lang="en">View Benefits</span>
                        </a>
                    </div>
                </div>
                <div class="md:w-1/2 flex justify-center">
                    <div class="relative w-full max-w-md">
                        <div class="bg-white rounded-2xl shadow-2xl p-8 float-animation">
                            <div class="text-center mb-6">
                                <h3 class="text-xl font-bold text-primary mb-2">
                                    <span class="lang" data-lang="en">Event Countdown</span>
                                </h3>
                                <div id="countdown" class="flex justify-center space-x-4 md:space-x-8 mt-4">
                                    <div class="countdown-item">
                                        <div id="days" class="text-3xl md:text-4xl font-bold text-primary">00</div>
                                        <div class="text-sm text-gray-600">
                                            <span class="lang" data-lang="en">Days</span>
                                        </div>
                                    </div>
                                    <div class="countdown-item">
                                        <div id="hours" class="text-3xl md:text-4xl font-bold text-primary">00</div>
                                        <div class="text-sm text-gray-600">
                                            <span class="lang" data-lang="en">Hours</span>
                                        </div>
                                    </div>
                                    <div class="countdown-item">
                                        <div id="minutes" class="text-3xl md:text-4xl font-bold text-primary">00</div>
                                        <div class="text-sm text-gray-600">
                                            <span class="lang" data-lang="en">Minutes</span>
                                        </div>
                                    </div>
                                    <div class="countdown-item">
                                        <div id="seconds" class="text-3xl md:text-4xl font-bold text-primary">00</div>
                                        <div class="text-sm text-gray-600">
                                            <span class="lang" data-lang="en">Seconds</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="bg-primary/5 rounded-xl p-4">
                                <div class="flex items-center mb-3">
                                    <i class="fa fa-calendar text-primary mr-3"></i>
                                    <div>
                                        <div class="text-sm text-gray-500">
                                            <span class="lang" data-lang="en">Date</span>
                                        </div>
                                        <div class="font-medium">May 19, 2026</div>
                                    </div>
                                </div>
                                <div class="flex items-center mb-3">
                                    <i class="fa fa-clock-o text-primary mr-3"></i>
                                    <div>
                                        <div class="text-sm text-gray-500">
                                            <span class="lang" data-lang="en">Time</span>
                                        </div>
                                        <div class="font-medium">10:30 AM</div>
                                    </div>
                                </div>
                                <div class="flex items-start">
                                    <i class="fa fa-map-marker text-primary mr-3 mt-1"></i>
                                    <div>
                                        <div class="text-sm text-gray-500">
                                            <span class="lang" data-lang="en">Location</span>
                                        </div>
                                        <div class="font-medium">Sadan Sewana, Beliaththa Road, Dematapitiya, Walasgala</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <!-- Decorative Elements -->
                        <div class="absolute -top-4 -right-4 w-16 h-16 bg-accent rounded-full flex items-center justify-center transform rotate-12 shadow-lg">
                            <i class="fa fa-star text-white text-2xl"></i>
                        </div>
                        <div class="absolute -bottom-4 -left-4 w-12 h-12 bg-secondary rounded-full flex items-center justify-center transform -rotate-12 shadow-lg">
                            <i class="fa fa-gift text-white text-xl"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Invitation Section -->
    <section id="details" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="max-w-3xl mx-auto bg-gradient-to-br from-primary/5 to-secondary/5 rounded-2xl p-8 shadow-lg border border-gray-100">
                <h2 class="text-3xl font-bold text-center mb-6 text-gradient">
                    <span class="lang" data-lang="en">Official Invitation</span>
                </h2>
                <div class="prose max-w-none">
                    <p class="mb-4">
                        <span class="lang" data-lang="en">Dear Sir/Madam:</span>
                    </p>
                    <p class="mb-4">
                        <span class="lang" data-lang="en">We sincerely thank you for your continued trust and support of AGMTV Sri Lanka. Our AGMTV office at the following address has been steadily expanding: Sadan Sewana, Beliaththa Road, Dematapitiya, Walasgala. To further strengthen communication and cooperation, we cordially invite you to visit our office, rekindle our friendship, and discuss future prospects together.</span>
                    </p>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 my-6">
                        <div class="flex items-center">
                            <i class="fa fa-calendar text-primary mr-3 text-xl"></i>
                            <div>
                                <div class="text-sm text-gray-500">
                                    <span class="lang" data-lang="en">Date</span>
                                </div>
                                <div class="font-medium">May 19, 2026</div>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <i class="fa fa-clock-o text-primary mr-3 text-xl"></i>
                            <div>
                                <div class="text-sm text-gray-500">
                                    <span class="lang" data-lang="en">Time</span>
                                </div>
                                <div class="font-medium">10:30 AM</div>
                            </div>
                        </div>
                        <div class="flex items-start md:col-span-2">
                            <i class="fa fa-map-marker text-primary mr-3 mt-1 text-xl"></i>
                            <div>
                                <div class="text-sm text-gray-500">
                                    <span class="lang" data-lang="en">Location</span>
                                </div>
                                <div class="font-medium">Sadan Sewana, Beliaththa Road, Dematapitiya, Walasgala</div>
                            </div>
                        </div>
                    </div>
                    <p class="mb-4">
                        <span class="lang" data-lang="en">Office Manager: Tarindu Timira</span>
                    </p>
                    <p>
                        <span class="lang" data-lang="en">We look forward to your visit.</span>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Benefits Section -->
    <section id="benefits" class="py-16 bg-gradient-to-br from-primary/5 to-secondary/5">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 text-gradient">
                <span class="lang" data-lang="en">Exciting Benefits</span>
            </h2>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Benefit 1 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden gift-box">
                    <div class="bg-primary text-white p-4">
                        <div class="flex justify-between items-center">
                            <h3 class="text-xl font-bold">
                                <span class="lang" data-lang="en">Benefits for full-time employees</span>
                            </h3>
                            <span class="bg-accent text-primary font-bold py-1 px-3 rounded-full">
                                <span class="lang" data-lang="en">Level K</span>
                            </span>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-center mb-6">
                            <div class="w-24 h-24 bg-gradient-to-br from-primary/20 to-primary/5 rounded-full flex items-center justify-center transform transition-all duration-500 hover:scale-110 hover:rotate-y-180 shadow-lg relative group">
                                <div class="absolute inset-0 bg-gradient-to-br from-primary/30 to-primary/10 rounded-full transform transition-all duration-500 group-hover:scale-95"></div>
                                <i class="fa fa-diamond text-primary text-5xl relative z-10 transform transition-all duration-500 group-hover:scale-110"></i>
                                <div class="absolute inset-0 rounded-full bg-primary/20 blur-sm opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                            </div>
                        </div>
                        <div class="text-center mb-4">
                            <span class="text-2xl font-bold text-primary">RS 5000</span>
                            <span class="text-gray-600 ml-1">
                                <span class="lang" data-lang="en">Cash</span>
                            </span>
                        </div>
                        <ul class="space-y-3 text-gray-700">
                            <li class="flex items-start">
                                <i class="fa fa-check-circle text-green-500 mt-1 mr-2"></i>
                                <span>
                                    <span class="lang" data-lang="en">For Level K members who joined before May 17th</span>
                                </span>
                            </li>
                            <li class="flex items-start">
                                <i class="fa fa-check-circle text-green-500 mt-1 mr-2"></i>
                                <span>
                                    <span class="lang" data-lang="en">Attend the opening ceremony on May 19th</span>
                                </span>
                            </li>
                            <li class="flex items-start">
                                <i class="fa fa-check-circle text-green-500 mt-1 mr-2"></i>
                                <span>
                                    <span class="lang" data-lang="en">Take 3-5 photos on-site and share to WhatsApp &amp; Telegram</span>
                                </span>
                            </li>
                        </ul>
                        <div class="mt-6 pt-4 border-t border-gray-200">
                            <p class="text-sm text-gray-500">
                                <i class="fa fa-info-circle mr-1"></i>
                                <span class="lang" data-lang="en">Reward will be credited within 1-3 business days</span>
                            </p>
                        </div>
                    </div>
                </div>
                
                <!-- Benefit 2 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden gift-box">
                    <div class="bg-secondary text-white p-4">
                        <h3 class="text-xl font-bold">
                            <span class="lang" data-lang="en">Newcomer Welcome Gift</span>
                        </h3>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-center mb-6">
                            <div class="w-24 h-24 bg-gradient-to-br from-secondary/20 to-secondary/5 rounded-full flex items-center justify-center transform transition-all duration-500 hover:scale-110 hover:rotate-y-180 shadow-lg relative group">
                                <div class="absolute inset-0 bg-gradient-to-br from-secondary/30 to-secondary/10 rounded-full transform transition-all duration-500 group-hover:scale-95"></div>
                                <i class="fa fa-star text-secondary text-5xl relative z-10 transform transition-all duration-500 group-hover:scale-110"></i>
                                <div class="absolute inset-0 rounded-full bg-secondary/20 blur-sm opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                            </div>
                        </div>
                        <div class="text-center mb-4">
                            <span class="text-2xl font-bold text-secondary">RS 500</span>
                            <span class="text-gray-600 ml-1">
                                <span class="lang" data-lang="en">Cash</span>
                            </span>
                        </div>
                        <ul class="space-y-3 text-gray-700">
                            <li class="flex items-start">
                                <i class="fa fa-check-circle text-green-500 mt-1 mr-2"></i>
                                <span>
                                    <span class="lang" data-lang="en">For new employees attending on opening day</span>
                                </span>
                            </li>
                            <li class="flex items-start">
                                <i class="fa fa-check-circle text-green-500 mt-1 mr-2"></i>
                                <span>
                                    <span class="lang" data-lang="en">Register an AGMTV work account on-site</span>
                                </span>
                            </li>
                            <li class="flex items-start">
                                <i class="fa fa-check-circle text-green-500 mt-1 mr-2"></i>
                                <span>
                                    <span class="lang" data-lang="en">Become an intern to claim your reward</span>
                                </span>
                            </li>
                        </ul>
                        <div class="mt-6 pt-4 border-t border-gray-200">
                            <p class="text-sm text-gray-500">
                                <i class="fa fa-info-circle mr-1"></i>
                                <span class="lang" data-lang="en">Contact Recruiting Manager to claim</span>
                            </p>
                        </div>
                    </div>
                </div>
                
                <!-- Benefit 3 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden gift-box">
                    <div class="bg-accent text-primary p-4">
                        <h3 class="text-xl font-bold">
                            <span class="lang" data-lang="en">Career Promotion Lucky Draw</span>
                        </h3>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-center mb-6">
                            <div class="w-24 h-24 bg-gradient-to-br from-accent/20 to-accent/5 rounded-full flex items-center justify-center transform transition-all duration-500 hover:scale-110 hover:rotate-y-180 shadow-lg relative group">
                                <div class="absolute inset-0 bg-gradient-to-br from-accent/30 to-accent/10 rounded-full transform transition-all duration-500 group-hover:scale-95"></div>
                                <i class="fa fa-certificate text-accent text-5xl relative z-10 transform transition-all duration-500 group-hover:scale-110"></i>
                                <div class="absolute inset-0 rounded-full bg-accent/20 blur-sm opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                            </div>
                        </div>
                        <div class="text-center mb-4">
                            <span class="text-2xl font-bold text-accent">
                                <span class="lang" data-lang="en">Lucky Wheel Draw</span>
                            </span>
                        </div>
                        <ul class="space-y-3 text-gray-700">
                            <li class="flex items-start">
                                <i class="fa fa-check-circle text-green-500 mt-1 mr-2"></i>
                                <span>
                                    <span class="lang" data-lang="en">Intern to K1: 1 Lucky Wheel Draw chance</span>
                                </span>
                            </li>
                            <li class="flex items-start">
                                <i class="fa fa-check-circle text-green-500 mt-1 mr-2"></i>
                                <span>
                                    <span class="lang" data-lang="en">Intern to K2: 2 Lucky Wheel Draw chances</span>
                                </span>
                            </li>
                            <li class="flex items-start">
                                <i class="fa fa-check-circle text-green-500 mt-1 mr-2"></i>
                                <span>
                                    <span class="lang" data-lang="en">Complete promotion on opening day to double your luck</span>
                                </span>
                            </li>
                        </ul>
                        <div class="mt-6 pt-4 border-t border-gray-200">
                            <p class="text-sm text-gray-500">
                                <i class="fa fa-info-circle mr-1"></i>
                                <span class="lang" data-lang="en">Contact Recruiting Manager after promotion</span>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Map Section -->
    <section id="location" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 text-gradient">
                <span class="lang" data-lang="en">Event Location</span>
            </h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                <div class="bg-gray-100 rounded-xl overflow-hidden h-96 relative">
                    <!-- Map Placeholder -->
                    <div class="absolute inset-0 bg-gray-200 overflow-hidden">
                        <div class="w-full h-full relative">
                            <!-- Team Image Background -->
                            <img src="https://p3-flow-imagex-sign.byteimg.com/tos-cn-i-a9rns2rl98/rc/pc/code_assistant/fa62bd2c72e546378dd182245aa878a9~tplv-a9rns2rl98-image.image?lk3s=8e244e95&amp;rcl=202605172344184313C98F30C8DD9D0E9F&amp;rrcfp=e75484ac&amp;x-expires=1779637463&amp;x-signature=Af396KA%2BCA%2FgSHxWQ%2FlpB4FTfhw%3D" alt="AGMTV Team" class="w-full h-full object-cover transform transition-transform duration-700 hover:scale-105">
                            
                            <!-- Overlay with Team Information -->
                            <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/30 to-transparent flex flex-col justify-end p-6">
                                <h3 class="text-2xl font-bold text-white mb-2">Our Team</h3>
                                <p class="text-gray-200 mb-4 max-w-md">Meet our dedicated professionals who are ready to welcome you to our new Matara District office.</p>
                                <div class="flex flex-wrap gap-3">
                                    <div class="bg-white/20 backdrop-blur-sm rounded-full px-4 py-1 text-white text-sm">Tarindu Timira - Office Manager</div>
                                    <div class="bg-white/20 backdrop-blur-sm rounded-full px-4 py-1 text-white text-sm">
</div>
                                    <div class="bg-white/20 backdrop-blur-sm rounded-full px-4 py-1 text-white text-sm">
</div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!-- In a real implementation, you would embed a Google Map here -->
                    <div class="w-full h-full bg-gray-200 flex items-center justify-center">
                        <div class="text-center">
                            <i class="fa fa-map-marker text-primary text-5xl mb-4"></i>
                            <p class="text-lg font-medium text-gray-700">Sadan Sewana, Beliaththa Road</p>
                            <p class="text-gray-600">Dematapitiya, Walasgala</p>
                        </div>
                    </div>
                </div>
                
                <div>
                    <h3 class="text-2xl font-bold mb-4 text-primary">
                        <span class="lang" data-lang="en">Sadan Sewana</span>
                    </h3>
                    <p class="text-gray-700 mb-6">
                        <span class="lang" data-lang="en">Our new office is located in the heart of Matara District, easily accessible from all major towns in the region. Join us for the grand opening celebration and explore our modern facilities.</span>
                    </p>
                    
                    <div class="space-y-4">
                        <div class="flex items-start">
                            <div class="bg-primary/10 p-2 rounded-full mr-4">
                                <i class="fa fa-map-marker text-primary"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold text-gray-900">
                                    <span class="lang" data-lang="en">Full Address</span>
                                </h4>
                                <p class="text-gray-600">Sadan Sewana, Beliaththa Road, Dematapitiya, Walasgala</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-primary/10 p-2 rounded-full mr-4">
                                <i class="fa fa-clock-o text-primary"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold text-gray-900">
                                    <span class="lang" data-lang="en">Event Time</span>
                                </h4>
                                <p class="text-gray-600">May 19, 2026 | 10:30 AM</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-primary/10 p-2 rounded-full mr-4">
                                <i class="fa fa-user text-primary"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold text-gray-900">
                                    <span class="lang" data-lang="en">Contact</span>
                                </h4>
                                <p class="text-gray-600">Tarindu Timira (Office Manager)</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark text-white py-12">
        <div class="container mx-auto px-4">
            
            <div class="border-t border-gray-800 mt-8 pt-8 text-center text-gray-500">
                <div class="mb-4">
                    <a href="https://agmtv-lk68.com/xml/index.html#/" class="inline-block bg-gradient-to-r from-primary to-blue-600 text-white font-bold py-3 px-6 rounded-full transform transition-all duration-300 hover:scale-105 hover:shadow-lg hover:shadow-blue-500/30 hover:-translate-y-1">
                        <span class="relative z-10">AGMTV Sri Lanka subsidiary official website</span>
                        <span class="absolute inset-0 bg-gradient-to-r from-blue-600 to-primary rounded-full opacity-0 hover:opacity-100 transition-opacity duration-300"></span>
                    </a>
                </div>
                <p>© 2026 AGMTV Sri Lanka. All rights reserved.</p>
                <p class="mt-2">
                    <span class="lang" data-lang="en">Valid until May 19, 2026</span>
                </p>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // Language Switching
        document.addEventListener('DOMContentLoaded', function() {
            const langBtns = document.querySelectorAll('.lang-btn');
            const langElements = document.querySelectorAll('.lang');
            
            // Set default language
            let currentLang = 'en';
            
            // Language switch function
            function switchLanguage(lang) {
                // Hide all language elements
                langElements.forEach(el => {
                    el.classList.add('hidden');
                });
                
                // Show elements for selected language
                document.querySelectorAll(`.lang[data-lang="${lang}"]`).forEach(el => {
                    el.classList.remove('hidden');
                });
                
                // Update button styles
                langBtns.forEach(btn => {
                    btn.classList.remove('bg-primary', 'text-white');
                    btn.classList.add('hover:bg-gray-200');
                });
                
                document.getElementById(`lang-${lang}`).classList.add('bg-primary', 'text-white');
                document.getElementById(`lang-${lang}`).classList.remove('hover:bg-gray-200');
                
                // Update current language
                currentLang = lang;
                
                // Update document language attribute
                document.documentElement.lang = lang;
            }
            
            // Add click event listeners to language buttons
            langBtns.forEach(btn => {
                btn.addEventListener('click', function() {
                    const lang = this.id.split('-')[1];
                    switchLanguage(lang);
                });
            });
            
            // Countdown Timer
            function updateCountdown() {
                const targetDate = new Date('May 19, 2026 10:30:00').getTime();
                const now = new Date().getTime();
                const distance = targetDate - now;
                
                // If the date is in the past, show zeros
                if (distance < 0) {
                    document.getElementById('days').innerText = '00';
                    document.getElementById('hours').innerText = '00';
                    document.getElementById('minutes').innerText = '00';
                    document.getElementById('seconds').innerText = '00';
                    return;
                }
                
                const days = Math.floor(distance / (1000 * 60 * 60 * 24));
                const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((distance % (1000 * 60)) / 1000);
                
                document.getElementById('days').innerText = days.toString().padStart(2, '0');
                document.getElementById('hours').innerText = hours.toString().padStart(2, '0');
                document.getElementById('minutes').innerText = minutes.toString().padStart(2, '0');
                document.getElementById('seconds').innerText = seconds.toString().padStart(2, '0');
            }
            
            // Initialize countdown
            updateCountdown();
            setInterval(updateCountdown, 1000);
            
            // Create celebration effect
            function createCelebration() {
                const celebrationContainer = document.getElementById('celebration-container');
                const colors = ['#1a56db', '#ff6b00', '#ffd700', '#10b981', '#ef4444', '#8b5cf6'];
                
                for (let i = 0; i < 50; i++) {
                    const celebration = document.createElement('div');
                    celebration.classList.add('celebration');
                    
                    // Random properties
                    celebration.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                    celebration.style.left = `${Math.random() * 100}vw`;
                    celebration.style.width = `${Math.random() * 10 + 5}px`;
                    celebration.style.height = `${Math.random() * 10 + 5}px`;
                    celebration.style.animationDelay = `${Math.random() * 3}s`;
                    celebration.style.animationDuration = `${Math.random() * 3 + 2}s`;
                    
                    celebrationContainer.appendChild(celebration);
                    
                    // Remove celebration after animation completes
                    setTimeout(() => {
                        celebration.remove();
                    }, 5000);
                }
            }
            
            // Create celebration periodically
            setInterval(createCelebration, 5000);
            createCelebration(); // Create initial celebration
            
            // Smooth scrolling for anchor links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        });
    </script>

</body></html>
