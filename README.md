<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FreshMart Express - Your Neighborhood Grocery</title>
    <link rel="icon" type="image/x-icon" href="/static/favicon.ico">
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/feather-icons"></script>
    <script src="https://cdn.jsdelivr.net/npm/feather-icons/dist/feather.min.js"></script>
    <style>
        .hero-gradient {
            background: linear-gradient(135deg, rgba(74, 222, 128, 0.9) 0%, rgba(34, 197, 94, 0.9) 100%);
        }
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
        }
        .transition-slow {
            transition: all 0.3s ease;
        }
    </style>
</head>
<body class="bg-gray-50 font-sans">
    <!-- Navigation -->
    <nav class="bg-white shadow-md sticky top-0 z-50">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i data-feather="shopping-cart" class="text-green-500"></i>
                <span class="text-xl font-bold text-green-600">FreshMart Express</span>
            </div>
            <div class="hidden md:flex space-x-6">
                <a href="#" class="text-green-600 font-medium">Home</a>
                <a href="#about" class="text-gray-600 hover:text-green-600 transition-slow">About</a>
                <a href="#services" class="text-gray-600 hover:text-green-600 transition-slow">Services</a>
                <a href="#offers" class="text-gray-600 hover:text-green-600 transition-slow">Offers</a>
                <a href="#contact" class="text-gray-600 hover:text-green-600 transition-slow">Contact</a>
            </div>
            <div class="flex items-center space-x-4">
                <button class="bg-green-500 hover:bg-green-600 text-white px-4 py-2 rounded-full transition-slow">
                    <i data-feather="user" class="inline mr-2"></i> Login
                </button>
                <button class="relative">
                    <i data-feather="shopping-bag" class="text-gray-700"></i>
                    <span class="absolute -top-2 -right-2 bg-green-500 text-white text-xs rounded-full h-5 w-5 flex items-center justify-center">3</span>
                </button>
                <button id="mobile-menu-button" class="md:hidden">
                    <i data-feather="menu" class="text-gray-700"></i>
                </button>
            </div>
        </div>
        <!-- Mobile menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white pb-4 px-4">
            <a href="#" class="block py-2 text-green-600 font-medium">Home</a>
            <a href="#about" class="block py-2 text-gray-600 hover:text-green-600 transition-slow">About</a>
            <a href="#services" class="block py-2 text-gray-600 hover:text-green-600 transition-slow">Services</a>
            <a href="#offers" class="block py-2 text-gray-600 hover:text-green-600 transition-slow">Offers</a>
            <a href="#contact" class="block py-2 text-gray-600 hover:text-green-600 transition-slow">Contact</a>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero-gradient text-white">
        <div class="container mx-auto px-4 py-20 md:py-32">
            <div class="max-w-2xl">
                <h1 class="text-4xl md:text-5xl font-bold mb-4">Fresh Groceries Delivered to Your Door</h1>
                <p class="text-xl mb-8">Discover the freshest produce, highest quality meats, and pantry essentials - all at affordable prices.</p>
                <div class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4">
                    <button class="bg-white text-green-600 hover:bg-gray-100 px-6 py-3 rounded-full font-medium transition-slow">
                        Shop Now <i data-feather="arrow-right" class="inline ml-2"></i>
                    </button>
                    <button class="bg-transparent border-2 border-white hover:bg-white hover:text-green-600 px-6 py-3 rounded-full font-medium transition-slow">
                        Weekly Deals
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-gray-50 p-6 rounded-xl text-center card-hover transition-slow">
                    <div class="bg-green-100 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i data-feather="truck" class="text-green-600 w-6 h-6"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Free Delivery</h3>
                    <p class="text-gray-600">On orders over $50 within 5 miles</p>
                </div>
                <div class="bg-gray-50 p-6 rounded-xl text-center card-hover transition-slow">
                    <div class="bg-green-100 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i data-feather="clock" class="text-green-600 w-6 h-6"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Express Checkout</h3>
                    <p class="text-gray-600">Skip the lines with our mobile app</p>
                </div>
                <div class="bg-gray-50 p-6 rounded-xl text-center card-hover transition-slow">
                    <div class="bg-green-100 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i data-feather="award" class="text-green-600 w-6 h-6"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Quality Guaranteed</h3>
                    <p class="text-gray-600">Freshness or your money back</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pr-8">
                    <img src="http://static.photos/food/640x360/42" alt="Fresh produce" class="rounded-xl shadow-lg w-full">
                </div>
                <div class="md:w-1/2">
                    <h2 class="text-3xl font-bold mb-6 text-gray-800">About FreshMart Express</h2>
                    <p class="text-gray-600 mb-4">Founded in 2010, FreshMart Express started as a small neighborhood grocery with a big vision - to provide fresh, affordable food to our community while supporting local farmers and producers.</p>
                    <p class="text-gray-600 mb-6">Today, we've grown to become your trusted one-stop shop for all your grocery needs, combining the personal service of a local market with the convenience and selection of a large supermarket.</p>
                    <button class="bg-green-500 hover:bg-green-600 text-white px-6 py-3 rounded-full font-medium transition-slow">
                        Our Story <i data-feather="arrow-right" class="inline ml-2"></i>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold mb-4 text-gray-800">Our Services</h2>
                <p class="text-gray-600 max-w-2xl mx-auto">We offer a variety of services to make your grocery shopping experience easier and more enjoyable.</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-gray-50 p-8 rounded-xl card-hover transition-slow">
                    <h3 class="text-2xl font-bold mb-4 text-green-600">Short-Term Services</h3>
                    <ul class="space-y-3">
                        <li class="flex items-start">
                            <i data-feather="check-circle" class="text-green-500 mr-2 mt-1"></i>
                            <span class="text-gray-700">Same-day home delivery (order by 2pm)</span>
                        </li>
                        <li class="flex items-start">
                            <i data-feather="check-circle" class="text-green-500 mr-2 mt-1"></i>
                            <span class="text-gray-700">Curbside pickup with 1-hour notice</span>
                        </li>
                        <li class="flex items-start">
                            <i data-feather="check-circle" class="text-green-500 mr-2 mt-1"></i>
                            <span class="text-gray-700">Weekly flash sales and discounts</span>
                        </li>
                    </ul>
                </div>
                <div class="bg-gray-50 p-8 rounded-xl card-hover transition-slow">
                    <h3 class="text-2xl font-bold mb-4 text-green-600">Long-Term Benefits</h3>
                    <ul class="space-y-3">
                        <li class="flex items-start">
                            <i data-feather="check-circle" class="text-green-500 mr-2 mt-1"></i>
                            <span class="text-gray-700">Loyalty rewards program (earn points on every purchase)</span>
                        </li>
                        <li class="flex items-start">
                            <i data-feather="check-circle" class="text-green-500 mr-2 mt-1"></i>
                            <span class="text-gray-700">Monthly subscription boxes (save 15%)</span>
                        </li>
                        <li class="flex items-start">
                            <i data-feather="check-circle" class="text-green-500 mr-2 mt-1"></i>
                            <span class="text-gray-700">Sustainable packaging options</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Offers Section -->
    <section id="offers" class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold mb-2 text-gray-800">Current Offers</h2>
                <p class="text-gray-600">Limited time deals you won't want to miss</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Offer 1 -->
                <div class="bg-white rounded-xl shadow-md overflow-hidden card-hover transition-slow">
                    <img src="http://static.photos/food/640x360/1" alt="Organic fruits" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="text-xl font-bold">Organic Fruits</h3>
                            <span class="bg-green-100 text-green-800 text-sm px-2 py-1 rounded">20% OFF</span>
                        </div>
                        <p class="text-gray-600 mb-4">Stock up on fresh organic apples, bananas, and berries this week.</p>
                        <button class="w-full bg-green-500 hover:bg-green-600 text-white py-2 rounded-lg transition-slow">
                            Add to Cart
                        </button>
                    </div>
                </div>
                <!-- Offer 2 -->
                <div class="bg-white rounded-xl shadow-md overflow-hidden card-hover transition-slow">
                    <img src="http://static.photos/food/640x360/2" alt="Dairy products" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="text-xl font-bold">Dairy Essentials</h3>
                            <span class="bg-green-100 text-green-800 text-sm px-2 py-1 rounded">Buy 1 Get 1</span>
                        </div>
                        <p class="text-gray-600 mb-4">Milk, cheese, yogurt and more. Limited time BOGO deal.</p>
                        <button class="w-full bg-green-500 hover:bg-green-600 text-white py-2 rounded-lg transition-slow">
                            Add to Cart
                        </button>
                    </div>
                </div>
                <!-- Offer 3 -->
                <div class="bg-white rounded-xl shadow-md overflow-hidden card-hover transition-slow">
                    <img src="http://static.photos/food/640x360/3" alt="Pantry staples" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="text-xl font-bold">Pantry Staples</h3>
                            <span class="bg-green-100 text-green-800 text-sm px-2 py-1 rounded">15% OFF</span>
                        </div>
                        <p class="text-gray-600 mb-4">Flour, sugar, oils and other cooking essentials.</p>
                        <button class="w-full bg-green-500 hover:bg-green-600 text-white py-2 rounded-lg transition-slow">
                            Add to Cart
                        </button>
                    </div>
                </div>
            </div>
            <div class="text-center mt-10">
                <button class="border-2 border-green-500 text-green-600 hover:bg-green-500 hover:text-white px-6 py-3 rounded-full font-medium transition-slow">
                    View All Offers
                </button>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-16 bg-green-600 text-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold mb-2">What Our Customers Say</h2>
                <p class="text-green-100">Don't just take our word for it</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Testimonial 1 -->
                <div class="bg-green-700 p-6 rounded-xl">
                    <div class="flex items-center mb-4">
                        <div class="flex">
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                        </div>
                    </div>
                    <p class="mb-4">"The produce at FreshMart is always fresh and reasonably priced. Their delivery service has been a lifesaver during busy weeks!"</p>
                    <div class="flex items-center">
                        <img src="http://static.photos/people/200x200/1" alt="Sarah J." class="w-10 h-10 rounded-full mr-3">
                        <div>
                            <h4 class="font-bold">Sarah J.</h4>
                            <p class="text-green-200 text-sm">Local Resident</p>
                        </div>
                    </div>
                </div>
                <!-- Testimonial 2 -->
                <div class="bg-green-700 p-6 rounded-xl">
                    <div class="flex items-center mb-4">
                        <div class="flex">
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                        </div>
                    </div>
                    <p class="mb-4">"I love their loyalty program. The points add up quickly and I've gotten several free items already. Staff is always friendly too!"</p>
                    <div class="flex items-center">
                        <img src="http://static.photos/people/200x200/2" alt="Michael T." class="w-10 h-10 rounded-full mr-3">
                        <div>
                            <h4 class="font-bold">Michael T.</h4>
                            <p class="text-green-200 text-sm">Frequent Shopper</p>
                        </div>
                    </div>
                </div>
                <!-- Testimonial 3 -->
                <div class="bg-green-700 p-6 rounded-xl">
                    <div class="flex items-center mb-4">
                        <div class="flex">
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                            <i data-feather="star" class="text-yellow-300 w-5 h-5"></i>
                        </div>
                    </div>
                    <p class="mb-4">"Their weekly deals are amazing! I plan my meals around what's on sale. The quality is consistently good and prices beat the big chains."</p>
                    <div class="flex items-center">
                        <img src="http://static.photos/people/200x200/3" alt="Lisa P." class="w-10 h-10 rounded-full mr-3">
                        <div>
                            <h4 class="font-bold">Lisa P.</h4>
                            <p class="text-green-200 text-sm">Budget Shopper</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pr-8">
                    <h2 class="text-3xl font-bold mb-6 text-gray-800">Contact Us</h2>
                    <div class="space-y-6">
                        <div class="flex items-start">
                            <i data-feather="map-pin" class="text-green-500 mr-4 mt-1"></i>
                            <div>
                                <h3 class="font-bold text-lg mb-1">Our Location</h3>
                                <p class="text-gray-600">123 Grocery Lane, Freshville, CA 90210</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <i data-feather="phone" class="text-green-500 mr-4 mt-1"></i>
                            <div>
                                <h3 class="font-bold text-lg mb-1">Call Us</h3>
                                <p class="text-gray-600">(555) 123-4567</p>
                                <p class="text-gray-600 text-sm">Mon-Sat: 8am-9pm, Sun: 9am-7pm</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <i data-feather="mail" class="text-green-500 mr-4 mt-1"></i>
                            <div>
                                <h3 class="font-bold text-lg mb-1">Email Us</h3>
                                <p class="text-gray-600">hello@freshmartexpress.com</p>
                            </div>
                        </div>
                    </div>
                    <div class="
