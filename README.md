<!DOCTYPE html>
<html lang="ar" dir="rtl" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أمبير للبطاريات | Ampere Batteries - طاقة تدوم ورعاية متكاملة لسيارتك</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Font - Cairo -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;800;900&display=swap" rel="stylesheet">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            dark: '#0A3A2A',     /* أخضر داكن فاخر */
                            primary: '#10B981',  /* أخضر حيوى (Emerald) */
                            light: '#ECFDF5',    /* أخضر فاتح خلفية */
                            accent: '#059669',   /* أخضر متوسط للتأثيرات */
                            gold: '#F59E0B'      /* لون إضافي للتقييمات */
                        }
                    },
                    fontFamily: {
                        cairo: ['Cairo', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Cairo', sans-serif;
        }
        .bg-grid-pattern {
            background-image: radial-gradient(rgba(16, 185, 129, 0.15) 1px, transparent 1px);
            background-size: 24px 24px;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 antialiased flex flex-col min-h-screen">

    <!-- Header / Navbar -->
    <header class="sticky top-0 z-40 bg-white/95 backdrop-blur-md border-b border-slate-100 shadow-sm">
        <!-- Top Bar for Quick Info & Emergency -->
        <div class="bg-brand-dark text-white text-xs py-2 px-4">
            <div class="max-w-7xl mx-auto flex flex-wrap justify-between items-center gap-2">
                <div class="flex items-center gap-4">
                    <span class="flex items-center gap-1.5"><i class="fa-solid fa-phone-volume text-brand-primary animate-pulse"></i> طوارئ الطريق: <a href="tel:920000000" class="font-bold underline hover:text-brand-primary">920000000</a></span>
                    <span class="hidden md:inline-block text-slate-400">|</span>
                    <span class="hidden md:inline-flex items-center gap-1"><i class="fa-solid fa-truck-fast text-brand-primary"></i> خدمة التوصيل والتركيب الميداني خلال 30 دقيقة</span>
                </div>
                <div class="flex items-center gap-3">
                    <span class="flex items-center gap-1"><i class="fa-solid fa-clock text-slate-300"></i> خدمة 24/7</span>
                </div>
            </div>
        </div>

        <!-- Main Navigation -->
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                
                <!-- Logo -->
                <a href="#" class="flex items-center gap-3 group">
                    <div class="w-12 h-12 bg-brand-dark rounded-xl flex items-center justify-center text-brand-primary font-black text-2xl shadow-lg group-hover:bg-brand-primary group-hover:text-white transition-all duration-300">
                        <i class="fa-solid fa-bolt"></i>
                    </div>
                    <div>
                        <span class="text-2xl font-black text-brand-dark tracking-tight block">أمبيـــر <span class="text-brand-primary">.</span></span>
                        <span class="text-[10px] text-slate-500 font-bold uppercase tracking-widest block -mt-1">Ampere Batteries</span>
                    </div>
                </a>

                <!-- Desktop Navigation Links -->
                <nav class="hidden lg:flex items-center gap-8 font-semibold text-slate-700">
                    <a href="#hero" class="hover:text-brand-primary transition-colors py-2 border-b-2 border-brand-primary text-brand-primary">الرئيسية</a>
                    <a href="#finder" class="hover:text-brand-primary transition-colors py-2 border-b-2 border-transparent hover:border-brand-primary">ابحث عن بطاريتك</a>
                    <a href="#products" class="hover:text-brand-primary transition-colors py-2 border-b-2 border-transparent hover:border-brand-primary">المنتجات</a>
                    <a href="#services" class="hover:text-brand-primary transition-colors py-2 border-b-2 border-transparent hover:border-brand-primary">خدماتنا</a>
                    <a href="#testimonials" class="hover:text-brand-primary transition-colors py-2 border-b-2 border-transparent hover:border-brand-primary">آراء العملاء</a>
                    <a href="#contact" class="hover:text-brand-primary transition-colors py-2 border-b-2 border-transparent hover:border-brand-primary">اتصل بنا</a>
                </nav>

                <!-- Header Actions -->
                <div class="flex items-center gap-3">
                    <!-- Cart Button -->
                    <button id="cartBtn" onclick="toggleCart()" class="relative p-3 bg-brand-light hover:bg-emerald-100 text-brand-dark rounded-xl transition-all flex items-center justify-center">
                        <i class="fa-solid fa-cart-shopping text-lg"></i>
                        <span id="cartCount" class="absolute -top-1 -right-1 bg-brand-primary text-white text-xs font-bold w-5 h-5 rounded-full flex items-center justify-center border-2 border-white">0</span>
                    </button>

                    <!-- Fast Call Button -->
                    <a href="tel:920000000" class="hidden sm:flex items-center gap-2 bg-brand-primary hover:bg-brand-accent text-white px-5 py-2.5 rounded-xl font-bold shadow-md shadow-emerald-200 transition-all transform active:scale-95">
                        <i class="fa-solid fa-headset"></i>
                        <span>اطلب فني الآن</span>
                    </a>

                    <!-- Mobile Menu Toggle Button -->
                    <button id="mobileMenuBtn" onclick="toggleMobileMenu()" class="lg:hidden p-2.5 text-slate-700 hover:text-brand-primary rounded-lg focus:outline-none">
                        <i class="fa-solid fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu Drawer -->
        <div id="mobileMenu" class="hidden lg:hidden bg-white border-b border-slate-200 px-4 pt-2 pb-6 space-y-3">
            <a href="#hero" onclick="toggleMobileMenu()" class="block py-2 text-slate-800 font-bold hover:text-brand-primary">الرئيسية</a>
            <a href="#finder" onclick="toggleMobileMenu()" class="block py-2 text-slate-800 font-bold hover:text-brand-primary">ابحث عن بطاريتك</a>
            <a href="#products" onclick="toggleMobileMenu()" class="block py-2 text-slate-800 font-bold hover:text-brand-primary">المنتجات</a>
            <a href="#services" onclick="toggleMobileMenu()" class="block py-2 text-slate-800 font-bold hover:text-brand-primary">خدماتنا</a>
            <a href="#testimonials" onclick="toggleMobileMenu()" class="block py-2 text-slate-800 font-bold hover:text-brand-primary">آراء العملاء</a>
            <a href="#contact" onclick="toggleMobileMenu()" class="block py-2 text-slate-800 font-bold hover:text-brand-primary">اتصل بنا</a>
            <a href="tel:920000000" class="flex items-center justify-center gap-2 bg-brand-primary text-white py-3 rounded-xl font-bold">
                <i class="fa-solid fa-phone"></i>
                <span>اتصل بنا فوراً: 920000000</span>
            </a>
        </div>
    </header>

    <main class="flex-grow">
        
        <!-- Hero Section -->
        <section id="hero" class="relative bg-brand-dark text-white overflow-hidden py-16 lg:py-24">
            <!-- Background Glow & Pattern -->
            <div class="absolute inset-0 bg-grid-pattern opacity-20"></div>
            <div class="absolute -top-24 -right-24 w-96 h-96 bg-brand-primary/20 rounded-full blur-3xl"></div>
            <div class="absolute bottom-0 left-0 w-80 h-80 bg-brand-primary/10 rounded-full blur-2xl"></div>

            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
                <div class="grid lg:grid-cols-12 gap-12 items-center">
                    
                    <!-- Text Content -->
                    <div class="lg:col-span-7 space-y-6 text-center lg:text-right">
                        <div class="inline-flex items-center gap-2 bg-white/10 backdrop-blur-md border border-white/20 px-4 py-1.5 rounded-full text-brand-primary text-sm font-semibold">
                            <span class="w-2 h-2 rounded-full bg-brand-primary animate-ping"></span>
                            المتجر الأول المعتمد لبطاريات السيارات
                        </div>
                        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-black leading-tight">
                            تعطلت بطاريتك؟ <br>
                            <span class="text-transparent bg-clip-text bg-gradient-to-l from-brand-primary to-emerald-200">نصلك ونركبها في موقعك</span>
                        </h1>
                        <p class="text-slate-300 text-lg max-w-2xl mx-auto lg:mx-0 font-light leading-relaxed">
                            أحصل على بطارية سيارات أصلية مع ضمان يصل إلى 24 شهراً. خدمة التوصيل، التركيب، وفحص نظام الشحن الكهربائي مجاناً أمام بيتك أو في الطريق.
                        </p>

                        <!-- Quick Actions -->
                        <div class="pt-4 flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4">
                            <a href="#finder" class="w-full sm:w-auto bg-brand-primary hover:bg-brand-accent text-white font-bold px-8 py-4 rounded-xl shadow-lg shadow-emerald-900/50 flex items-center justify-center gap-3 transition-all transform hover:-translate-y-1">
                                <i class="fa-solid fa-car"></i>
                                <span>اختر بطارية سيارتك</span>
                            </a>
                            <a href="tel:920000000" class="w-full sm:w-auto bg-white/10 hover:bg-white/20 text-white font-bold px-8 py-4 rounded-xl border border-white/20 flex items-center justify-center gap-3 transition-all">
                                <i class="fa-solid fa-phone-flip text-brand-primary"></i>
                                <span>طلب امداد سريع 24/7</span>
                            </a>
                        </div>

                        <!-- Stats Highlights -->
                        <div class="pt-8 border-t border-white/10 grid grid-cols-3 gap-4 text-center lg:text-right">
                            <div>
                                <p class="text-2xl lg:text-3xl font-black text-brand-primary">+50K</p>
                                <p class="text-xs text-slate-400 font-medium">عميل راضٍ</p>
                            </div>
                            <div>
                                <p class="text-2xl lg:text-3xl font-black text-brand-primary">30 دقيقة</p>
                                <p class="text-xs text-slate-400 font-medium">متوسط سرعة الوصول</p>
                            </div>
                            <div>
                                <p class="text-2xl lg:text-3xl font-black text-brand-primary">100%</p>
                                <p class="text-xs text-slate-400 font-medium">منتجات أصلية وضمان</p>
                            </div>
                        </div>
                    </div>

                    <!-- Visual / Hero Image Banner -->
                    <div class="lg:col-span-5 relative flex justify-center">
                        <div class="relative w-full max-w-md bg-gradient-to-b from-white/10 to-white/5 border border-white/10 rounded-3xl p-6 backdrop-blur-md shadow-2xl">
                            <!-- Card Header Badge -->
                            <div class="flex justify-between items-center mb-6">
                                <span class="bg-brand-primary text-slate-900 text-xs font-bold px-3 py-1 rounded-md">أعلى جودة</span>
                                <div class="flex items-center text-brand-gold text-sm gap-1">
                                    <i class="fa-solid fa-star"></i>
                                    <i class="fa-solid fa-star"></i>
                                    <i class="fa-solid fa-star"></i>
                                    <i class="fa-solid fa-star"></i>
                                    <i class="fa-solid fa-star"></i>
                                </div>
                            </div>
                            
                            <!-- Battery Mockup / Graphic -->
                            <div class="py-8 flex justify-center items-center relative">
                                <div class="w-48 h-48 bg-emerald-500/10 rounded-full absolute animate-ping"></div>
                                <div class="relative z-10 text-center">
                                    <i class="fa-solid fa-car-battery text-8xl text-brand-primary drop-shadow-[0_10px_10px_rgba(0,0,0,0.5)]"></i>
                                    <div class="mt-4 bg-brand-dark/80 px-4 py-2 rounded-xl border border-brand-primary/30 inline-block">
                                        <p class="text-xs text-slate-300">تقنية AGM & EFB اليابانية والكورية</p>
                                    </div>
                                </div>
                            </div>

                            <!-- Features List -->
                            <div class="space-y-2 pt-4 border-t border-white/10 text-xs text-slate-300">
                                <div class="flex items-center gap-2">
                                    <i class="fa-solid fa-circle-check text-brand-primary"></i>
                                    <span>شاملة الفحص والتركيب في الموقع</span>
                                </div>
                                <div class="flex items-center gap-2">
                                    <i class="fa-solid fa-circle-check text-brand-primary"></i>
                                    <span>ضمان حقيقي يستبدل فورياً</span>
                                </div>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <!-- Battery Finder Widget Section -->
        <section id="finder" class="relative -mt-10 z-20 max-w-5xl mx-auto px-4">
            <div class="bg-white rounded-3xl shadow-2xl border border-slate-100 p-6 md:p-8">
                <div class="text-center max-w-xl mx-auto mb-6">
                    <span class="text-brand-accent font-bold text-sm tracking-wide">أداة البحث الذكية</span>
                    <h2 class="text-2xl md:text-3xl font-black text-brand-dark mt-1">ابحث عن البطارية المناسبة لسيارتك</h2>
                    <p class="text-slate-500 text-sm mt-1">حدد مواصفات سيارتك وسنظهر لك البطاريات المتوافقة 100%</p>
                </div>

                <form id="batteryFinderForm" onsubmit="searchBatteries(event)" class="grid grid-cols-1 md:grid-cols-4 gap-4">
                    <!-- Step 1: Make -->
                    <div>
                        <label class="block text-xs font-bold text-slate-700 mb-2"><i class="fa-solid fa-car-side text-brand-primary ml-1"></i> ماركة السيارة</label>
                        <select id="carMake" onchange="updateModels()" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-4 py-3 text-sm font-semibold text-slate-700 focus:outline-none focus:border-brand-primary focus:ring-2 focus:ring-brand-primary/20">
                            <option value="">اختر الماركة...</option>
                            <option value="toyota">تويوتا (Toyota)</option>
                            <option value="hyundai">هيونداي (Hyundai)</option>
                            <option value="ford">فورد (Ford)</option>
                            <option value="nissan">نيسان (Nissan)</option>
                            <option value="gmc">جي إم سي / شفروليه</option>
                        </select>
                    </div>

                    <!-- Step 2: Model -->
                    <div>
                        <label class="block text-xs font-bold text-slate-700 mb-2"><i class="fa-solid fa-car-rear text-brand-primary ml-1"></i> موديل السيارة</label>
                        <select id="carModel" disabled class="w-full bg-slate-50 border border-slate-200 rounded-xl px-4 py-3 text-sm font-semibold text-slate-700 focus:outline-none focus:border-brand-primary focus:ring-2 focus:ring-brand-primary/20 disabled:opacity-50">
                            <option value="">اختر الموديل...</option>
                        </select>
                    </div>

                    <!-- Step 3: Year -->
                    <div>
                        <label class="block text-xs font-bold text-slate-700 mb-2"><i class="fa-solid fa-calendar-days text-brand-primary ml-1"></i> سنة الصنع</label>
                        <select id="carYear" disabled class="w-full bg-slate-50 border border-slate-200 rounded-xl px-4 py-3 text-sm font-semibold text-slate-700 focus:outline-none focus:border-brand-primary focus:ring-2 focus:ring-brand-primary/20 disabled:opacity-50">
                            <option value="">اختر السنة...</option>
                        </select>
                    </div>

                    <!-- Submit Button -->
                    <div class="flex items-end">
                        <button type="submit" class="w-full bg-brand-dark hover:bg-brand-primary text-white font-bold py-3.5 px-6 rounded-xl transition-all flex items-center justify-center gap-2 shadow-md">
                            <i class="fa-solid fa-magnifying-glass"></i>
                            <span>اعرض النتائج</span>
                        </button>
                    </div>
                </form>
            </div>
        </section>

        <!-- Products Section -->
        <section id="products" class="py-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-12 gap-4">
                <div>
                    <span class="text-brand-accent font-bold text-sm tracking-wide">المنتجات الأكثر مبيعاً</span>
                    <h2 class="text-3xl md:text-4xl font-black text-brand-dark mt-1">بطاريات معتمدة عالية الأداء</h2>
                </div>

                <!-- Product Filters -->
                <div class="flex flex-wrap gap-2" id="filterButtons">
                    <button onclick="filterProducts('all')" class="filter-btn active bg-brand-dark text-white font-bold px-4 py-2 rounded-xl text-sm transition-all">الكل</button>
                    <button onclick="filterProducts('80ah')" class="filter-btn bg-white text-slate-600 border border-slate-200 font-semibold px-4 py-2 rounded-xl text-sm hover:border-brand-primary transition-all">70 - 80 أمبير</button>
                    <button onclick="filterProducts('60ah')" class="filter-btn bg-white text-slate-600 border border-slate-200 font-semibold px-4 py-2 rounded-xl text-sm hover:border-brand-primary transition-all">50 - 60 أمبير</button>
                    <button onclick="filterProducts('agm')" class="filter-btn bg-white text-slate-600 border border-slate-200 font-semibold px-4 py-2 rounded-xl text-sm hover:border-brand-primary transition-all">تقنية AGM</button>
                </div>
            </div>

            <!-- Products Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8" id="productsGrid">
                <!-- Products dynamically rendered by JS -->
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="py-20 bg-brand-light relative">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-2xl mx-auto mb-16">
                    <span class="text-brand-accent font-bold text-sm tracking-wide">لماذا نعد الأفضل؟</span>
                    <h2 class="text-3xl md:text-4xl font-black text-brand-dark mt-1">خدمات متكاملة تصلك أينما كنت</h2>
                    <p class="text-slate-600 mt-2">نحن لا نبيع البطاريات فقط، بل نقدم خدمة العناية الكاملة بالمنظومة الكهربائية لسيارتك.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <!-- Service 1 -->
                    <div class="bg-white p-8 rounded-3xl border border-emerald-100/50 shadow-sm hover:shadow-xl transition-all duration-300 group">
                        <div class="w-16 h-16 bg-brand-light rounded-2xl flex items-center justify-center text-brand-primary text-2xl font-black mb-6 group-hover:bg-brand-primary group-hover:text-white transition-all">
                            <i class="fa-solid fa-truck-ramp-box"></i>
                        </div>
                        <h3 class="text-xl font-bold text-brand-dark mb-3">التوصيل والتركيب السريع</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            فريق من الفنيين المحترفين يصلك خلال 30 دقيقة داخل المدينة لتركيب البطارية بأسلوب احترافي وبدون فقدان إعدادات السيارة.
                        </p>
                    </div>

                    <!-- Service 2 -->
                    <div class="bg-white p-8 rounded-3xl border border-emerald-100/50 shadow-sm hover:shadow-xl transition-all duration-300 group">
                        <div class="w-16 h-16 bg-brand-light rounded-2xl flex items-center justify-center text-brand-primary text-2xl font-black mb-6 group-hover:bg-brand-primary group-hover:text-white transition-all">
                            <i class="fa-solid fa-microchip"></i>
                        </div>
                        <h3 class="text-xl font-bold text-brand-dark mb-3">فحص كمبيوتر والدينامو</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            قبل تغيير البطارية، يقوم الفني بفحص شامل لدينامو الشحن وتسريب الكهرباء للتأكد من أن المشكلة من البطارية فعلاً.
                        </p>
                    </div>

                    <!-- Service 3 -->
                    <div class="bg-white p-8 rounded-3xl border border-emerald-100/50 shadow-sm hover:shadow-xl transition-all duration-300 group">
                        <div class="w-16 h-16 bg-brand-light rounded-2xl flex items-center justify-center text-brand-primary text-2xl font-black mb-6 group-hover:bg-brand-primary group-hover:text-white transition-all">
                            <i class="fa-solid fa-shield-halved"></i>
                        </div>
                        <h3 class="text-xl font-bold text-brand-dark mb-3">ضمان استبدال فوري</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            نضمن كافة بطارياتنا بضمان استبدال حقيقي ومباشر بدون انتظار أو تعقيدات في حال ظهور أي عيب مصنعي.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Testimonials Section -->
        <section id="testimonials" class="py-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-xl mx-auto mb-16">
                <span class="text-brand-accent font-bold text-sm tracking-wide">آراء وتجارب</span>
                <h2 class="text-3xl md:text-4xl font-black text-brand-dark mt-1">ماذا يقول عملاؤنا عن خدماتنا؟</h2>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Review 1 -->
                <div class="bg-slate-50 p-6 rounded-2xl border border-slate-200/60 relative">
                    <div class="flex items-center gap-1 text-brand-gold text-sm mb-4">
                        <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                    </div>
                    <p class="text-slate-700 text-sm leading-relaxed mb-6">
                        "تعطلت البطارية في المواقف بعد الدوام، اتصلت برقم الطوارئ ووصل الفني خلال 20 دقيقة بالضبط. ركب بطارية هانكوك وفحص الدينامو مجاناً. خدمة احترافية جداً."
                    </p>
                    <div class="flex items-center gap-3 pt-4 border-t border-slate-200">
                        <div class="w-10 h-10 bg-brand-dark text-white rounded-full flex items-center justify-center font-bold">م</div>
                        <div>
                            <h4 class="font-bold text-slate-800 text-sm">محمد العتيبي</h4>
                            <span class="text-xs text-slate-500">عميل في الرياض</span>
                        </div>
                    </div>
                </div>

                <!-- Review 2 -->
                <div class="bg-slate-50 p-6 rounded-2xl border border-slate-200/60 relative">
                    <div class="flex items-center gap-1 text-brand-gold text-sm mb-4">
                        <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                    </div>
                    <p class="text-slate-700 text-sm leading-relaxed mb-6">
                        "الموقع سهل جداً في اختيار البطارية المناسبة لسيارتي لاندكروزر. الأسعار ممتازة مقارنة بالسوق وتاريخ الإنتاج جديد جداً. شكراً لسرعة التجاوب."
                    </p>
                    <div class="flex items-center gap-3 pt-4 border-t border-slate-200">
                        <div class="w-10 h-10 bg-brand-primary text-white rounded-full flex items-center justify-center font-bold">خ</div>
                        <div>
                            <h4 class="font-bold text-slate-800 text-sm">خالد الشمري</h4>
                            <span class="text-xs text-slate-500">عميل في جدة</span>
                        </div>
                    </div>
                </div>

                <!-- Review 3 -->
                <div class="bg-slate-50 p-6 rounded-2xl border border-slate-200/60 relative">
                    <div class="flex items-center gap-1 text-brand-gold text-sm mb-4">
                        <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                    </div>
                    <p class="text-slate-700 text-sm leading-relaxed mb-6">
                        "ممتازين في التعامل وأهم شيء أن الفني احترافي ولم يمسح البرمجة الخاصة بالسيارة أثناء تغيير البطارية. ننصح بالتعامل معهم بشدة."
                    </p>
                    <div class="flex items-center gap-3 pt-4 border-t border-slate-200">
                        <div class="w-10 h-10 bg-brand-dark text-white rounded-full flex items-center justify-center font-bold">س</div>
                        <div>
                            <h4 class="font-bold text-slate-800 text-sm">سارة الغامدي</h4>
                            <span class="text-xs text-slate-500">عميلة في الدمام</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact & Emergency CTA Section -->
        <section id="contact" class="py-16 bg-brand-dark text-white relative">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid lg:grid-cols-2 gap-12 items-center">
                    <div>
                        <span class="text-brand-primary font-bold text-sm tracking-wide">تواصل معنا</span>
                        <h2 class="text-3xl md:text-4xl font-black mt-2 leading-tight">هل تحتاج مساعدة عاجلة أو استفسار؟</h2>
                        <p class="text-slate-300 mt-4 leading-relaxed">
                            فريق الدعم الفني متواجد على مدار 24 ساعة للإجابة على كافة تساؤلاتك ومساعدتك في اختيار البطارية الأنسب لسيارتك.
                        </p>

                        <div class="mt-8 space-y-4">
                            <div class="flex items-center gap-4">
                                <div class="w-12 h-12 bg-white/10 rounded-xl flex items-center justify-center text-brand-primary text-xl">
                                    <i class="fa-solid fa-phone"></i>
                                </div>
                                <div>
                                    <p class="text-xs text-slate-400">الهاتف المجاني والطوارئ</p>
                                    <p class="text-lg font-bold text-white">920000000</p>
                                </div>
                            </div>

                            <div class="flex items-center gap-4">
                                <div class="w-12 h-12 bg-white/10 rounded-xl flex items-center justify-center text-brand-primary text-xl">
                                    <i class="fa-solid fa-envelope"></i>
                                </div>
                                <div>
                                    <p class="text-xs text-slate-400">البريد الإلكتروني</p>
                                    <p class="text-lg font-bold text-white">support@ampere-batteries.com</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Quick Message Form -->
                    <div class="bg-white text-slate-800 p-8 rounded-3xl shadow-xl">
                        <h3 class="text-xl font-bold text-brand-dark mb-4">أرسل لنا رسالة سريعة</h3>
                        <form onsubmit="handleContactSubmit(event)" class="space-y-4">
                            <div>
                                <label class="block text-xs font-bold text-slate-700 mb-1">الاسم الكامل</label>
                                <input type="text" required placeholder="أدخل اسمك" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-4 py-3 text-sm focus:outline-none focus:border-brand-primary">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-slate-700 mb-1">رقم الجوال</label>
                                <input type="tel" required placeholder="05xxxxxxxx" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-4 py-3 text-sm focus:outline-none focus:border-brand-primary">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-slate-700 mb-1">الرسالة</label>
                                <textarea rows="3" required placeholder="كيف يمكننا مساعدتك؟" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-4 py-3 text-sm focus:outline-none focus:border-brand-primary"></textarea>
                            </div>
                            <button type="submit" class="w-full bg-brand-primary hover:bg-brand-accent text-white font-bold py-3.5 rounded-xl transition-all shadow-md">
                                إرسال الرسالة
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="bg-slate-900 text-slate-400 border-t border-slate-800 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
                <div>
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-10 h-10 bg-brand-primary rounded-xl flex items-center justify-center text-white font-black text-xl">
                            <i class="fa-solid fa-bolt"></i>
                        </div>
                        <span class="text-xl font-black text-white">أمبيـــر</span>
                    </div>
                    <p class="text-xs leading-relaxed">
                        وجهتك الأولى لشراء وتبديل بطاريات السيارات في المملكة. جودة عالية، سرعة إنجاز، وضمان معتمد.
                    </p>
                </div>

                <div>
                    <h4 class="text-white font-bold text-sm mb-4">روابط سريعة</h4>
                    <ul class="space-y-2 text-xs">
                        <li><a href="#hero" class="hover:text-brand-primary">الرئيسية</a></li>
                        <li><a href="#finder" class="hover:text-brand-primary">البحث عن بطارية</a></li>
                        <li><a href="#products" class="hover:text-brand-primary">كتالوج المنتجات</a></li>
                        <li><a href="#services" class="hover:text-brand-primary">خدماتنا</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-bold text-sm mb-4">أنواع البطاريات</h4>
                    <ul class="space-y-2 text-xs">
                        <li><a href="#" class="hover:text-brand-primary">بطاريات AGM للتوقف والبدء</a></li>
                        <li><a href="#" class="hover:text-brand-primary">بطاريات كورية جافة</a></li>
                        <li><a href="#" class="hover:text-brand-primary">بطاريات يابانية عالية التحمل</a></li>
                        <li><a href="#" class="hover:text-brand-primary">بطاريات الشاحنات والسيارات الكبيرة</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-bold text-sm mb-4">وسائل الدفع المقبولة</h4>
                    <div class="flex flex-wrap gap-2 text-2xl text-slate-300">
                        <i class="fa-brands fa-cc-visa"></i>
                        <i class="fa-brands fa-cc-mastercard"></i>
                        <i class="fa-brands fa-apple-pay"></i>
                        <i class="fa-solid fa-money-bill-wave"></i>
                    </div>
                    <p class="text-[11px] mt-4 text-slate-500">نوفر الدفع عند التركيب كاش أو مدى.</p>
                </div>
            </div>

            <div class="pt-8 border-t border-slate-800 text-center text-xs text-slate-500">
                <p>© 2026 متجر أمبير للبطاريات (Ampere Batteries). جميع الحقوق محفوظة.</p>
            </div>
        </div>
    </footer>

    <!-- Shopping Cart Drawer Side Panel -->
    <div id="cartDrawer" class="fixed inset-0 z-50 overflow-hidden hidden">
        <div class="absolute inset-0 bg-slate-900/60 backdrop-blur-sm transition-opacity" onclick="toggleCart()"></div>
        <div class="fixed inset-y-0 left-0 max-w-full flex">
            <div class="w-screen max-w-md bg-white shadow-2xl flex flex-col">
                <!-- Cart Header -->
                <div class="p-6 bg-brand-dark text-white flex items-center justify-between">
                    <div class="flex items-center gap-2">
                        <i class="fa-solid fa-cart-shopping text-brand-primary"></i>
                        <h3 class="font-bold text-lg">سلة المشتريات</h3>
                    </div>
                    <button onclick="toggleCart()" class="text-slate-400 hover:text-white"><i class="fa-solid fa-xmark text-xl"></i></button>
                </div>

                <!-- Cart Items List -->
                <div id="cartItemsContainer" class="flex-grow overflow-y-auto p-6 space-y-4">
                    <!-- Dynamic cart items will appear here -->
                </div>

                <!-- Cart Footer -->
                <div class="p-6 border-t border-slate-100 bg-slate-50 space-y-4">
                    <div class="flex justify-between items-center font-bold text-slate-800">
                        <span>الإجمالي المفترض:</span>
                        <span id="cartTotal" class="text-xl text-brand-dark">0 ر.س</span>
                    </div>
                    <p class="text-xs text-slate-500">* السعر شامل الضريبة، التوصيل والتركيب المجاني.</p>
                    <button onclick="checkout()" class="w-full bg-brand-primary hover:bg-brand-accent text-white font-bold py-3.5 rounded-xl shadow-md transition-all">
                        متابعة الطلب والتركيب
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- Notification Toast -->
    <div id="toast" class="fixed bottom-5 left-5 z-50 bg-brand-dark text-white px-6 py-3 rounded-xl shadow-2xl flex items-center gap-3 transform translate-y-20 opacity-0 transition-all duration-300 pointer-events-none">
        <i class="fa-solid fa-circle-check text-brand-primary text-xl"></i>
        <span id="toastMsg" class="text-sm font-semibold">تمت الإضافة بنجاح</span>
    </div>

    <!-- JavaScript Application Logic -->
    <script>
        // Database Mock Data
        const carData = {
            toyota: {
                name: "تويوتا",
                models: {
                    camry: { name: "كامري", years: ["2018-2024", "2012-2017", "2007-2011"] },
                    corolla: { name: "كورولا", years: ["2019-2024", "2014-2018"] },
                    landcruiser: { name: "لاندكروزر", years: ["2022-2024", "2008-2021"] }
                }
            },
            hyundai: {
                name: "هيونداي",
                models: {
                    sonata: { name: "سوناتا", years: ["2020-2024", "2015-2019"] },
                    elantra: { name: "إلنترا", years: ["2021-2024", "2016-2020"] },
                    tucson: { name: "توسان", years: ["2021-2024", "2016-2020"] }
                }
            },
            ford: {
                name: "فورد",
                models: {
                    f150: { name: "F-150", years: ["2018-2024"] },
                    explorer: { name: "إكسبلورر", years: ["2020-2024", "2011-2019"] }
                }
            }
        };

        const products = [
            {
                id: 1,
                name: "بطارية هانكوك (Hankook) 80 أمبير",
                brand: "هانكوك - كوري",
                type: "80ah",
                price: 340,
                oldPrice: 380,
                warranty: "12 شهر",
                badge: "الأكثر مبيعاً",
                icon: "fa-car-battery"
            },
            {
                id: 2,
                name: "بطارية إيه سي ديلكو (ACDelco) 60 أمبير",
                brand: "ACDelco - معتمد",
                type: "60ah",
                price: 260,
                oldPrice: 290,
                warranty: "12 شهر",
                badge: "اقتصادي",
                icon: "fa-battery-full"
            },
            {
                id: 3,
                name: "بطارية فوشي AGM للسيارات الحديثة 70AH",
                brand: "Varta AGM - ألماني",
                type: "agm",
                price: 680,
                oldPrice: 750,
                warranty: "24 شهر",
                badge: "تقنية AGM",
                icon: "fa-bolt-lightning"
            },
            {
                id: 4,
                name: "بطارية أمارون (Amaron) 55 أمبير",
                brand: "Amaron - هندي ياباني",
                type: "60ah",
                price: 290,
                oldPrice: 320,
                warranty: "18 شهر",
                badge: "عمر أطول",
                icon: "fa-car-battery"
            },
            {
                id: 5,
                name: "بطارية أوبتيكا AGM عالية التحمل 75AH",
                brand: "Optima - أمريكي",
                type: "agm",
                price: 850,
                oldPrice: 920,
                warranty: "24 شهر",
                badge: "للطرق الوعرة",
                icon: "fa-shield-halved"
            },
            {
                id: 6,
                name: "بطارية يواسا (Yuasa) 80 أمبير",
                brand: "Yuasa - ياباني",
                type: "80ah",
                price: 410,
                oldPrice: 450,
                warranty: "18 شهر",
                badge: "أداء عالي",
                icon: "fa-car-battery"
            }
        ];

        let cart = [];

        // App Initialization
        document.addEventListener('DOMContentLoaded', () => {
            renderProducts(products);
        });

        // Render Products
        function renderProducts(items) {
            const grid = document.getElementById('productsGrid');
            grid.innerHTML = items.map(p => `
                <div class="bg-white rounded-3xl border border-slate-100 shadow-sm hover:shadow-xl transition-all duration-300 p-6 flex flex-col justify-between group">
                    <div>
                        <div class="flex justify-between items-start mb-4">
                            <span class="bg-brand-light text-brand-dark text-xs font-bold px-3 py-1 rounded-full border border-emerald-200">${p.badge}</span>
                            <div class="text-left">
                                <span class="text-xl font-black text-brand-dark">${p.price} <span class="text-xs">ر.س</span></span>
                                ${p.oldPrice ? `<p class="text-xs text-slate-400 line-through">${p.oldPrice} ر.س</p>` : ''}
                            </div>
                        </div>

                        <div class="my-6 text-center py-6 bg-slate-50 rounded-2xl group-hover:bg-brand-light transition-colors">
                            <i class="fa-solid ${p.icon} text-6xl text-brand-primary"></i>
                        </div>

                        <span class="text-xs font-semibold text-slate-400">${p.brand}</span>
                        <h3 class="text-lg font-bold text-slate-800 mt-1 mb-3">${p.name}</h3>

                        <div class="space-y-1.5 text-xs text-slate-600 mb-6">
                            <div class="flex items-center gap-2">
                                <i class="fa-solid fa-shield text-brand-primary"></i>
                                <span>الضمان: <strong class="text-slate-800">${p.warranty}</strong></span>
                            </div>
                            <div class="flex items-center gap-2">
                                <i class="fa-solid fa-truck-fast text-brand-primary"></i>
                                <span>يشمل التوصيل والتركيب الميداني</span>
                            </div>
                        </div>
                    </div>

                    <button onclick="addToCart(${p.id})" class="w-full bg-slate-900 hover:bg-brand-primary text-white font-bold py-3 rounded-xl transition-all flex items-center justify-center gap-2 shadow-sm">
                        <i class="fa-solid fa-cart-plus"></i>
                        <span>إضافة للسلة والطلب</span>
                    </button>
                </div>
            `).join('');
        }

        // Filter Products
        function filterProducts(category) {
            // Update active button state
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.classList.remove('bg-brand-dark', 'text-white');
                btn.classList.add('bg-white', 'text-slate-600', 'border');
            });
            event.target.classList.add('bg-brand-dark', 'text-white');
            event.target.classList.remove('bg-white', 'text-slate-600');

            if (category === 'all') {
                renderProducts(products);
            } else {
                const filtered = products.filter(p => p.type === category);
                renderProducts(filtered);
            }
        }

        // Battery Finder Dropdown Dynamic Logic
        function updateModels() {
            const makeKey = document.getElementById('carMake').value;
            const modelSelect = document.getElementById('carModel');
            const yearSelect = document.getElementById('carYear');

            modelSelect.innerHTML = '<option value="">اختر الموديل...</option>';
            yearSelect.innerHTML = '<option value="">اختر السنة...</option>';
            yearSelect.disabled = true;

            if (makeKey && carData[makeKey]) {
                modelSelect.disabled = false;
                const models = carData[makeKey].models;
                for (let key in models) {
                    modelSelect.innerHTML += `<option value="${key}">${models[key].name}</option>`;
                }
            } else {
                modelSelect.disabled = true;
            }
        }

        document.getElementById('carModel').addEventListener('change', function() {
            const makeKey = document.getElementById('carMake').value;
            const modelKey = this.value;
            const yearSelect = document.getElementById('carYear');

            yearSelect.innerHTML = '<option value="">اختر السنة...</option>';

            if (makeKey && modelKey && carData[makeKey].models[modelKey]) {
                yearSelect.disabled = false;
                const years = carData[makeKey].models[modelKey].years;
                years.forEach(y => {
                    yearSelect.innerHTML += `<option value="${y}">${y}</option>`;
                });
            } else {
                yearSelect.disabled = true;
            }
        });

        function searchBatteries(e) {
            e.preventDefault();
            const make = document.getElementById('carMake').value;
            if(!make) {
                showToast("يرجى اختيار ماركة السيارة أولاً");
                return;
            }
            showToast("جاري تصفية البطاريات المتوافقة لسيارتك...");
            
            // Scroll smoothly to products
            document.getElementById('products').scrollIntoView({ behavior: 'smooth' });
        }

        // Shopping Cart Logic
        function addToCart(id) {
            const product = products.find(p => p.id === id);
            const existing = cart.find(item => item.id === id);

            if (existing) {
                existing.qty++;
            } else {
                cart.push({ ...product, qty: 1 });
            }

            updateCartUI();
            showToast(`تمت إضافة ${product.name} إلى السلة`);
        }

        function removeFromCart(id) {
            cart = cart.filter(item => item.id !== id);
            updateCartUI();
        }

        function updateCartUI() {
            // Count
            const totalCount = cart.reduce((acc, item) => acc + item.qty, 0);
            document.getElementById('cartCount').innerText = totalCount;

            // Total Price
            const totalPrice = cart.reduce((acc, item) => acc + (item.price * item.qty), 0);
            document.getElementById('cartTotal').innerText = `${totalPrice} ر.س`;

            // List Container
            const container = document.getElementById('cartItemsContainer');
            if (cart.length === 0) {
                container.innerHTML = `
                    <div class="text-center py-12 text-slate-400">
                        <i class="fa-solid fa-basket-shopping text-5xl mb-3"></i>
                        <p class="text-sm font-semibold">سلة المشتريات فارغة حالياً</p>
                    </div>
                `;
            } else {
                container.innerHTML = cart.map(item => `
                    <div class="flex items-center justify-between p-4 bg-slate-50 rounded-2xl border border-slate-200/60">
                        <div>
                            <h4 class="font-bold text-slate-800 text-sm">${item.name}</h4>
                            <p class="text-xs text-brand-accent font-semibold">${item.price} ر.س x ${item.qty}</p>
                        </div>
                        <button onclick="removeFromCart(${item.id})" class="text-red-500 hover:text-red-700 p-2">
                            <i class="fa-solid fa-trash-can"></i>
                        </button>
                    </div>
                `).join('');
            }
        }

        function toggleCart() {
            const drawer = document.getElementById('cartDrawer');
            drawer.classList.toggle('hidden');
        }

        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
        }

        function checkout() {
            if(cart.length === 0) {
                showToast("السلة فارغة! يرجى إضافة بطارية أولاً.");
                return;
            }
            alert("شكراً لطلبك! سيتم توجيهك فوراً للتواصل مع الفني لتحديد الموقع وتركيب البطارية.");
            cart = [];
            updateCartUI();
            toggleCart();
        }

        // Toast Notification Function
        function showToast(msg) {
            const toast = document.getElementById('toast');
            document.getElementById('toastMsg').innerText = msg;
            toast.classList.remove('translate-y-20', 'opacity-0');
            
            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 3000);
        }

        function handleContactSubmit(e) {
            e.preventDefault();
            showToast("تم إرسال طلبك بنجاح! سيتواصل معك الفني خلال دقائق.");
            e.target.reset();
        }
