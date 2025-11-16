# college-project
This is my first git repository
<br>
Author-Farah 
minimalist e-commerce template 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clarity Store | Branded Stationery & Goods</title>
    <!-- Load Tailwind CSS via CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- CSS Configuration Script: Defines Custom Brand Colors -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        // Your brand colors: Deep Charcoal and Muted Gold
                        'primary-black': '#1a1a1a',   // Deep Charcoal / Off-Black
                        'accent-gold': '#b8860b',     // Muted Gold
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style>
        /* Base styling */
        body {
            font-family: 'Inter', sans-serif;
            -webkit-font-smoothing: antialiased;
        }

        /* --- Product Card Interaction (CSS ONLY) --- */
        .product-card {
            transition: transform 0.2s ease-out, box-shadow 0.2s ease-out, border 0.2s ease-out;
            border: 1px solid #e5e5e5; /* Light initial border */
        }
        .product-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 15px 20px -5px rgba(0, 0, 0, 0.1);
            border-color: var(--tw-colors-accent-gold); /* Using the custom color */
        }
        .product-card:hover .product-image {
            transform: scale(1.05);
            opacity: 0.9;
        }
        .product-image {
            transition: transform 0.4s ease-in-out, opacity 0.4s ease-in-out;
        }
        
        /* Ensure all links and buttons are focusable and accessible */
        a:focus, button:focus {
            outline: 2px solid var(--tw-colors-accent-gold);
            outline-offset: 2px;
        }
        
        /* Specific styling for the hero button interaction */
        .hero-btn:hover {
            background-color: #1a1a1a;
            color: white;
            border-color: #1a1a1a;
        }
    </style>
