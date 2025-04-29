## Hi there 👋
<<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Paragliding Adventures</title>
    <script src="https://cdn.tailwindcss.com/3.4.16"></script>
    <script>tailwind.config={theme:{extend:{colors:{primary:'#3B82F6',secondary:'#10B981'},borderRadius:{'none':'0px','sm':'4px',DEFAULT:'8px','md':'12px','lg':'16px','xl':'20px','2xl':'24px','3xl':'32px','full':'9999px','button':'8px'}}}}</script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/remixicon/4.6.0/remixicon.min.css">
    <style>
        :where([class^="ri-"])::before { content: "\f3c2"; }
        body {
            font-family: 'Inter', sans-serif;
        }
        .date-input::-webkit-calendar-picker-indicator {
            display: none;
        }
        input[type="number"]::-webkit-inner-spin-button,
        input[type="number"]::-webkit-outer-spin-button {
            -webkit-appearance: none;
            margin: 0;
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Navigation Bar -->
    <nav class="fixed top-0 left-0 w-full bg-black
    z-50 transition-all duration-300" id="navbar">
        <div class="px-6 py-0.5 flex justify-between items-center">
            <div class="text-white font-['Pacifico'] text-2xl">FlyingVenture</div>
            <button class="w-10 h-10 flex items-center justify-center text-white bg-white/20 backdrop-blur-md rounded-full cursor-pointer">
                <i class="ri-menu-line ri-lg"></i>
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative h-[500px] overflow-hidden">
        <img src="https://readdy.ai/api/search-image?query=paragliding%20over%20beautiful%20mountains%20in%20Bir-Billing%2C%20India%2C%20aerial%20view%20of%20colorful%20paragliders%20flying%20over%20lush%20green%20valleys%20and%20snow-capped%20Himalayan%20mountains%2C%20stunning%20landscape%2C%20clear%20blue%20sky%2C%20adventure%20sports%2C%20breathtaking%20scenic%20view%2C%20professional%20photography&width=375&height=500&seq=1&orientation=portrait" 
             alt="Paragliding Experience" 
             class="w-full h-full object-cover object-top">
        <div class="absolute inset-0 bg-gradient-to-b from-black/50 to-black/70 flex flex-col justify-end p-6">
            <h1 class="text-white text-3xl font-bold mb-2">Experience the Joy of Flying</h1>
            <p class="text-white text-lg mb-6">Bir-Billing's Most Trusted Platform</p>
            <button class="bg-primary text-white py-3 px-6 rounded-button font-semibold text-lg shadow-lg w-full cursor-pointer">
                Book Now
            </button>
        </div>
    </section>

    <!-- Refund Policy Banner -->
    <section class="bg-blue-50 p-4 flex items-center border-b border-blue-100">
        <div class="w-10 h-10 flex items-center justify-center text-primary mr-3">
            <i class="ri-shield-check-line ri-lg"></i>
        </div>
        <div class="flex-1">
            <h3 class="text-gray-800 font-semibold">100% Refund Guarantee</h3>
            <p class="text-gray-600 text-sm">Cancel up to 42 hours before flight</p>
        </div>
        <button class="text-primary font-medium text-sm cursor-pointer">
            Learn More
        </button>
    </section>

    <!-- Quick Booking Widget -->
    <section class="px-4 -mt-6 relative z-10">
        <div class="bg-white rounded-lg shadow-lg p-5">
            <h2 class="text-lg font-semibold text-gray-800 mb-4">Book Your Flight</h2>
            
            <div class="mb-4">
                <label class="block text-sm font-medium text-gray-700 mb-1">Select Date</label>
                <div class="relative">
                    <input type="date" class="date-input w-full border border-gray-300 rounded p-3 pr-10 text-gray-700" min="2025-04-28">
                    <div class="absolute right-3 top-1/2 transform -translate-y-1/2 w-5 h-5 flex items-center justify-center text-gray-500">
                        <i class="ri-calendar-line"></i>
                    </div>
                </div>
            </div>
            
            <div class="mb-4">
                <label class="block text-sm font-medium text-gray-700 mb-1">Preferred Time</label>
                <div class="relative">
                    <select class="w-full border border-gray-300 rounded p-3 pr-10 text-gray-700 appearance-none">
                        <option value="">Select time slot</option>
                        <option value="morning">Morning (7:00 AM - 10:00 AM)</option>
                        <option value="midday">Midday (10:00 AM - 1:00 PM)</option>
                        <option value="afternoon">Afternoon (1:00 PM - 4:00 PM)</option>
                    </select>
                    <div class="absolute right-3 top-1/2 transform -translate-y-1/2 w-5 h-5 flex items-center justify-center text-gray-500">
                        <i class="ri-time-line"></i>
                    </div>
                </div>
            </div>
            
            <div class="mb-5">
                <label class="block text-sm font-medium text-gray-700 mb-1">Number of Persons</label>
                <div class="flex items-center border border-gray-300 rounded overflow-hidden">
                    <button id="decrease" class="w-12 h-12 flex items-center justify-center text-gray-500 bg-gray-100 cursor-pointer">
                        <i class="ri-subtract-line ri-lg"></i>
                    </button>
                    <input type="number" id="persons" value="1" min="1" max="10" class="w-full h-12 text-center border-none text-gray-700">
                    <button id="increase" class="w-12 h-12 flex items-center justify-center text-gray-500 bg-gray-100 cursor-pointer">
                        <i class="ri-add-line ri-lg"></i>
                    </button>
                </div>
            </div>
            
            <button class="bg-primary text-white py-3 px-6 rounded-button font-semibold w-full cursor-pointer">
                Check Availability
            </button>
        </div>
    </section>

    <!-- Key Features Section -->
    <section class="px-4 py-8">
        <h2 class="text-xl font-semibold text-gray-800 mb-6">Why Choose Us</h2>
        
        <div class="grid grid-cols-2 gap-4">
            <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center text-center">
                <div class="w-14 h-14 flex items-center justify-center bg-blue-100 rounded-full mb-3 text-primary">
                    <i class="ri-user-star-line ri-lg"></i>
                </div>
                <h3 class="font-medium text-gray-800 mb-1">Certified Pilots</h3>
                <p class="text-gray-600 text-sm">Experienced professionals with 1000+ flights</p>
            </div>
            
            <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center text-center">
                <div class="w-14 h-14 flex items-center justify-center bg-green-100 rounded-full mb-3 text-secondary">
                    <i class="ri-shield-check-line ri-lg"></i>
                </div>
                <h3 class="font-medium text-gray-800 mb-1">Safety First</h3>
                <p class="text-gray-600 text-sm">Premium equipment inspected daily</p>
            </div>
            
            <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center text-center">
                <div class="w-14 h-14 flex items-center justify-center bg-blue-100 rounded-full mb-3 text-primary">
                    <i class="ri-price-tag-3-line ri-lg"></i>
                </div>
                <h3 class="font-medium text-gray-800 mb-1">Best Price</h3>
                <p class="text-gray-600 text-sm">Guaranteed lowest rates with no hidden fees</p>
            </div>
            
            <div class="bg-white p-4 rounded-lg shadow-sm flex flex-col items-center text-center">
                <div class="w-14 h-14 flex items-center justify-center bg-green-100 rounded-full mb-3 text-secondary">
                    <i class="ri-flashlight-line ri-lg"></i>
                </div>
                <h3 class="font-medium text-gray-800 mb-1">Instant Booking</h3>
                <p class="text-gray-600 text-sm">Confirm your slot in less than 2 minutes</p>
            </div>
        </div>
    </section>

    <!-- Flight Packages -->
    <section class="px-4 py-6 bg-white">
        <h2 class="text-xl font-semibold text-gray-800 mb-1">Our Flight Packages</h2>
        <p class="text-gray-600 mb-6">Choose the perfect experience for you</p>
        
        <div class="space-y-4">
            <div class="border border-gray-200 rounded-lg overflow-hidden">
                <div class="relative h-48 overflow-hidden">
                    <img src="https://readdy.ai/api/search-image?query=paragliding%20tandem%20flight%20with%20instructor%20and%20passenger%2C%20beautiful%20mountain%20landscape%20view%20from%20above%2C%20clear%20blue%20sky%2C%20professional%20adventure%20sports%20photography%2C%20vibrant%20paraglider%20canopy%2C%20scenic%20Himalayan%20mountains%20below&width=375&height=192&seq=2&orientation=landscape" 
                         alt="Standard Flight" 
                         class="w-full h-full object-cover object-top">
                    <div class="absolute top-3 right-3 bg-primary text-white px-3 py-1 rounded-full text-sm font-medium">
                        Most Popular
                    </div>
                </div>
                <div class="p-4">
                    <div class="flex justify-between items-start mb-2">
                        <div>
                            <h3 class="text-lg font-semibold text-gray-800">Standard Flight</h3>
                            <p class="text-gray-600 text-sm">10-15 minutes</p>
                        </div>
                        <div class="text-right">
                            <p class="text-sm text-gray-500">from</p>
                            <p class="text-xl font-bold text-gray-800">₹2,499</p>
                        </div>
                    </div>
                    
                    <div class="mb-4">
                        <div class="flex items-start mb-2">
                            <i class="ri-check-line text-green-500 mt-1 mr-2"></i>
                            <p class="text-gray-700 text-sm">Tandem flight with certified pilot</p>
                        </div>
                        <div class="flex items-start mb-2">
                            <i class="ri-check-line text-green-500 mt-1 mr-2"></i>
                            <p class="text-gray-700 text-sm">Basic maneuvers experience</p>
                        </div>
                        <div class="flex items-start">
                            <i class="ri-check-line text-green-500 mt-1 mr-2"></i>
                            <p class="text-gray-700 text-sm">Free4K video with GoPro</p>
                        </div>
                    </div>
                    
                    <button class="bg-primary text-white py-2.5 px-4 rounded-button font-medium w-full cursor-pointer">
                        Select Package
                    </button>
                </div>
            </div>
            
            <div class="border border-gray-200 rounded-lg overflow-hidden">
                <div class="relative h-48 overflow-hidden">
                    <img src="https://readdy.ai/api/search-image?query=premium%20paragliding%20experience%2C%20pilot%20performing%20acrobatic%20maneuvers%20with%20passenger%2C%20breathtaking%20aerial%20view%20of%20mountains%20and%20valleys%2C%20high-quality%20adventure%20sports%20photography%2C%20vibrant%20paraglider%20against%20blue%20sky&width=375&height=192&seq=3&orientation=landscape" 
                         alt="Premium Flight" 
                         class="w-full h-full object-cover object-top">
                </div>
                <div class="p-4">
                    <div class="flex justify-between items-start mb-2">
                        <div>
                            <h3 class="text-lg font-semibold text-gray-800">Premium Flight</h3>
                            <p class="text-gray-600 text-sm">15-20 minutes</p>
                        </div>
                        <div class="text-right">
                            <p class="text-sm text-gray-500">from</p>
                            <p class="text-xl font-bold text-gray-800">₹3,999</p>
                        </div>
                    </div>
                    
                    <div class="mb-4">
                        <div class="flex items-start mb-2">
                            <i class="ri-check-line text-green-500 mt-1 mr-2"></i>
                            <p class="text-gray-700 text-sm">Extended flight duration</p>
                        </div>
                        <div class="flex items-start mb-2">
                            <i class="ri-check-line text-green-500 mt-1 mr-2"></i>
                            <p class="text-gray-700 text-sm">Acrobatic maneuvers included</p>
                        </div>
                        <div class="flex items-start mb-2">
                            <i class="ri-check-line text-green-500 mt-1 mr-2"></i>
                            <p class="text-gray-700 text-sm">Free4K video with GoPro</p>
                        </div>
                        <div class="flex items-start">
                            <i class="ri-check-line text-green-500 mt-1 mr-2"></i>
                            <p class="text-gray-700 text-sm"> Flying stunts </p>
                        </div>
                    </div>
                    
                    <button class="bg-white border border-primary text-primary py-2.5 px-4 rounded-button font-medium w-full cursor-pointer">
                        Select Package
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Trust Indicators -->
    <section class="px-4 py-8 bg-gray-50">
        <h2 class="text-xl font-semibold text-gray-800 mb-6">Why Customers Trust Us</h2>
        
        <div class="bg-white rounded-lg shadow-sm p-4 mb-5">
            <div class="flex items-center mb-4">
                <div class="flex text-yellow-400">
                    <i class="ri-star-fill"></i>
                    <i class="ri-star-fill"></i>
                    <i class="ri-star-fill"></i>
                    <i class="ri-star-fill"></i>
                    <i class="ri-star-half-fill"></i>
                </div>
                <p class="ml-2 text-gray-700 font-medium">4.8/5 from 1,200+ reviews</p>
            </div>
            
            <div class="flex items-center justify-between mb-3">
                <div class="flex items-center">
                    <div class="w-10 h-10 flex items-center justify-center bg-blue-100 rounded-full mr-3 text-primary">
                        <i class="ri-flight-takeoff-line"></i>
                    </div>
                    <div>
                        <h3 class="font-medium text-gray-800">5,000+</h3>
                        <p class="text-gray-600 text-sm">Successful flights</p>
                    </div>
                </div>
                
                <div class="flex items-center">
                    <div class="w-10 h-10 flex items-center justify-center bg-green-100 rounded-full mr-3 text-secondary">
                        <i class="ri-user-smile-line"></i>
                    </div>
                    <div>
                        <h3 class="font-medium text-gray-800">98%</h3>
                        <p class="text-gray-600 text-sm">Happy customers</p>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="bg-white rounded-lg shadow-sm p-4">
            <h3 class="font-medium text-gray-800 mb-3">Recent Customer Review</h3>
            
            <div class="border-l-4 border-primary pl-3 mb-4">
                <p class="text-gray-700 italic mb-2">"An incredible experience! The views were breathtaking and my pilot Rahul made me feel completely safe. Worth every penny!"</p>
                <div class="flex items-center">
                    <p class="text-gray-600 text-sm font-medium">Sarah Johnson</p>
                    <div class="mx-2 w-1 h-1 bg-gray-400 rounded-full"></div>
                    <p class="text-gray-500 text-sm">April 25, 2025</p>
                </div>
            </div>
            
            <button class="text-primary font-medium text-sm cursor-pointer">
                Read more reviews
            </button>
        </div>
    </section>

    <!-- Certification Badges -->
    <section class="px-4 py-6 bg-white border-t border-gray-200">
        <h2 class="text-lg font-semibold text-gray-800 mb-4">Safety Certifications</h2>
        
        <div class="flex flex-wrap justify-between">
            <div class="w-[30%] flex flex-col items-center mb-4">
                <div class="w-12 h-12 flex items-center justify-center bg-blue-100 rounded-full mb-2 text-primary">
                    <i class="ri-award-line ri-lg"></i>
                </div>
                <p class="text-gray-700 text-xs text-center">APPI Certified</p>
            </div>
            
            <div class="w-[30%] flex flex-col items-center mb-4">
                <div class="w-12 h-12 flex items-center justify-center bg-blue-100 rounded-full mb-2 text-primary">
                    <i class="ri-shield-star-line ri-lg"></i>
                </div>
                <p class="text-gray-700 text-xs text-center">BHPA Member</p>
            </div>
            
            <div class="w-[30%] flex flex-col items-center mb-4">
                <div class="w-12 h-12 flex items-center justify-center bg-blue-100 rounded-full mb-2 text-primary">
                    <i class="ri-heart-pulse-line ri-lg"></i>
                </div>
                <p class="text-gray-700 text-xs text-center">First Aid Trained</p>
            </div>
        </div>
    </section>

    <!-- Back to Top Button -->
    <button id="backToTop" class="fixed bottom-20 right-4 w-10 h-10 bg-white shadow-md rounded-full flex items-center justify-center text-primary opacity-0 transition-opacity duration-300 cursor-pointer">
        <i class="ri-arrow-up-line ri-lg"></i>
    </button>

    <!-- Bottom Action Bar -->
    <div class="fixed bottom-0 left-0 w-full bg-white border-t border-gray-200 px-4 py-3 flex items-center justify-between z-40">
        <div>
            <p class="text-xs text-gray-500">Need help?</p>
            <a href="tel:+919876543210" class="text-gray-800 font-medium">+91 9157648877</a>
        </div>
        
        <div class="flex">
            <a href="https://wa.me/919876543210" class="mr-3 w-10 h-10 flex items-center justify-center bg-green-500 rounded-full text-white cursor-pointer">
                <i class="ri-whatsapp-line ri-lg"></i>
            </a>
            <button class="bg-primary text-white py-2 px-6 rounded-button font-medium cursor-pointer">
                Call Now
            </button>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Person counter functionality
            const decreaseBtn = document.getElementById('decrease');
            const increaseBtn = document.getElementById('increase');
            const personsInput = document.getElementById('persons');
            
            decreaseBtn.addEventListener('click', function() {
                const currentValue = parseInt(personsInput.value);
                if (currentValue > 1) {
                    personsInput.value = currentValue - 1;
                }
            });
            
            increaseBtn.addEventListener('click', function() {
                const currentValue = parseInt(personsInput.value);
                if (currentValue < 10) {
                    personsInput.value = currentValue + 1;
                }
            });
            
            // Set minimum date to today
            const today = new Date();
            const yyyy = today.getFullYear();
            const mm = String(today.getMonth() + 1).padStart(2, '0');
            const dd = String(today.getDate()).padStart(2, '0');
            const todayString = `${yyyy}-${mm}-${dd}`;
            
            const dateInput = document.querySelector('input[type="date"]');
            dateInput.min = todayString;
            dateInput.value = todayString;
        });
        
        // Navbar background change on scroll
        window.addEventListener('scroll', function() {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 10) {
                navbar.classList.add('bg-white', 'shadow-md');
                navbar.classList.remove('bg-transparent');
                navbar.querySelectorAll('.text-white').forEach(el => {
                    el.classList.remove('text-white');
                    el.classList.add('text-gray-800');
                });
            } else {
                navbar.classList.remove('bg-white', 'shadow-md');
                navbar.classList.add('bg-transparent');
                navbar.querySelectorAll('.text-gray-800').forEach(el => {
                    el.classList.remove('text-gray-800');
                    el.classList.add('text-white');
                });
            }
        });
        
        // Back to top button
        document.addEventListener('DOMContentLoaded', function() {
            const backToTopBtn = document.getElementById('backToTop');
            
            window.addEventListener('scroll', function() {
                if (window.scrollY > 300) {
                    backToTopBtn.classList.remove('opacity-0');
                    backToTopBtn.classList.add('opacity-100');
                } else {
                    backToTopBtn.classList.remove('opacity-100');
                    backToTopBtn.classList.add('opacity-0');
                }
            });
            
            backToTopBtn.addEventListener('click', function() {
                window.scrollTo({
                    top: 0,
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>

<!--
**FlyVenture/FlyVenture** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

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
