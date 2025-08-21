<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MEDIVA - Healthcare & Wellness App</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
        
        .gradient-bg {
            background: linear-gradient(-45deg, #ec4899, #8b5cf6, #0ea5e9, #06b6d4);
            background-size: 400% 400%;
            animation: gradientShift 8s ease-in-out infinite;
        }
        
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .hero-bg {
            background-image: linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)), url('https://images.unsplash.com/photo-1594381898411-846e7d193883?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            animation: zoomSubtle 8s ease-in-out infinite;
        }
        
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 1s ease-out forwards;
        }
        
        .fade-in-delay-1 { animation-delay: 0.2s; }
        .fade-in-delay-2 { animation-delay: 0.4s; }
        .fade-in-delay-3 { animation-delay: 0.6s; }
        .fade-in-delay-4 { animation-delay: 0.8s; }
        .fade-in-delay-5 { animation-delay: 1s; }
        
        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .float-hover {
            transition: all 0.3s ease;
        }
        
        .float-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        }
        
        .pulse-glow {
            animation: pulseGlow 2s ease-in-out infinite;
        }
        
        @keyframes pulseGlow {
            0%, 100% { 
                box-shadow: 0 0 10px rgba(255, 255, 255, 0.3);
                transform: scale(1);
            }
            50% { 
                box-shadow: 0 0 20px rgba(255, 255, 255, 0.6);
                transform: scale(1.05);
            }
        }
        
        @keyframes zoomSubtle {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.02); }
        }
        
        .menu-item {
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .menu-item:hover {
            transform: translateX(10px);
            color: #06b6d4;
        }
        
        .text-shadow {
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
    </style>
</head>
<body class="min-h-screen overflow-hidden">
    <div class="flex min-h-screen">
        <!-- Left Side with Background Image -->
        <div class="w-1/2 hero-bg flex flex-col justify-center items-center p-12 relative text-white">
            <!-- MEDIVA Title -->
            <div class="fade-in mb-8 text-center">
                <h1 class="text-6xl font-bold text-teal-400 mb-4 text-shadow">MEDIVA</h1>
            </div>
            
            <!-- Description Text -->
            <div class="fade-in fade-in-delay-2 max-w-md text-center bg-black bg-opacity-40 p-8 rounded-2xl backdrop-blur-sm">
                <p class="text-white text-lg leading-relaxed mb-6">
                    <strong>MEDIVA</strong> is a healthcare and wellness app combining the words 
                    <em>Med</em> (Medicine) and <em>Diva</em> (Goddess).
                </p>
                
                <div class="text-left">
                    <p class="text-white font-medium mb-3">Our motive is to:</p>
                    <ul class="space-y-2 text-white">
                        <li class="fade-in fade-in-delay-3">1) Improve patient care</li>
                        <li class="fade-in fade-in-delay-4">2) Support healthcare providers</li>
                        <li class="fade-in fade-in-delay-5">3) Enhance accessibility</li>
                    </ul>
                </div>
            </div>
        </div>
        
        <!-- Right Side -->
        <div class="w-1/2 gradient-bg flex flex-col justify-center items-center p-12 text-white">
            <!-- Sign In Button -->
            <div class="fade-in mb-12">
                <button class="float-hover bg-white text-gray-800 px-12 py-4 rounded-full text-xl font-semibold shadow-lg">
                    SIGN IN / LOG IN
                </button>
            </div>
            
            <!-- Menu Items -->
            <div class="space-y-6 text-center mb-16">
                <div class="menu-item fade-in fade-in-delay-1 text-xl font-medium">User Profile</div>
                <div class="menu-item fade-in fade-in-delay-2 text-xl font-medium">Appointment Booking</div>
                <div class="menu-item fade-in fade-in-delay-3 text-xl font-medium">Clients Status</div>
                <div class="menu-item fade-in fade-in-delay-4 text-xl font-medium">Book a Consultation</div>
                <div class="menu-item fade-in fade-in-delay-5 text-xl font-medium">Health Records</div>
            </div>
            
            <!-- Social Media Icons -->
            <div class="flex space-x-8 fade-in fade-in-delay-5">
                <!-- Instagram -->
                <div class="pulse-glow p-3 rounded-full bg-white bg-opacity-20 cursor-pointer hover:bg-opacity-30 transition-all">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                    </svg>
                </div>
                
                <!-- Facebook -->
                <div class="pulse-glow p-3 rounded-full bg-white bg-opacity-20 cursor-pointer hover:bg-opacity-30 transition-all">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                    </svg>
                </div>
                
                <!-- Twitter -->
                <div class="pulse-glow p-3 rounded-full bg-white bg-opacity-20 cursor-pointer hover:bg-opacity-30 transition-all">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
                    </svg>
                </div>
            </div>
        </div>
    </div>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'972c7b9fb3d63c5e',t:'MTc1NTgwMzk3Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
