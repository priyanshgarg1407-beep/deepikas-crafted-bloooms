<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deepika's Crafted Bloom • Handcrafted Candles & Eternal Flowers</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Inter:wght@300;400;500;600&display=swap');
       
        :root {
            --gold: #d4af37;
        }
       
        body {
            font-family: 'Inter', system-ui, sans-serif;
        }
       
        .heading-font {
            font-family: 'Playfair Display', sans-serif;
        }
 
        .hero-bg {
            background-image: linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)), url('https://picsum.photos/id/1015/2000/1200');
            background-size: cover;
            background-position: center;
        }
 
        .product-card {
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }
       
        .product-card:hover {
            transform: translateY(-12px);
            box-shadow: 0 25px 50px -12px rgb(0 0 0 / 0.25);
        }
 
        .nav-link {
            position: relative;
        }
       
        .nav-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -4px;
            left: 0;
            background-color: #d4af37;
            transition: all 0.3s ease;
        }
       
        .nav-link:hover:after {
            width: 100%;
        }
 
        .floral-divider {
            background: linear-gradient(90deg, transparent, #d4af37, transparent);
            height: 1px;
        }
    </style>
</head>
<body class="bg-[#f9f5f0] text-gray-800">
    <!-- Navbar -->
    <nav class="bg-white border-b border-gray-100 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-6 py-5 flex items-center justify-between">
            <div class="flex items-center gap-x-3">
                <div class="w-9 h-9 bg-[#d4af37] rounded-full flex items-center justify-center text-white text-2xl">🌸</div>
                <div>
                    <span class="heading-font text-2xl tracking-tight font-semibold">Deepika's</span>
                    <span class="heading-font text-2xl tracking-tight font-light text-amber-700">Crafted Bloom</span>
                </div>
            </div>
           
            <div class="hidden md:flex items-center gap-x-10 text-sm font-medium">
                <a href="#" onclick="navigateTo('shop')" class="nav-link cursor-pointer">Shop</a>
                <a href="#" onclick="navigateTo('candles')" class="nav-link cursor-pointer">Candles</a>
                <a href="#" onclick="navigateTo('blooms')" class="nav-link cursor-pointer">Eternal Blooms</a>
                <a href="#" onclick="navigateTo('resin')" class="nav-link cursor-pointer">Resin Art</a>
                <a href="#" onclick="navigateTo('about')" class="nav-link cursor-pointer">Our Story</a>
            </div>
           
            <div class="flex items-center gap-x-6">
                <button onclick="toggleSearch()" class="text-xl hover:text-amber-700 transition-colors">
                    <i class="fa-solid fa-magnifying-glass"></i>
                </button>
                <button onclick="toggleCart()" class="text-xl hover:text-amber-700 transition-colors relative">
                    <i class="fa-solid fa-bag-shopping"></i>
                    <span id="cart-count" class="absolute -top-1 -right-1 bg-rose-500 text-white text-[10px] w-4 h-4 flex items-center justify-center rounded-full">3</span>
                </button>
                <button class="md:hidden text-2xl">
                    <i class="fa-solid fa-bars"></i>
                </button>
            </div>
        </div>
    </nav>
 
    <!-- Hero -->
    <header class="hero-bg h-screen flex items-center text-white">
        <div class="max-w-4xl mx-auto px-6 text-center">
            <div class="inline-flex items-center gap-x-2 bg-white/20 backdrop-blur-md px-6 py-2 rounded-full text-sm mb-6">
                <span class="w-2 h-2 bg-emerald-400 rounded-full animate-pulse"></span>
                HANDCRAFTED IN INDIA
            </div>
            <h1 class="heading-font text-7xl md:text-8xl font-light tracking-tighter leading-none mb-6">
                Blooms that<br>never fade.<br>Flames that<br>heal the soul.
            </h1>
            <p class="max-w-md mx-auto text-lg text-white/80 mb-10">
                Timeless candles, preserved flowers &amp; resin treasures crafted with love by Deepika.
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <button onclick="navigateTo('shop')"
                        class="bg-white text-black px-10 py-6 rounded-2xl font-medium hover:bg-amber-100 transition-all flex items-center justify-center gap-x-3 group">
                    SHOP COLLECTION
                    <span class="group-active:rotate-45 transition-transform">→</span>
                </button>
                <button onclick="navigateTo('about')"
                        class="border border-white/70 hover:bg-white/10 px-8 py-6 rounded-2xl font-medium transition-all">
                    MEET DEEPIKA
                </button>
            </div>
            <div class="mt-16 flex justify-center gap-x-8 text-xs tracking-widest">
                <div class="flex items-center gap-x-2">
                    <i class="fa-solid fa-leaf text-emerald-300"></i>
                    <span>NATURAL SOY WAX</span>
                </div>
                <div class="flex items-center gap-x-2">
                    <i class="fa-solid fa-seedling text-emerald-300"></i>
                    <span>ETERNAL PRESERVED BLOOMS</span>
                </div>
            </div>
        </div>
       
        <div class="absolute bottom-10 left-1/2 flex flex-col items-center">
            <div class="text-xs tracking-[3px] mb-3 opacity-70">SCROLL TO EXPLORE</div>
            <div class="w-px h-12 bg-gradient-to-b from-transparent via-white to-transparent"></div>
        </div>
    </header>
 
    <!-- Trust Bar -->
    <div class="bg-white py-5 border-b">
        <div class="max-w-6xl mx-auto flex flex-wrap justify-center items-center gap-x-10 gap-y-4 text-sm text-gray-500">
            <div class="flex items-center gap-x-3">
                <i class="fa-solid fa-truck text-amber-700"></i>
                <span>Free shipping on orders above ₹5000</span>
            </div>
            <div class="flex items-center gap-x-3">
                <i class="fa-solid fa-shield-halved text-amber-700"></i>
                <span>1 Year Craftsmanship Warranty</span>
            </div>
            <div class="flex items-center gap-x-3">
                <i class="fa-solid fa-gem text-amber-700"></i>
                <span>Premium &amp; Ethical Materials</span>
            </div>
        </div>
    </div>
 
    <!-- Featured Products -->
    <section id="shop" class="max-w-7xl mx-auto px-6 py-24">
        <div class="flex justify-between items-end mb-12">
            <div>
                <span class="uppercase text-amber-700 text-sm tracking-widest font-medium">Signature Collection</span>
                <h2 class="heading-font text-5xl font-light">Crafted with Intention</h2>
            </div>
            <a href="#" onclick="navigateTo('shop')" class="group flex items-center gap-x-2 text-sm font-medium">
                VIEW ALL
                <span class="transition-transform group-hover:translate-x-1">→</span>
            </a>
        </div>
       
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
            <!-- Product 1 -->
            <div class="product-card bg-white rounded-3xl overflow-hidden group">
                <div class="h-80 bg-[#f5e8d3] relative">
                    <img src=”IMG_6861.jpeg” alt="Golden Hour Candle"
                         class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute top-5 right-5 bg-white text-xs font-medium px-4 py-2 rounded-2xl shadow">Bestseller</div>
                </div>
                <div class="p-6">
                    <div class="flex justify-between">
                        <div>
                            <h3 class="font-medium">Golden Hour Bloom Candle</h3>
                            <p class="text-sm text-gray-500">Sandalwood • Rose • Vanilla</p>
                        </div>
                        <div class="text-right">
                            <span class="font-semibold">₹1,890</span>
                        </div>
                    </div>
                    <button onclick="addToCart(this)"
                            class="mt-6 w-full bg-amber-900 hover:bg-black text-white py-4 rounded-2xl text-sm tracking-wider transition-colors">
                        ADD TO BASKET
                    </button>
                </div>
            </div>
           
            <!-- Product 2 -->
            <div class="product-card bg-white rounded-3xl overflow-hidden group">
                <div class="h-80 bg-[#f0e4e8] relative">
                    <img src="https://picsum.photos/id/201/600/800" alt="Eternal Rose"
                         class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                </div>
                <div class="p-6">
                    <div class="flex justify-between">
                        <div>
                            <h3 class="font-medium">Preserved Rose Bell Jar</h3>
                            <p class="text-sm text-gray-500">Lasts forever • Gift-ready</p>
                        </div>
                        <div class="text-right">
                            <span class="font-semibold">₹3,450</span>
                        </div>
                    </div>
                    <button onclick="addToCart(this)"
                            class="mt-6 w-full bg-amber-900 hover:bg-black text-white py-4 rounded-2xl text-sm tracking-wider transition-colors">
                        ADD TO BASKET
                    </button>
                </div>
            </div>
           
            <!-- Product 3 -->
            <div class="product-card bg-white rounded-3xl overflow-hidden group">
                <div class="h-80 bg-[#e8f0f5] relative">
                    <img src="https://picsum.photos/id/870/600/800" alt="Resin Tray"
                         class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                </div>
                <div class="p-6">
                    <div class="flex justify-between">
                        <div>
                            <h3 class="font-medium">Floral Resin Serving Tray</h3>
                            <p class="text-sm text-gray-500">Real dried flowers</p>
                        </div>
                        <div class="text-right">
                            <span class="font-semibold">₹2,690</span>
                        </div>
                    </div>
                    <button onclick="addToCart(this)"
                            class="mt-6 w-full bg-amber-900 hover:bg-black text-white py-4 rounded-2xl text-sm tracking-wider transition-colors">
                        ADD TO BASKET
                    </button>
                </div>
            </div>
           
            <!-- Product 4 -->
            <div class="product-card bg-white rounded-3xl overflow-hidden group">
                <div class="h-80 bg-[#f5f0e8] relative">
                    <img src="https://picsum.photos/id/106/600/800" alt="Gift Set"
                         class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute top-5 left-5 bg-rose-500 text-white text-xs font-medium px-4 py-2 rounded-2xl">Limited</div>
                </div>
                <div class="p-6">
                    <div class="flex justify-between">
                        <div>
                            <h3 class="font-medium">The Bridal Bloom Box</h3>
                            <p class="text-sm text-gray-500">Candle + Resin + Flowers</p>
                        </div>
                        <div class="text-right">
                            <span class="font-semibold">₹6,800</span>
                        </div>
                    </div>
                    <button onclick="addToCart(this)"
                            class="mt-6 w-full bg-amber-900 hover:bg-black text-white py-4 rounded-2xl text-sm tracking-wider transition-colors">
                        ADD TO BASKET
                    </button>
                </div>
            </div>
        </div>
    </section>
 
    <!-- Instagram Inspired Gallery -->
    <section class="bg-[#0a0a0a] py-20 text-white">
        <div class="max-w-7xl mx-auto px-6">
            <div class="flex justify-between items-center mb-10">
                <h2 class="heading-font text-5xl font-light">@deepikascraftedblooms</h2>
                <a href="https://www.instagram.com/deepikascraftedblooms/" target="_blank"
                   class="flex items-center gap-x-2 border border-white/30 hover:border-white px-6 py-3 rounded-2xl text-sm">
                    <i class="fa-brands fa-instagram"></i>
                    FOLLOW ON INSTAGRAM
                </a>
            </div>
           
            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4">
                <img src="https://picsum.photos/id/1015/600/600" class="aspect-square object-cover rounded-3xl hover:scale-105 transition-transform cursor-pointer" alt="">
                <img src="https://picsum.photos/id/201/600/600" class="aspect-square object-cover rounded-3xl hover:scale-105 transition-transform cursor-pointer" alt="">
                <img src="https://picsum.photos/id/870/600/600" class="aspect-square object-cover rounded-3xl hover:scale-105 transition-transform cursor-pointer" alt="">
                <img src="https://picsum.photos/id/106/600/600" class="aspect-square object-cover rounded-3xl hover:scale-105 transition-transform cursor-pointer" alt="">
                <img src="https://picsum.photos/id/133/600/600" class="aspect-square object-cover rounded-3xl hover:scale-105 transition-transform cursor-pointer" alt="">
                <img src="https://picsum.photos/id/180/600/600" class="aspect-square object-cover rounded-3xl hover:scale-105 transition-transform cursor-pointer" alt="">
            </div>
        </div>
    </section>
 
    <!-- About Deepika -->
    <section id="about" class="max-w-7xl mx-auto px-6 py-24 grid md:grid-cols-2 gap-16 items-center">
        <div>
            <img src="https://picsum.photos/id/64/800/900" alt="Deepika"
                 class="rounded-3xl shadow-2xl">
        </div>
        <div class="space-y-8">
            <div class="uppercase text-amber-700 text-sm tracking-widest">Our Founder &amp; Artisan</div>
            <h2 class="heading-font text-6xl leading-none font-light">Every piece tells a story of patience, love, and quiet beauty.</h2>
            <p class="text-lg leading-relaxed text-gray-600">
                Hi, I'm Deepika. What began as a passion for creating beautiful things for my own home has grown into Deepika's Crafted Bloom — a small studio where I hand-pour every candle, preserve every bloom, and craft every resin piece with utmost care.
            </p>
            <p class="text-lg leading-relaxed text-gray-600">
                My goal is simple: to bring warmth, elegance, and moments of mindfulness into your everyday spaces.
            </p>
            <div class="pt-6 border-t flex items-center gap-x-8">
                <div>
                    <div class="text-4xl font-light">500+</div>
                    <div class="text-sm">Happy Homes</div>
                </div>
                <div>
                    <div class="text-4xl font-light">100%</div>
                    <div class="text-sm">Handcrafted</div>
                </div>
            </div>
            <button onclick="alert('Thank you for wanting to know more about my journey ❤️')"
                    class="border border-amber-900 px-8 py-5 rounded-2xl hover:bg-amber-50 transition-colors">
                READ MY JOURNEY
            </button>
        </div>
    </section>
 
    <!-- Footer -->
    <footer class="bg-[#111] text-gray-300">
        <div class="max-w-7xl mx-auto px-6 pt-20 pb-12">
            <div class="grid grid-cols-2 md:grid-cols-5 gap-y-12">
                <div>
                    <div class="flex items-center gap-x-3 text-white mb-6">
                        <div class="w-8 h-8 bg-amber-400 rounded-full flex items-center justify-center text-xl">🌺</div>
                        <span class="heading-font text-2xl">Deepika's Crafted Bloom</span>
                    </div>
                    <p class="text-sm leading-relaxed max-w-xs">
                        Handcrafted candles, eternal flowers &amp; resin art from a small studio in India.
                    </p>
                </div>
               
                <div>
                    <div class="font-medium text-white mb-4">Shop</div>
                    <div class="space-y-2 text-sm">
                        <div class="cursor-pointer hover:text-white">Signature Candles</div>
                        <div class="cursor-pointer hover:text-white">Eternal Blooms</div>
                        <div class="cursor-pointer hover:text-white">Resin Treasures</div>
                        <div class="cursor-pointer hover:text-white">Gift Collections</div>
                    </div>
                </div>
               
                <div>
                    <div class="font-medium text-white mb-4">Learn</div>
                    <div class="space-y-2 text-sm">
                        <div class="cursor-pointer hover:text-white">Our Story</div>
                        <div class="cursor-pointer hover:text-white">Journal</div>
                        <div class="cursor-pointer hover:text-white">Craft Process</div>
                        <div class="cursor-pointer hover:text-white">Sustainability</div>
                    </div>
                </div>
               
                <div>
                    <div class="font-medium text-white mb-4">Connect</div>
                    <div class="space-y-2 text-sm">
                        <a href="https://www.instagram.com/deepikascraftedblooms/" target="_blank" class="flex items-center gap-x-2 hover:text-white">
                            <i class="fa-brands fa-instagram"></i> @deepikascraftedblooms
                        </a>
                        <div class="cursor-pointer hover:text-white">WhatsApp</div>
                        <div class="cursor-pointer hover:text-white">Email Us</div>
                    </div>
                </div>
               
                <div>
                    <div class="font-medium text-white mb-4">Newsletter</div>
                    <p class="text-xs mb-4">Monthly drops, stories from the studio &amp; early access to new collections.</p>
                    <div class="flex">
                        <input type="email" placeholder="your@email.com"
                               class="bg-white/10 border border-white/20 rounded-l-2xl px-5 py-4 text-sm flex-1 focus:outline-none">
                        <button class="bg-amber-400 text-black px-8 rounded-r-2xl font-medium">→</button>
                    </div>
                </div>
            </div>
           
            <div class="floral-divider my-16"></div>
           
            <div class="text-xs flex flex-col md:flex-row justify-between items-center gap-y-4 text-gray-500">
                <div>© 2026 Deepika's Crafted Bloom. All rights reserved.</div>
                <div class="flex gap-x-6">
                    <span class="cursor-pointer hover:text-gray-300">Privacy</span>
                    <span class="cursor-pointer hover:text-gray-300">Shipping</span>
                    <span class="cursor-pointer hover:text-gray-300">Returns</span>
                </div>
                <div>Made with ❤️ in India</div>
            </div>
        </div>
    </footer>
 
    <!-- Cart Sidebar -->
    <div id="cart-sidebar" class="fixed top-0 right-0 h-full w-full max-w-md bg-white shadow-2xl translate-x-full transition-transform duration-500 z-[100] flex flex-col">
        <div class="p-6 border-b flex justify-between items-center">
            <h3 class="text-2xl font-light">Your Basket</h3>
            <button onclick="toggleCart()" class="text-3xl leading-none">×</button>
        </div>
       
        <div id="cart-items" class="flex-1 p-6 overflow-auto space-y-8">
            <!-- JS populated -->
        </div>
       
        <div class="p-6 border-t">
            <div class="flex justify-between text-lg mb-6">
                <span>Total</span>
                <span id="cart-total" class="font-semibold">₹0</span>
            </div>
            <button onclick="checkout()"
                    class="w-full bg-gradient-to-r from-amber-900 to-black text-white py-6 rounded-3xl text-sm tracking-widest">
                PROCEED TO CHECKOUT
            </button>
            <p class="text-center text-xs mt-6 text-gray-400">or 4 interest-free payments of ₹X with</p>
        </div>
    </div>
 
    <script>
        // Tailwind script already included
       
        function navigateTo(section) {
            document.getElementById(section).scrollIntoView({ behavior: "smooth" });
        }
       
        let cart = [];
       
        function addToCart(btn) {
            const productName = btn.parentElement.querySelector('h3').textContent;
            const priceText = btn.parentElement.querySelector('.font-semibold').textContent;
            const price = parseInt(priceText.replace('₹', '').replace(',', ''));
           
            cart.push({
                name: productName,
                price: price,
                qty: 1
            });
           
            updateCartCount();
            renderCart();
           
            // Visual feedback
            btn.textContent = "ADDED ✓";
            setTimeout(() => {
                btn.textContent = "ADD TO BASKET";
            }, 1500);
        }
       
        function updateCartCount() {
            document.getElementById('cart-count').textContent = cart.length;
        }
       
        function renderCart() {
            const container = document.getElementById('cart-items');
            let html = '';
            let total = 0;
           
            cart.forEach((item, index) => {
                total += item.price * item.qty;
                html += `
                    <div class="flex gap-4">
                        <div class="w-20 h-20 bg-gray-100 rounded-2xl flex-shrink-0"></div>
                        <div class="flex-1">
                            <div class="flex justify-between">
                                <div class="font-medium">${item.name}</div>
                                <div class="text-sm font-medium">₹${item.price}</div>
                            </div>
                            <div class="flex items-center gap-x-4 mt-3 text-sm">
                                <button onclick="changeQty(${index}, -1)" class="w-6 h-6 border flex items-center justify-center hover:bg-gray-100 rounded">-</button>
                                <span>${item.qty}</span>
                                <button onclick="changeQty(${index}, 1)" class="w-6 h-6 border flex items-center justify-center hover:bg-gray-100 rounded">+</button>
                                <button onclick="removeFromCart(${index})" class="ml-auto text-rose-500 text-xs">Remove</button>
                            </div>
                        </div>
                    </div>
                `;
            });
           
            container.innerHTML = html || `<div class="h-full flex items-center justify-center text-gray-400">Your basket is empty</div>`;
            document.getElementById('cart-total').textContent = `₹${total}`;
        }
       
        function changeQty(index, change) {
            cart[index].qty += change;
            if (cart[index].qty < 1) cart[index].qty = 1;
            renderCart();
        }
       
        function removeFromCart(index) {
            cart.splice(index, 1);
            updateCartCount();
            renderCart();
        }
       
        function toggleCart() {
            const sidebar = document.getElementById('cart-sidebar');
            if (sidebar.classList.contains('translate-x-full')) {
                sidebar.classList.remove('translate-x-full');
                renderCart();
            } else {
                sidebar.classList.add('translate-x-full');
            }
        }
       
        function toggleSearch() {
            alert("Search coming soon ✨\nTry our bestselling Golden Hour Bloom Candle!");
        }
       
        function checkout() {
            if (cart.length === 0) return;
            alert("Thank you for shopping with Deepika's Crafted Bloom!\n\n(This is a demo website. In a real store this would take you to payment.)");
            cart = [];
            updateCartCount();
            toggleCart();
        }
       
        // Keyboard escape support
        document.addEventListener('keydown', function(e) {
            if (e.key === "Escape") {
                const sidebar = document.getElementById('cart-sidebar');
                if (!sidebar.classList.contains('translate-x-full')) {
                    toggleCart();
                }
            }
        });
       
        // Initialize
        window.onload = function() {
            console.log("%cDeepika's Crafted Bloom - Premium Demo Website Ready 🌸", "color:#d4af37; font-family:Playfair Display; font-size:13px");
        };
    </script>
</body>
</html>
 
