<script lang="ts">
    import AppButtons from "$lib/components/AppButtons.svelte";
    import PhoneMockup from "$lib/components/PhoneMockup.svelte";
</script>

<div class="w-full overflow-hidden">
    <!-- Header -->
    <header class="w-full py-8 flex flex-col items-center justify-center text-center">
        <h1 class="text-4xl font-serif font-medium tracking-tight">Atoms.</h1>
        <p class="text-xs uppercase tracking-widest text-gray-500 mt-2 font-sans">The official Atomic Habits app</p>
    </header>

    <!-- Hero Section -->
    <section class="max-w-7xl mx-auto px-6 pt-12 pb-24 grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <div class="flex flex-col items-start space-y-8">
            <h2 class="text-6xl md:text-7xl font-serif leading-[1.1]">
                Tiny changes,<br/>
                remarkable results.
            </h2>
            <p class="text-gray-600 max-w-md leading-relaxed">
                Based on the easy and proven habit change method from the NYT best-seller, Atom's helps you build good habits and break bad ones.
            </p>
            <div class="pt-2">
                <AppButtons />
            </div>
        </div>
        
        <div class="relative flex justify-center items-center">
            <!-- Abstract Background Shapes -->
            <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[500px] h-[500px] opacity-50 pointer-events-none">
                 <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-full fill-[#F2EBE0]">
                    <path d="M44.7,-76.4C58.9,-69.2,71.8,-59.1,81.6,-46.6C91.4,-34.1,98.2,-19.2,95.8,-5.2C93.4,8.8,81.8,21.9,71.2,33.7C60.6,45.4,51,55.8,39.9,64.4C28.8,73,16.2,79.8,2.6,75.3C-11,70.8,-25.6,55,-38.7,42.5C-51.8,30,-63.4,20.8,-69.3,8.7C-75.2,-3.4,-75.4,-18.4,-68.8,-31.6C-62.2,-44.8,-48.8,-56.2,-35.4,-63.8C-22,-71.4,-8.6,-75.2,5.2,-84.2C19,-93.2,30.5,-107.4,44.7,-76.4Z" transform="translate(100 100)" />
                  </svg>
            </div>
            
            <PhoneMockup>
                <!-- Mockup Content -->
                <div class="flex flex-col h-full p-6 items-center pt-16">
                    <h3 class="text-3xl font-serif text-center mb-2">Create your<br>first habit</h3>
                    <div class="w-16 h-16 bg-orange-100 rounded-full flex items-center justify-center mb-6 mt-4">
                        <span class="text-2xl">☀️</span>
                    </div>
                    <button class="bg-black text-white px-8 py-3 rounded-full w-full font-medium mt-auto mb-12">
                        Create Habit ->
                    </button>
                </div>
            </PhoneMockup>
        </div>
    </section>

    <!-- Dark Section (Laws) -->
    <section class="bg-[#1C1C1C] text-white py-24 overflow-hidden relative">
        <div class="max-w-7xl mx-auto px-6 mb-16">
            <p class="text-xl md:text-2xl font-serif max-w-lg leading-relaxed text-gray-300">
                Atoms is the only app built on scientifically-backed laws of habit change.
            </p>
        </div>

        <div class="relative w-full overflow-x-hidden">
            <div class="flex whitespace-nowrap px-6 gap-4 md:gap-12 items-center">
                 <!-- Item 1 -->
                 <div class="inline-flex items-baseline">
                    <span class="text-[120px] md:text-[180px] font-serif font-light text-transparent stroke-text opacity-50" style="-webkit-text-stroke: 1px rgba(255,255,255,0.5);">1.</span>
                    <div class="flex flex-col ml-4">
                        <span class="text-5xl md:text-7xl font-serif">Make it</span>
                        <span class="text-5xl md:text-7xl font-serif font-bold">obvious.</span>
                    </div>
                 </div>
                 
                 <!-- Item 2 -->
                 <div class="inline-flex items-baseline ml-12 md:ml-24">
                    <span class="text-[120px] md:text-[180px] font-serif font-light text-[#E6D8C0]">2.</span>
                    <div class="flex flex-col ml-4">
                        <span class="text-5xl md:text-7xl font-serif">Make it</span>
                        <span class="text-5xl md:text-7xl font-serif font-bold">attractive.</span>
                    </div>
                 </div>

                 <!-- Hint of Item 3 -->
                   <div class="inline-flex items-baseline ml-12 md:ml-24 opacity-20">
                    <span class="text-[120px] md:text-[180px] font-serif font-light">3.</span>
                 </div>
            </div>
        </div>

        <div class="max-w-7xl mx-auto px-6 mt-12 flex justify-end">
            <div class="flex gap-2">
                <div class="w-3 h-3 rounded-full bg-white"></div>
                <div class="w-3 h-3 rounded-full bg-gray-600"></div>
            </div>
        </div>
    </section>

    <!-- Why we're different -->
    <section class="py-32 max-w-5xl mx-auto px-6">
        <div class="text-center mb-24">
            <p class="text-sm uppercase tracking-widest text-gray-500">Why we're different</p>
        </div>

        <div class="space-y-32">
            <!-- Feature 1 -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center group">
                <div>
                    <h3 class="text-5xl md:text-6xl font-serif mb-6 group-hover:italic transition-all duration-300">We know<br>what really<br>works</h3>
                    <p class="text-gray-600 max-w-xs text-sm leading-relaxed">
                        We don't rely on guesswork. Our principles of habit change make it obvious, attractive, easy, and satisfying.
                    </p>
                    <div class="mt-4 text-xs text-gray-400">→</div>
                </div>
                <div class="flex justify-center">
                    <!-- Illustration Placeholder: Stacked Rocks -->
                    <div class="w-64 h-64 relative">
                        <svg viewBox="0 0 200 200" class="w-full h-full stroke-black fill-none stroke-[1.5]">
                            <path d="M60,140 Q50,120 70,110 Q90,100 110,110 Q130,120 120,140 Q110,160 90,160 Q70,160 60,140 Z" />
                            <path d="M75,105 Q65,85 85,75 Q105,65 125,75 Q145,85 135,105 Q125,125 105,125 Q85,125 75,105 Z" />
                            <path d="M90,70 Q80,50 100,40 Q120,30 140,40 Q160,50 150,70 Q140,90 120,90 Q100,90 90,70 Z" />
                        </svg>
                        <div class="absolute -z-10 top-10 right-10 w-40 h-40 bg-[#F2EBE0] rounded-full opacity-50 blur-xl"></div>
                    </div>
                </div>
            </div>

            <!-- Feature 2 -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center group">
                <div>
                    <h3 class="text-5xl md:text-6xl font-serif mb-6 group-hover:italic transition-all duration-300">We meet<br>you where<br>you are</h3>
                    <p class="text-gray-600 max-w-xs text-sm leading-relaxed">
                        Whether you're just starting or already on a roll, we have the right tools to help you find your balance.
                    </p>
                    <div class="mt-4 text-xs text-gray-400">→</div>
                </div>
                <div class="flex justify-center">
                    <!-- Illustration Placeholder: Handshake -->
                    <div class="w-64 h-64 relative">
                        <svg viewBox="0 0 200 200" class="w-full h-full stroke-black fill-none stroke-[1.5]">
                            <path d="M40,100 L80,100 L100,80 L120,100 L160,100" />
                            <path d="M40,120 L80,120 L100,140 L120,120 L160,120" />
                             <!-- Simplified abstract representation -->
                             <circle cx="100" cy="110" r="40" class="stroke-black" />
                        </svg>
                         <div class="absolute -z-10 top-10 right-10 w-40 h-40 bg-[#F2EBE0] rounded-full opacity-50 blur-xl"></div>
                    </div>
                </div>
            </div>

            <!-- Feature 3 -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center group">
                <div>
                    <h3 class="text-5xl md:text-6xl font-serif mb-6 group-hover:italic transition-all duration-300">We evolve<br>as you<br>evolve</h3>
                    <p class="text-gray-600 max-w-xs text-sm leading-relaxed">
                        Building tiny habits leads to remarkable results. We scale up just like you do, one step at a time.
                    </p>
                    <div class="mt-4 text-xs text-gray-400">→</div>
                </div>
                <div class="flex justify-center">
                    <!-- Illustration Placeholder: Tools -->
                    <div class="w-64 h-64 relative">
                        <svg viewBox="0 0 200 200" class="w-full h-full stroke-black fill-none stroke-[1.5]">
                            <path d="M50,150 L150,50" />
                            <circle cx="150" cy="50" r="10" />
                            <rect x="40" y="140" width="20" height="20" transform="rotate(45 50 150)" />
                        </svg>
                         <div class="absolute -z-10 top-10 right-10 w-40 h-40 bg-[#F2EBE0] rounded-full opacity-50 blur-xl"></div>
                    </div>
                </div>
            </div>
            
             <!-- Feature 4 -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center group">
                <div>
                    <h3 class="text-5xl md:text-6xl font-serif mb-6 group-hover:italic transition-all duration-300">We're in it<br>for the<br>long-haul</h3>
                    <p class="text-gray-600 max-w-xs text-sm leading-relaxed">
                        We support you in creating habits that last, focusing on consistency over intensity.
                    </p>
                    <div class="mt-4 text-xs text-gray-400">→</div>
                </div>
                <div class="flex justify-center">
                    <!-- Illustration Placeholder: Clock -->
                    <div class="w-64 h-64 relative">
                         <svg viewBox="0 0 200 200" class="w-full h-full stroke-black fill-none stroke-[1.5]">
                            <circle cx="100" cy="100" r="50" />
                            <path d="M100,100 L100,70" />
                            <path d="M100,100 L120,110" />
                            <path d="M90,40 L110,40" />
                        </svg>
                         <div class="absolute -z-10 top-10 right-10 w-40 h-40 bg-[#F2EBE0] rounded-full opacity-50 blur-xl"></div>
                    </div>
                </div>
            </div>

             <!-- Feature 5 -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center group">
                <div>
                    <h3 class="text-5xl md:text-6xl font-serif mb-6 group-hover:italic transition-all duration-300">We know<br>what it<br>takes to<br>show up</h3>
                    <p class="text-gray-600 max-w-xs text-sm leading-relaxed">
                        We understand the ups and downs. We help you get back on track without shame or guilt.
                    </p>
                    <div class="mt-4 text-xs text-gray-400">→</div>
                </div>
                <div class="flex justify-center">
                    <!-- Illustration Placeholder: Heart -->
                    <div class="w-64 h-64 relative">
                         <svg viewBox="0 0 200 200" class="w-full h-full stroke-black fill-none stroke-[1.5]">
                            <path d="M100,160 C100,160 40,100 40,60 C40,30 70,30 100,60 C130,30 160,30 160,60 C160,100 100,160 100,160 Z" />
                        </svg>
                         <div class="absolute -z-10 top-10 right-10 w-40 h-40 bg-[#F2EBE0] rounded-full opacity-50 blur-xl"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Mid CTA -->
    <section class="py-24 bg-[#FCFAF7] border-y border-gray-100">
        <div class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
            <div>
                <p class="text-2xl md:text-3xl font-serif leading-relaxed mb-8">
                    Build good habits, break bad ones, and make better decisions in just five good minutes a day. Get started today and cast a vote for future you.
                </p>
                <AppButtons />
            </div>
            <div class="flex justify-center">
                <!-- Jar Illustration -->
                 <div class="w-64 h-64 relative">
                     <svg viewBox="0 0 200 200" class="w-full h-full stroke-black fill-none stroke-[1.5]">
                        <path d="M60,60 L140,60 L140,160 Q140,180 120,180 L80,180 Q60,180 60,160 Z" />
                        <path d="M55,60 L145,60 L145,40 L55,40 Z" />
                        <path d="M70,100 L130,100" />
                        <path d="M70,140 L130,140" />
                    </svg>
                    <div class="absolute -z-10 bottom-0 left-10 w-40 h-20 bg-[#E6D8C0] rounded-full opacity-50 blur-xl"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Dark Cards Section -->
    <section class="py-24">
        <div class="max-w-4xl mx-auto px-6 mb-16">
            <h2 class="text-4xl font-serif">Atoms is designed to help you<br>take action.</h2>
            <p class="text-gray-500 mt-4 max-w-md">
                Our core features are designed to help you build power habits, track progress, and make lasting change.
            </p>
        </div>

        <div class="max-w-6xl mx-auto px-6 space-y-8">
            <!-- Card 1 -->
            <div class="bg-[#1C1C1C] rounded-[2rem] p-12 md:p-20 text-white relative overflow-hidden flex flex-col md:flex-row items-center gap-12">
                <div class="relative z-10 w-full md:w-1/2 flex justify-center">
                     <PhoneMockup>
                         <div class="p-6 flex flex-col h-full bg-white text-black">
                             <div class="text-xs text-gray-500 uppercase tracking-widest mb-4">Identity</div>
                             <h4 class="text-xl font-serif">I am a reader</h4>
                             <div class="mt-4 space-y-2">
                                 <div class="p-3 bg-gray-50 rounded-lg flex items-center gap-3">
                                     <div class="w-4 h-4 rounded-full border border-gray-300"></div>
                                     <span class="text-sm">Read 10 pages</span>
                                 </div>
                             </div>
                         </div>
                     </PhoneMockup>
                </div>
                <div class="w-full md:w-1/2 relative z-10">
                    <p class="text-xs uppercase tracking-widest text-gray-400 mb-2">Not just habits</p>
                    <h3 class="text-4xl md:text-5xl font-serif mb-6">Identity-based<br>habits</h3>
                    <p class="text-gray-400 leading-relaxed">
                        Most apps focus on outcome-based habits. We help you focus on identity-based habits. It's not about what you want to achieve. It's about who you wish to become.
                    </p>
                </div>
                <!-- Abstract BG -->
                <div class="absolute left-0 bottom-0 w-1/2 h-full bg-white opacity-5 rounded-full blur-3xl translate-y-1/2 -translate-x-1/4"></div>
            </div>

             <!-- Card 2 -->
            <div class="bg-[#1C1C1C] rounded-[2rem] p-12 md:p-20 text-white relative overflow-hidden flex flex-col md:flex-row-reverse items-center gap-12">
                <div class="relative z-10 w-full md:w-1/2 flex justify-center">
                     <PhoneMockup>
                         <div class="p-6 flex flex-col h-full bg-white text-black items-center justify-center">
                             <div class="w-20 h-20 rounded-full bg-orange-100 flex items-center justify-center mb-4">
                                 <span class="text-2xl">🏆</span>
                             </div>
                             <h4 class="text-xl font-serif text-center">Habit Master</h4>
                             <p class="text-sm text-gray-500 text-center mt-2">100 Days Streak</p>
                         </div>
                     </PhoneMockup>
                </div>
                <div class="w-full md:w-1/2 relative z-10">
                    <p class="text-xs uppercase tracking-widest text-gray-400 mb-2">Supportive environment</p>
                    <h3 class="text-4xl md:text-5xl font-serif mb-6">A journey with<br>support</h3>
                    <p class="text-gray-400 leading-relaxed">
                        Atoms connects you with people on the same journey. Share progress, celebrate wins, and find accountability partners.
                    </p>
                </div>
            </div>

             <!-- Card 3 -->
            <div class="bg-[#1C1C1C] rounded-[2rem] p-12 md:p-20 text-white relative overflow-hidden flex flex-col md:flex-row items-center gap-12">
                <div class="relative z-10 w-full md:w-1/2 flex justify-center">
                     <PhoneMockup>
                         <div class="p-6 flex flex-col h-full bg-white text-black">
                             <div class="bg-black text-white p-4 rounded-xl mb-4">
                                 <p class="text-sm font-medium">Time to read!</p>
                                 <p class="text-xs text-gray-400 mt-1">It's 8:00 PM. Grab your book.</p>
                             </div>
                         </div>
                     </PhoneMockup>
                </div>
                <div class="w-full md:w-1/2 relative z-10">
                    <p class="text-xs uppercase tracking-widest text-gray-400 mb-2">Habit reminders</p>
                    <h3 class="text-4xl md:text-5xl font-serif mb-6">Everyone<br>needs a nudge</h3>
                    <p class="text-gray-400 leading-relaxed">
                        Set up reminders that work for you. Never miss a habit again with our flexible notification system.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Daily Lessons -->
    <section class="py-24 bg-[#FCFAF7]">
        <div class="max-w-7xl mx-auto px-6">
            <h2 class="text-3xl font-serif mb-12">Daily Lessons</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Lesson 1 -->
                <div class="bg-white p-8 rounded-xl aspect-[4/5] flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-8 h-8 bg-gray-100 rounded-full flex items-center justify-center text-xs">01</div>
                    <h3 class="text-2xl font-serif">Make Your Habits Fun</h3>
                    <div class="text-xs text-gray-400 uppercase tracking-widest">Read Lesson -></div>
                </div>
                 <!-- Lesson 2 -->
                <div class="bg-white p-8 rounded-xl aspect-[4/5] flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-8 h-8 bg-gray-100 rounded-full flex items-center justify-center text-xs">02</div>
                    <h3 class="text-2xl font-serif">Aim to Be Great in 10 Years</h3>
                    <div class="text-xs text-gray-400 uppercase tracking-widest">Read Lesson -></div>
                </div>
                 <!-- Lesson 3 -->
                <div class="bg-white p-8 rounded-xl aspect-[4/5] flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-8 h-8 bg-gray-100 rounded-full flex items-center justify-center text-xs">03</div>
                    <h3 class="text-2xl font-serif">Start Small</h3>
                    <div class="text-xs text-gray-400 uppercase tracking-widest">Read Lesson -></div>
                </div>
                 <!-- Lesson 4 -->
                <div class="bg-white p-8 rounded-xl aspect-[4/5] flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-8 h-8 bg-gray-100 rounded-full flex items-center justify-center text-xs">04</div>
                    <h3 class="text-2xl font-serif">Everything is Imperfect</h3>
                    <div class="text-xs text-gray-400 uppercase tracking-widest">Read Lesson -></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Book Section -->
    <section class="py-32 max-w-5xl mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
            <div>
                <p class="text-2xl font-serif leading-relaxed mb-8">
                    Get started today with the app based on the NYT best-seller that has already helped over 20 million people.
                </p>
                <AppButtons />
            </div>
            <div class="flex justify-center relative">
                <!-- Book Cover Placeholder -->
                <div class="w-64 aspect-[2/3] bg-[#EAE4D3] shadow-2xl relative flex flex-col items-center justify-center text-center p-6 border-l-4 border-gray-200">
                    <p class="text-xs uppercase tracking-widest text-gray-500 mb-4">New York Times Bestseller</p>
                    <h3 class="text-3xl font-serif font-bold text-gray-800 mb-1">Atomic<br>Habits</h3>
                    <p class="text-sm text-gray-600 mt-4">Tiny Changes,<br>Remarkable Results</p>
                    <div class="mt-auto pt-8 text-sm font-bold text-gray-800">James Clear</div>
                    
                    <!-- Decorative dots -->
                    <div class="absolute top-4 right-4 w-2 h-2 bg-orange-400 rounded-full"></div>
                </div>
                 <div class="absolute -z-10 top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-80 h-80 bg-[#F2EBE0] rounded-full opacity-50 blur-2xl"></div>
            </div>
        </div>
    </section>

    <!-- Testimonial -->
    <section class="bg-[#1C1C1C] text-white py-32">
        <div class="max-w-7xl mx-auto px-6 grid grid-cols-1 lg:grid-cols-2 gap-16">
            <div>
                <h2 class="text-2xl font-serif mb-12">See what people are saying about Atoms</h2>
                <h3 class="text-5xl md:text-7xl font-serif leading-tight">Love the<br>flexibility.</h3>
            </div>
            <div class="flex flex-col justify-end">
                <p class="text-gray-400 text-lg leading-relaxed mb-8">
                    "The personalized focus of the habit you create make it unique and non-standardized. Minimalistic but inviting style UI. I never feel overwhelmed, making it a normal, human experience. Love the measurement/assessment and introspection. This program is encouraging but unobtrusive. Great job!"
                </p>
                <div>
                    <p class="font-bold">User from USA</p>
                    <p class="text-sm text-gray-500">App Store Review</p>
                </div>
                <div class="mt-12 flex justify-end">
                    <button class="text-white hover:opacity-70 transition-opacity">
                        <svg width="48" height="24" viewBox="0 0 50 24" fill="none" stroke="currentColor" stroke-width="2">
                            <path d="M0 12H48M48 12L38 2M48 12L38 22" />
                        </svg>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Share Section -->
    <section class="py-32 bg-[#FCFAF7] relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
            <div class="relative z-10">
                <p class="text-3xl font-serif leading-relaxed mb-8 max-w-md">
                    Share Atoms with a friend and support each other in making tiny changes for remarkable results.
                </p>
                <AppButtons />
            </div>
            <div class="flex justify-center relative z-10">
                 <PhoneMockup>
                     <div class="flex items-center justify-center h-full bg-white">
                         <h1 class="text-4xl font-serif">Atoms.</h1>
                     </div>
                 </PhoneMockup>
            </div>
        </div>
        <!-- Divider Line -->
        <div class="absolute top-1/2 left-0 w-full h-px bg-gray-200 -z-0"></div>
    </section>

    <!-- Footer -->
    <footer class="pt-24 pb-12 px-6">
        <div class="max-w-7xl mx-auto flex flex-col items-center text-center">
            <div class="mb-16">
                <!-- Big Logo -->
                 <div class="relative inline-block">
                    <span class="text-[120px] md:text-[180px] font-serif leading-none">Atoms</span>
                    <span class="text-[120px] md:text-[180px] font-serif leading-none text-red-600">.</span>
                    <!-- Apple Illustration overlay on the 'o' if possible, or just use text for now as requested 1:1 but simplified -->
                    <!-- The screenshot shows an apple replacing the 'o' or near it. Let's try to make the 'o' an apple -->
                     <div class="absolute top-[45%] left-[68%] -translate-x-1/2 -translate-y-1/2 w-[90px] h-[100px] md:w-[130px] md:h-[140px]">
                         <!-- Apple SVG -->
                         <svg viewBox="0 0 100 120" class="w-full h-full fill-[#E84E36]">
                             <path d="M50,30 C30,30 10,40 10,70 C10,100 30,115 50,115 C70,115 90,100 90,70 C90,40 70,30 50,30 Z" />
                             <path d="M50,30 C50,30 55,10 45,5" stroke="#3E2723" stroke-width="3" fill="none"/>
                         </svg>
                     </div>
                 </div>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-4 gap-8 mb-16 text-sm text-gray-600">
                <div class="flex flex-col gap-3 text-left md:text-center">
                    <span class="font-bold text-gray-900 uppercase tracking-widest text-xs mb-2">Introduction</span>
                    <a href="#">Method</a>
                    <a href="#">Story</a>
                </div>
                <div class="flex flex-col gap-3 text-left md:text-center">
                    <span class="font-bold text-gray-900 uppercase tracking-widest text-xs mb-2">Coaching</span>
                    <a href="#">1-on-1 Coaching</a>
                    <a href="#">FAQ</a>
                </div>
                 <div class="flex flex-col gap-3 text-left md:text-center">
                    <span class="font-bold text-gray-900 uppercase tracking-widest text-xs mb-2">Company</span>
                    <a href="#">Newsletter</a>
                    <a href="#">Contact</a>
                </div>
                 <div class="flex flex-col gap-3 text-left md:text-center">
                    <span class="font-bold text-gray-900 uppercase tracking-widest text-xs mb-2">Legal</span>
                    <a href="#">Terms</a>
                    <a href="#">Privacy</a>
                </div>
            </div>

            <div class="flex flex-col md:flex-row items-center justify-between w-full border-t border-gray-200 pt-12 gap-8">
                <div class="text-xs text-gray-400">
                    © 2024 Atoms Inc.
                </div>
                <div class="flex gap-6">
                    <!-- Social Icons -->
                    <a href="#" class="w-5 h-5 bg-gray-300 rounded-full"></a>
                    <a href="#" class="w-5 h-5 bg-gray-300 rounded-full"></a>
                    <a href="#" class="w-5 h-5 bg-gray-300 rounded-full"></a>
                </div>
                <div>
                     <AppButtons />
                </div>
            </div>
        </div>
    </footer>
</div>

<style>
    /* Custom stroke text utility */
    .stroke-text {
        -webkit-text-stroke: 1px rgba(255, 255, 255, 0.5);
        color: transparent;
    }
</style>