</head>
<body class="bg-white text-primary-black">

    <!-- Header: Sticky and essential navigation -->
    <header class="bg-white sticky top-0 z-20 border-b border-gray-100 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <!-- Logo/Brand -->
            <h1 class="text-3xl font-extrabold tracking-widest text-primary-black uppercase">
                <a href="/" aria-label="Home page link" class="hover:text-accent-gold transition">CLARITY</a>
            </h1>
            
            <!-- Desktop Navigation Links -->
            <nav class="hidden md:flex space-x-8 text-sm font-medium">
                <a href="#" class="hover:text-accent-gold transition uppercase tracking-wider">Shop All</a>
                <a href="#" class="hover:text-accent-gold transition uppercase tracking-wider">Stationery</a>
                <a href="#" class="hover:text-accent-gold transition uppercase tracking-wider">Deskware</a>
                <a href="#" class="hover:text-accent-gold transition uppercase tracking-wider">About</a>
            </nav>

            <!-- Icons: Search, Account, Cart -->
            <div class="flex items-center space-x-4">
                <button aria-label="Search products" class="p-2 text-primary-black hover:text-accent-gold transition">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path></svg>
                </button>
                <button aria-label="User Account" class="p-2 text-primary-black hover:text-accent-gold transition hidden sm:block">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path></svg>
                </button>
                <button aria-label="Shopping Cart" class="p-2 text-primary-black hover:text-accent-gold transition relative">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
                    <span class="absolute top-1 right-1 inline-flex items-center justify-center h-4 w-4 text-xs font-bold bg-accent-gold text-white rounded-full">2</span>
                </button>
            </div>
        </div>
    </header>

    <!-- Hero Section: Highlighting a key collection/message -->
    <section class="bg-gray-50 py-12 md:py-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row items-center justify-between gap-8">
            <!-- Text Content -->
            <div class="md:w-1/2 text-center md:text-left">
                <p class="text-sm text-gray-500 uppercase tracking-widest mb-2">The Archive Collection</p>
                <h2 class="text-5xl md:text-6xl font-extrabold text-primary-black mb-4 leading-tight">
                    Tools for Timeless Work
                </h2>
                <p class="text-lg text-gray-700 mb-8 max-w-lg mx-auto md:mx-0">
                    Discover high-quality, sustainably sourced paper and premium writing instruments, designed to last and inspire your best ideas.
                </p>
                <a href="#" class="hero-btn inline-block px-8 py-3 text-lg font-semibold border-2 border-primary-black text-primary-black rounded-full hover:bg-primary-black hover:text-white transition duration-300 uppercase tracking-wider">
                    Shop Notebooks
                </a>
            </div>
            <!-- Image (Placeholder for visual appeal) -->
            <div class="md:w-1/2 flex justify-center">
                <!-- Switched to a reliable placeholder URL to ensure the layout loads correctly in this environment -->
                <img src="https://placehold.co/600x600/b8860b/ffffff?text=Premium+Deskware" 
                     alt="A placeholder for premium desk setup image" 
                     class="w-full max-w-sm rounded-lg shadow-xl">
            </div>
        </div>
    </section>

    <!-- Product Showcase Section -->
    <main class="max-w-7xl mx-auto py-12 sm:py-20 px-4 sm:px-6 lg:px-8">
        
        <!-- Category Filter Bar -->
        <div class="flex flex-wrap gap-3 justify-center mb-12">
            <a href="#" class="px-5 py-2 text-sm font-semibold rounded-full border-2 border-primary-black bg-primary-black text-white uppercase tracking-wider transition">All Products</a>
            <a href="#" class="px-5 py-2 text-sm font-semibold rounded-full border-2 border-gray-300 text-gray-600 hover:border-accent-gold hover:text-accent-gold transition">Notebooks</a>
            <a href="#" class="px-5 py-2 text-sm font-semibold rounded-full border-2 border-gray-300 text-gray-600 hover:border-accent-gold hover:text-accent-gold transition">Pens & Pencils</a>
            <a href="#" class="px-5 py-2 text-sm font-semibold rounded-full border-2 border-gray-300 text-gray-600 hover:border-accent-gold hover:text-accent-gold transition">Desk Accessories</a>
        </div>

        <h2 class="text-3xl font-bold text-primary-black mb-10 text-center">
            New Arrivals in Stationery
        </h2>

        <!-- Product Grid: 8 Items -->
        <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6 sm:gap-8">
            
            <!-- Product Card 1: Premium Lined Journal -->
            <a href="#" class="product-card block rounded-xl overflow-hidden bg-white" aria-label="View Premium Lined Journal product details">
                <div class="relative bg-gray-50 aspect-square overflow-hidden">
                    <img src="https://placehold.co/600x600/b8860b/ffffff?text=Lined+Journal" 
                         alt="Leather-bound journal with gold gilded edges" 
                         class="product-image w-full h-full object-cover">
                    <span class="absolute top-3 left-3 bg-red-600 text-white text-xs font-semibold px-2 py-0.5 rounded-full uppercase tracking-wider shadow-md">Sale</span>
                </div>
                
                <div class="p-4 text-center">
                    <h3 class="text-lg font-semibold text-primary-black mb-1">Premium Lined Journal</h3>
                    <p class="text-sm text-gray-500 mb-3">A5 format, 200 pages, soft cover.</p>
                    <div class="flex items-center justify-center space-x-2">
                        <span class="text-xl font-bold text-primary-black">$28.00</span>
                        <span class="text-sm text-gray-400 line-through">$35.00</span>
                    </div>
                    <!-- Add to Cart Link -->
                    <span class="mt-3 inline-block w-full bg-primary-black text-white font-medium py-2 rounded-lg text-sm uppercase hover:bg-accent-gold transition duration-200">
                        View Item
                    </span>
                </div>
            </a>

            <!-- Product Card 2: Horizon Sketchbook -->
            <a href="#" class="product-card block rounded-xl overflow-hidden bg-white" aria-label="View Horizon Sketchbook product details">
                <div class="relative bg-gray-50 aspect-square overflow-hidden">
                    <img src="https://placehold.co/600x600/1a1a1a/b8860b?text=Sketchbook+Black" 
                         alt="Black cover spiral-bound sketchbook" 
                         class="product-image w-full h-full object-cover">
                </div>
                <div class="p-4 text-center">
                    <h3 class="text-lg font-semibold text-primary-black mb-1">Horizon Sketchbook</h3>
                    <p class="text-sm text-gray-500 mb-3">Thick, acid-free paper, spiral bound.</p>
                    <div class="flex items-center justify-center">
                        <span class="text-xl font-bold text-primary-black">$18.99</span>
                    </div>
                    <span class="mt-3 inline-block w-full bg-primary-black text-white font-medium py-2 rounded-lg text-sm uppercase hover:bg-accent-gold transition duration-200">
                        View Item
                    </span>
                </div>
            </a>
            
            <!-- Product Card 3: Gel Pen Set -->
            <a href="#" class="product-card block rounded-xl overflow-hidden bg-white" aria-label="View Minimalist Gel Pen Set product details">
                <div class="relative bg-gray-50 aspect-square overflow-hidden">
                    <img src="https://placehold.co/600x600/cccccc/1a1a1a?text=Gel+Pen+Set" 
                         alt="Set of five black minimalist gel pens" 
                         class="product-image w-full h-full object-cover">
                     <span class="absolute top-3 left-3 bg-primary-black text-white text-xs font-semibold px-2 py-0.5 rounded-full uppercase tracking-wider shadow-md">New</span>
                </div>
                <div class="p-4 text-center">
                    <h3 class="text-lg font-semibold text-primary-black mb-1">Gel Pen Set (5-Pack)</h3>
                    <p class="text-sm text-gray-500 mb-3">Smooth ink flow, 0.5mm tip.</p>
                    <div class="flex items-center justify-center">
                        <span class="text-xl font-bold text-primary-black">$12.00</span>
                    </div>
                    <span class="mt-3 inline-block w-full bg-primary-black text-white font-medium py-2 rounded-lg text-sm uppercase hover:bg-accent-gold transition duration-200">
                        View Item
                    </span>
                </div>
            </a>

            <!-- Product Card 4: Desk Calendar Pad (Out of Stock Example) -->
            <div class="product-card rounded-xl overflow-hidden opacity-60 bg-white" aria-label="A3 Desk Calendar Pad - Out of Stock">
                <div class="relative bg-gray-50 aspect-square overflow-hidden">
                    <img src="https://placehold.co/600x600/e0e0e0/4a4a4a?text=Calendar+Pad" 
                         alt="Desk calendar blotter pad, light gray" 
                         class="w-full h-full object-cover">
                    <div class="absolute inset-0 flex items-center justify-center bg-black bg-opacity-40">
                         <span class="text-white text-xl font-bold tracking-wider p-2 border-2 border-white">SOLD OUT</span>
                    </div>
                </div>
                <div class="p-4 text-center">
                    <h3 class="text-lg font-semibold text-gray-500 mb-1">A3 Desk Calendar Pad</h3>
                    <p class="text-sm text-gray-400 mb-3">Weekly planner, tear-off sheets.</p>
                    <div class="flex items-center justify-center">
                        <span class="text-xl font-bold text-gray-500">$34.50</span>
                    </div>
                    <!-- Disabled Button Style -->
                    <button disabled class="mt-3 inline-block w-full bg-gray-200 text-gray-500 font-medium py-2 rounded-lg text-sm uppercase cursor-not-allowed">
                        Unavailable
                    </button>
                </div>
            </div>

            <!-- Product Card 5: Solid Brass Ruler -->
            <a href="#" class="product-card block rounded-xl overflow-hidden bg-white" aria-label="View Solid Brass Ruler product details">
                <div class="relative bg-gray-50 aspect-square overflow-hidden">
                    <img src="https://placehold.co/600x600/b8860b/1a1a1a?text=Brass+Ruler" 
                         alt="Solid 12-inch brass ruler with etched markings" 
                         class="product-image w-full h-full object-cover">
                </div>
                <div class="p-4 text-center">
                    <h3 class="text-lg font-semibold text-primary-black mb-1">Solid Brass Ruler</h3>
                    <p class="text-sm text-gray-500 mb-3">12 inch, precise metric and imperial.</p>
                    <div class="flex items-center justify-center">
                        <span class="text-xl font-bold text-primary-black">$39.00</span>
                    </div>
                    <span class="mt-3 inline-block w-full bg-primary-black text-white font-medium py-2 rounded-lg text-sm uppercase hover:bg-accent-gold transition duration-200">
                        View Item
                    </span>
                </div>
            </a>

            <!-- Product Card 6: Desktop Stapler -->
            <a href="#" class="product-card block rounded-xl overflow-hidden bg-white" aria-label="View Minimalist Desktop Stapler product details">
                <div class="relative bg-gray-50 aspect-square overflow-hidden">
                    <img src="https://placehold.co/600x600/777777/ffffff?text=Stapler+Chrome" 
                         alt="Sleek silver chrome desktop stapler" 
                         class="product-image w-full h-full object-cover">
                </div>
                <div class="p-4 text-center">
                    <h3 class="text-lg font-semibold text-primary-black mb-1">Desktop Stapler</h3>
                    <p class="text-sm text-gray-500 mb-3">Heavy-duty, quiet operation.</p>
                    <div class="flex items-center justify-center">
                        <span class="text-xl font-bold text-primary-black">$22.50</span>
                    </div>
                    <span class="mt-3 inline-block w-full bg-primary-black text-white font-medium py-2 rounded-lg text-sm uppercase hover:bg-accent-gold transition duration-200">
                        View Item
                    </span>
                </div>
            </a>

            <!-- Product Card 7: Graphite Pencil Set -->
            <a href="#" class="product-card block rounded-xl overflow-hidden bg-white" aria-label="View Professional Graphite Pencil Set product details">
                <div class="relative bg-gray-50 aspect-square overflow-hidden">
                    <img src="https://placehold.co/600x600/333333/999999?text=Pencil+Set" 
                         alt="Set of twelve professional graphite pencils" 
                         class="product-image w-full h-full object-cover">
                    <span class="absolute top-3 right-3 bg-red-600 text-white text-xs font-semibold px-2 py-0.5 rounded-full uppercase tracking-wider shadow-md">30% Off</span>
                </div>
                <div class="p-4 text-center">
                    <h3 class="text-lg font-semibold text-primary-black mb-1">Graphite Pencil Set</h3>
                    <p class="text-sm text-gray-500 mb-3">12 grades from 6H to 8B.</p>
                    <div class="flex items-center justify-center space-x-2">
                        <span class="text-xl font-bold text-primary-black">$17.50</span>
                        <span class="text-sm text-gray-400 line-through">$25.00</span>
                    </div>
                    <span class="mt-3 inline-block w-full bg-primary-black text-white font-medium py-2 rounded-lg text-sm uppercase hover:bg-accent-gold transition duration-200">
                        View Item
                    </span>
                </div>
            </a>

            <!-- Product Card 8: Archival File Folders -->
            <a href="#" class="product-card block rounded-xl overflow-hidden bg-white" aria-label="View Archival File Folders product details">
                <div class="relative bg-gray-50 aspect-square overflow-hidden">
                    <img src="https://placehold.co/600x600/f5f5f5/555555?text=File+Folders" 
                         alt="Stack of minimalist white archival file folders" 
                         class="product-image w-full h-full object-cover">
                </div>
                <div class="p-4 text-center">
                    <h3 class="text-lg font-semibold text-primary-black mb-1">Archival File Folders</h3>
                    <p class="text-sm text-gray-500 mb-3">Set of 10, acid-free construction.</p>
                    <div class="flex items-center justify-center">
                        <span class="text-xl font-bold text-primary-black">$9.99</span>
                    </div>
                    <span class="mt-3 inline-block w-full bg-primary-black text-white font-medium py-2 rounded-lg text-sm uppercase hover:bg-accent-gold transition duration-200">
                        View Item
                    </span>
                </div>
            </a>

        </div>
        
        <!-- Call to Action/View More Button -->
        <div class="text-center mt-12">
             <a href="#" class="inline-block px-10 py-3 text-base font-semibold border-2 border-primary-black text-primary-black rounded-full hover:bg-primary-black hover:text-white transition duration-300 uppercase tracking-wider">
                    View Entire Collection
             </a>
        </div>

    </main>

    <!-- Footer: Utility and Contact Info -->
    <footer class="bg-primary-black mt-20">
        <div class="max-w-7xl mx-auto py-10 px-4 sm:px-6 lg:px-8 text-white">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
                <!-- Column 1: Brand -->
                <div>
                    <h4 class="text-lg font-bold mb-4 tracking-widest text-accent-gold">CLARITY</h4>
                    <p class="text-sm text-gray-400">Tools for focused living. Simple, beautiful, functional.</p>
                </div>
                <!-- Column 2: Quick Links -->
                <div>
                    <h4 class="text-lg font-semibold mb-4 border-b border-gray-700 pb-1">Shop</h4>
                    <ul class="space-y-2 text-sm">
                        <li><a href="#" class="text-gray-400 hover:text-accent-gold transition">New Arrivals</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-accent-gold transition">Notebooks</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-accent-gold transition">Writing</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-accent-gold transition">Sale Items</a></li>
                    </ul>
                </div>
                <!-- Column 3: Customer Service -->
                <div>
                    <h4 class="text-lg font-semibold mb-4 border-b border-gray-700 pb-1">Help</h4>
                    <ul class="space-y-2 text-sm">
                        <li><a href="#" class="text-gray-400 hover:text-accent-gold transition">Contact Us</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-accent-gold transition">Shipping & Returns</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-accent-gold transition">FAQ</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-accent-gold transition">Privacy Policy</a></li>
                    </ul>
                </div>
                <!-- Column 4: Newsletter -->
                <div>
                    <h4 class="text-lg font-semibold mb-4 border-b border-gray-700 pb-1">Stay Updated</h4>
                    <p class="text-sm text-gray-400 mb-4">Get 10% off your first order.</p>
                    <form>
                        <input type="email" placeholder="Enter your email" aria-label="Email for newsletter subscription" class="w-full p-2 text-sm text-primary-black bg-white rounded-md border-none focus:ring-accent-gold focus:border-accent-gold">
                        <button type="submit" class="w-full mt-2 bg-accent-gold text-primary-black font-bold py-2 rounded-md text-sm hover:bg-yellow-600 transition">Subscribe</button>
                    </form>
                </div>
            </div>
            
            <div class="text-center border-t border-gray-700 pt-8 mt-8">
                <p class="text-gray-500 text-xs">&copy; 2024 Clarity Store. All rights reserved. Designed for minimal focus.</p>
            </div>
        </div>
    </footer>

</body>
</html>
