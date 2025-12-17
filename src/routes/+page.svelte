<script lang="ts">
    import AppButtons from "$lib/components/AppButtons.svelte";
    import PhoneMockup from "$lib/components/PhoneMockup.svelte";
</script>

<div class="w-full overflow-hidden">
    <!-- Header -->
    <header class="max-w-7xl mx-auto w-full py-6 px-6 flex items-center justify-between">
        <div class="flex items-center gap-2.5">
            <div class="w-7 h-7 text-primary-500">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 102 101" fill="none" class="w-full h-full">
                    <circle cx="50.1521" cy="12" r="12" fill="currentColor"/>
                    <circle cx="77.5405" cy="77.5356" r="4.35749" transform="rotate(135 77.5405 77.5356)" fill="currentColor"/>
                    <circle cx="50.1521" cy="89" r="12" fill="currentColor"/>
                    <ellipse cx="89.1521" cy="50" rx="12" ry="12" transform="rotate(90 89.1521 50)" fill="currentColor"/>
                    <ellipse cx="11.6521" cy="50" rx="12" ry="11.5" transform="rotate(90 11.6521 50)" fill="currentColor"/>
                    <circle cx="23.0268" cy="23.022" r="4.35749" transform="rotate(135 23.0268 23.022)" fill="currentColor"/>
                    <circle cx="4.35749" cy="4.35749" r="4.35749" transform="matrix(0.707107 0.707107 0.707107 -0.707107 16.8643 77.5356)" fill="currentColor"/>
                    <circle cx="4.35749" cy="4.35749" r="4.35749" transform="matrix(0.707107 0.707107 0.707107 -0.707107 71.3782 23.022)" fill="currentColor"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M71.4038 10.0694C73.0426 10.9302 73.6734 12.9567 72.8126 14.5956L69.5393 20.8272C68.6785 22.4661 66.6521 23.0969 65.0132 22.236C63.3743 21.3752 62.7436 19.3488 63.6044 17.7099L66.8776 11.4782C67.7384 9.83932 69.7649 9.20858 71.4038 10.0694Z" fill="currentColor"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M35.5541 78.3214C37.193 79.1822 37.8238 81.2086 36.9629 82.8475L33.6897 89.0792C32.8289 90.7181 30.8025 91.3488 29.1636 90.488C27.5247 89.6272 26.894 87.6007 27.7548 85.9619L31.028 79.7302C31.8888 78.0913 33.9153 77.4605 35.5541 78.3214Z" fill="currentColor"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M29.1641 10.0694C27.5252 10.9302 26.8945 12.9567 27.7553 14.5956L31.0285 20.8272C31.8894 22.4661 33.9158 23.0969 35.5547 22.236C37.1936 21.3752 37.8243 19.3488 36.9635 17.7099L33.6903 11.4782C32.8294 9.83932 30.803 9.20858 29.1641 10.0694Z" fill="currentColor"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M65.0128 78.3214C63.3739 79.1822 62.7431 81.2086 63.604 82.8475L66.8772 89.0792C67.738 90.7181 69.7644 91.3488 71.4033 90.488C73.0422 89.6272 73.6729 87.6007 72.8121 85.9619L69.5389 79.7302C68.6781 78.0913 66.6516 77.4605 65.0128 78.3214Z" fill="currentColor"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M22.1371 35.7495C21.288 37.3945 19.2661 38.0397 17.6211 37.1905L11.3662 33.9618C9.72125 33.1127 9.07608 31.0908 9.92521 29.4458C10.7743 27.8009 12.7962 27.1557 14.4412 28.0048L20.6961 31.2335C22.341 32.0826 22.9862 34.1045 22.1371 35.7495Z" fill="currentColor"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M90.3414 28.8728C89.4689 27.2401 87.438 26.6238 85.8053 27.4963L79.5971 30.8139C77.9644 31.6863 77.3481 33.7172 78.2206 35.3499C79.0931 36.9826 81.1239 37.5989 82.7567 36.7264L88.9649 33.4089C90.5976 32.5364 91.2139 30.5055 90.3414 28.8728Z" fill="currentColor"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M22.1371 64.8079C21.288 63.1629 19.2661 62.5177 17.6211 63.3668L11.3662 66.5956C9.72125 67.4447 9.07608 69.4666 9.92521 71.1115C10.7743 72.7565 12.7962 73.4017 14.4412 72.5526L20.6961 69.3239C22.341 68.4747 22.9862 66.4529 22.1371 64.8079Z" fill="currentColor"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M90.3414 71.6848C89.4689 73.3175 87.438 73.9338 85.8053 73.0613L79.5971 69.7438C77.9644 68.8713 77.3481 66.8404 78.2206 65.2077C79.0931 63.575 81.1239 62.9587 82.7567 63.8312L88.9649 67.1487C90.5976 68.0212 91.2139 70.0521 90.3414 71.6848Z" fill="currentColor"/>
                </svg>
            </div>
            <span class="text-xl font-serif font-medium tracking-tight">Actimate</span>
        </div>
        <p class="text-[10px] uppercase tracking-[0.2em] text-gray-400 font-medium hidden sm:block">AI-Powered Productivity</p>
    </header>

    <!-- Hero Section -->
    <section class="max-w-7xl mx-auto px-6 pt-16 md:pt-24 pb-24 grid grid-cols-1 lg:grid-cols-[1.1fr_0.9fr] gap-12 lg:gap-8 items-center">
        <div class="flex flex-col items-start space-y-10">
            <h2 class="text-5xl sm:text-6xl md:text-[4.5rem] lg:text-[5rem] font-serif leading-[1.08] tracking-[-0.02em]">
                The <span class="italic">ADHD</span> planner<br/>
                that actually<br/>
                <span class="text-primary-500">keeps you</span><br/>
                on track.
            </h2>
            <p class="text-gray-500 max-w-xl leading-[1.7] text-lg">
                Actimate combines your goals, habits, tasks, and calendar into one system, with an AI accountability partner that checks in on you, so you finally follow through.
            </p>
            <div>
                <AppButtons />
            </div>
        </div>
        
        <div class="relative flex justify-center lg:justify-end items-center py-8">
            <!-- Single Phone -->
            <div class="phone-frame">
                <div class="phone-screen">
                    <!-- App Screenshot -->
                    <img 
                        src="/uploaded/1765982071029-8ze6vh5.png" 
                        alt="Actimate app timeline view showing daily tasks and schedule"
                        class="w-full h-full object-cover"
                    />
                </div>
            </div>
        </div>
    </section>

    <!-- Dark Section (Principles) -->
    <section class="bg-[#1C1C1C] text-white py-24 md:py-32 overflow-hidden relative">
        <!-- Subtle grain texture overlay -->
        <div class="absolute inset-0 opacity-[0.03] pointer-events-none" style="background-image: url('data:image/svg+xml,%3Csvg viewBox=%220 0 256 256%22 xmlns=%22http://www.w3.org/2000/svg%22%3E%3Cfilter id=%22noise%22%3E%3CfeTurbulence type=%22fractalNoise%22 baseFrequency=%220.9%22 numOctaves=%224%22 stitchTiles=%22stitch%22/%3E%3C/filter%3E%3Crect width=%22100%25%22 height=%22100%25%22 filter=%22url(%23noise)%22/%3E%3C/svg%3E');"></div>

        <div class="max-w-7xl mx-auto px-6 relative">
            <!-- Header -->
            <div class="mb-20 md:mb-28">
                <p class="text-sm uppercase tracking-[0.2em] text-gray-500 mb-4">Our Philosophy</p>
                <p class="text-xl md:text-2xl font-serif max-w-xl leading-relaxed text-gray-300">
                    Actimate is built on three core principles that turn scattered focus into consistent achievement.
                </p>
            </div>

            <!-- Principles Grid -->
            <div class="space-y-16 md:space-y-0 md:flex md:justify-between md:items-start">
                <!-- Principle 1 -->
                <div class="principle-card group cursor-pointer max-w-xs">
                    <div class="mb-6 md:mb-8">
                        <span class="principle-number text-[100px] md:text-[120px] lg:text-[140px] font-serif font-light leading-none text-gray-600 group-hover:text-primary-500 transition-all duration-300">1</span>
                    </div>
                    <div class="space-y-1">
                        <h3 class="text-3xl md:text-4xl font-serif leading-[1.1] tracking-[-0.01em]">Proactive</h3>
                        <h3 class="text-3xl md:text-4xl font-serif font-bold leading-[1.1] tracking-[-0.01em]">accountability.</h3>
                    </div>
                    <p class="mt-6 text-gray-500 leading-relaxed text-sm">
                        Don't wait for motivation. Pia checks in on you, follows up when you go quiet, and keeps you moving forward.
                    </p>
                </div>

                <!-- Principle 2 -->
                <div class="principle-card group cursor-pointer max-w-xs">
                    <div class="mb-6 md:mb-8">
                        <span class="principle-number text-[100px] md:text-[120px] lg:text-[140px] font-serif font-light leading-none text-gray-600 group-hover:text-primary-500 transition-all duration-300">2</span>
                    </div>
                    <div class="space-y-1">
                        <h3 class="text-3xl md:text-4xl font-serif leading-[1.1] tracking-[-0.01em]">Identity-based</h3>
                        <h3 class="text-3xl md:text-4xl font-serif font-bold leading-[1.1] tracking-[-0.01em]">goals.</h3>
                    </div>
                    <p class="mt-6 text-gray-500 leading-relaxed text-sm">
                        Link habits to who you want to become. Every action is a vote for your future self.
                    </p>
                </div>

                <!-- Principle 3 -->
                <div class="principle-card group cursor-pointer max-w-xs">
                    <div class="mb-6 md:mb-8">
                        <span class="principle-number text-[100px] md:text-[120px] lg:text-[140px] font-serif font-light leading-none text-gray-600 group-hover:text-primary-500 transition-all duration-300">3</span>
                    </div>
                    <div class="space-y-1">
                        <h3 class="text-3xl md:text-4xl font-serif leading-[1.1] tracking-[-0.01em]">Progress over</h3>
                        <h3 class="text-3xl md:text-4xl font-serif font-bold leading-[1.1] tracking-[-0.01em]">perfection.</h3>
                    </div>
                    <p class="mt-6 text-gray-500 leading-relaxed text-sm">
                        Small wins compound. Focus on showing up consistently, not being perfect every time.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- The Struggle Section -->
    <section class="py-24 md:py-32 max-w-7xl mx-auto px-6">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 lg:gap-24 items-start">
            <!-- Left: Large typography -->
            <div class="lg:sticky lg:top-24">
                <p class="text-sm uppercase tracking-[0.2em] text-primary-500 font-medium mb-6">Sound familiar?</p>
                <h2 class="text-5xl md:text-6xl lg:text-7xl font-serif leading-[1.05] tracking-[-0.02em]">
                    The gap between<br/>
                    <span class="italic text-gray-400">what you plan</span><br/>
                    and what you do.
                </h2>
            </div>

            <!-- Right: Pain points as a list -->
            <div class="space-y-12 lg:pt-8">
                <div class="group cursor-pointer">
                    <div class="flex items-start gap-6">
                        <span class="text-5xl font-serif text-gray-200 leading-none group-hover:text-primary-500 transition-colors">1</span>
                        <p class="text-xl text-gray-600 leading-relaxed pt-2">
                            Every Monday feels like a fresh start. By Wednesday, the system falls apart.
                        </p>
                    </div>
                </div>
                <div class="group cursor-pointer">
                    <div class="flex items-start gap-6">
                        <span class="text-5xl font-serif text-gray-200 leading-none group-hover:text-primary-500 transition-colors">2</span>
                        <p class="text-xl text-gray-600 leading-relaxed pt-2">
                            You meant to take a quick break. Now it's 4pm and you've done nothing.
                        </p>
                    </div>
                </div>
                <div class="group cursor-pointer">
                    <div class="flex items-start gap-6">
                        <span class="text-5xl font-serif text-gray-200 leading-none group-hover:text-primary-500 transition-colors">3</span>
                        <p class="text-xl text-gray-600 leading-relaxed pt-2">
                            The task list is right there. But your brain won't cooperate.
                        </p>
                    </div>
                </div>
                <div class="group cursor-pointer">
                    <div class="flex items-start gap-6">
                        <span class="text-5xl font-serif text-gray-200 leading-none group-hover:text-primary-500 transition-colors">4</span>
                        <p class="text-xl text-gray-600 leading-relaxed pt-2">
                            You've tried every app. Nothing sticks because nothing holds you accountable.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Solution CTA Section -->
    <section class="py-24 md:py-32 max-w-7xl mx-auto px-6">
        <div class="border border-gray-200 rounded-3xl p-10 md:p-16 lg:p-20 relative overflow-hidden">
            <!-- Subtle gradient background -->
            <div class="absolute inset-0 bg-gradient-to-br from-primary-50/50 via-transparent to-orange-50/30 pointer-events-none"></div>

            <div class="relative max-w-3xl">
                <p class="text-sm uppercase tracking-[0.2em] text-primary-500 font-medium mb-6">The solution</p>

                <h2 class="text-3xl md:text-4xl lg:text-5xl font-serif leading-[1.12] tracking-[-0.02em] mb-8">
                    You don't need another to-do app. You need a system that works <span class="italic">with</span> your brain—and someone in your corner.
                </h2>

                <p class="text-gray-500 text-lg mb-10 max-w-xl">Start showing up for yourself today.</p>

                <AppButtons />
            </div>

            <!-- Decorative element -->
            <div class="hidden lg:block absolute -right-20 -bottom-20 w-80 h-80 rounded-full border border-gray-100"></div>
            <div class="hidden lg:block absolute -right-10 -bottom-10 w-60 h-60 rounded-full border border-primary-100"></div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="py-24">
        <div class="max-w-4xl mx-auto px-6 mb-16">
            <h2 class="text-4xl md:text-5xl font-serif leading-[1.1] tracking-[-0.02em]">Actimate is designed to help you<br><span class="text-primary-500">make progress</span> on what matters.</h2>
            <p class="text-gray-500 mt-6 max-w-lg text-lg">
                Our core features combine AI-powered scheduling with proactive accountability to keep you on track.
            </p>
        </div>

        <div class="max-w-6xl mx-auto px-6 space-y-8">
            <!-- Card 1: AI Accountability Partner - Pia -->
            <div class="bg-[#1C1C1C] rounded-[2rem] p-12 md:p-24 text-white relative overflow-hidden">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <!-- Visual: Pia Chat Interface -->
                    <div class="relative flex justify-center items-center min-h-[400px] order-2 lg:order-1">
                        <div class="relative w-full max-w-[340px]">
                            <!-- Phone mockup with screenshot -->
                            <div class="phone-frame-feature">
                                <div class="phone-screen-feature">
                                    <img 
                                        src="/uploaded/1765983102802-mimj8rk.png" 
                                        alt="Pia AI chat interface showing personalized coaching and accountability features"
                                        class="w-full h-full object-cover"
                                    />
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Content -->
                    <div class="order-1 lg:order-2">
                        <p class="text-xs uppercase tracking-widest text-gray-400 mb-3">Your AI Accountability Partner</p>
                        <h3 class="text-4xl md:text-5xl font-serif mb-6 leading-[1.1] tracking-[-0.02em]">Meet Pia—<br>the partner who<br>never forgets</h3>
                        <p class="text-gray-400 leading-relaxed text-lg">
                            Pia isn't a chatbot that waits for you to ask. She checks in at the times you set, asks about your progress, and follows up on the goals you've been avoiding. It's like having a supportive friend who actually remembers.
                        </p>
                    </div>
                </div>
            </div>

            <!-- Card 2: Smart Scheduling -->
            <div class="bg-[#1C1C1C] rounded-[2rem] p-12 md:p-24 text-white relative overflow-hidden">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <!-- Content -->
                    <div>
                        <p class="text-xs uppercase tracking-widest text-gray-400 mb-3">Smart Scheduling</p>
                        <h3 class="text-4xl md:text-5xl font-serif mb-6 leading-[1.1] tracking-[-0.02em]">AI finds time<br>for your goals</h3>
                        <p class="text-gray-400 leading-relaxed text-lg">
                            Our AI analyzes your calendar and automatically schedules time for your most important goals. No more hoping you'll find time—Actimate makes it happen.
                        </p>
                    </div>

                    <!-- Visual: Calendar blocks -->
                    <div class="flex justify-center items-center min-h-[400px]">
                        <div class="w-full max-w-[300px]">
                            <div class="bg-white/5 rounded-2xl p-5 border border-white/10">
                                <div class="flex items-center justify-between mb-4">
                                    <span class="text-sm font-medium text-white/80">This Week</span>
                                    <span class="text-xs text-white/40">Auto-scheduled</span>
                                </div>

                                <div class="space-y-2.5">
                                    <div class="flex gap-3">
                                        <span class="text-xs text-white/30 w-12 pt-1">9 AM</span>
                                        <div class="flex-1 bg-primary-500/30 rounded-xl p-3 border border-primary-500/30">
                                            <span class="text-sm text-white">Deep Work: Project X</span>
                                        </div>
                                    </div>
                                    <div class="flex gap-3">
                                        <span class="text-xs text-white/30 w-12 pt-1">11 AM</span>
                                        <div class="flex-1 bg-white/10 rounded-xl p-3 border border-white/10">
                                            <span class="text-sm text-white/60">Team standup</span>
                                        </div>
                                    </div>
                                    <div class="flex gap-3">
                                        <span class="text-xs text-white/30 w-12 pt-1">2 PM</span>
                                        <div class="flex-1 bg-primary-500/20 rounded-xl p-3 border border-primary-500/20">
                                            <span class="text-sm text-white">Workout</span>
                                        </div>
                                    </div>
                                    <div class="flex gap-3">
                                        <span class="text-xs text-white/30 w-12 pt-1">4 PM</span>
                                        <div class="flex-1 bg-primary-500/20 rounded-xl p-3 border border-primary-500/20">
                                            <span class="text-sm text-white/90">Reading: ML Papers</span>
                                        </div>
                                    </div>
                                </div>

                                <div class="mt-4 pt-4 border-t border-white/10 flex items-center gap-2">
                                    <div class="w-2 h-2 bg-green-400 rounded-full"></div>
                                    <span class="text-xs text-white/50">3 goals auto-scheduled</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Card 3: Proactive Coaching -->
            <div class="bg-[#1C1C1C] rounded-[2rem] p-12 md:p-24 text-white relative overflow-hidden">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <!-- Visual: Coaching messages -->
                    <div class="flex justify-center items-center min-h-[400px] order-2 lg:order-1">
                        <div class="space-y-4 w-full max-w-[320px]">
                            <div class="bg-white/5 rounded-2xl p-4 border border-white/10">
                                <div class="flex items-start gap-3">
                                    <div class="w-9 h-9 rounded-full bg-primary-500 flex items-center justify-center flex-shrink-0">
                                        <svg class="w-4 h-4 text-white" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                                    </div>
                                    <div>
                                        <p class="text-xs text-white/40 mb-1">8:00 AM</p>
                                        <p class="text-sm text-white/90">Good morning! You have 2 goals scheduled today. Ready to start?</p>
                                    </div>
                                </div>
                            </div>

                            <div class="bg-white/5 rounded-2xl p-4 border border-white/10 ml-8">
                                <div class="flex items-start gap-3">
                                    <div class="w-9 h-9 rounded-full bg-primary-500 flex items-center justify-center flex-shrink-0">
                                        <svg class="w-4 h-4 text-white" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                                    </div>
                                    <div>
                                        <p class="text-xs text-white/40 mb-1">2:15 PM</p>
                                        <p class="text-sm text-white/90">Great job finishing your deep work session!</p>
                                    </div>
                                </div>
                            </div>

                            <div class="bg-white/5 rounded-2xl p-4 border border-white/10">
                                <div class="flex items-start gap-3">
                                    <div class="w-9 h-9 rounded-full bg-primary-500 flex items-center justify-center flex-shrink-0">
                                        <svg class="w-4 h-4 text-white" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                                    </div>
                                    <div>
                                        <p class="text-xs text-white/40 mb-1">6:00 PM</p>
                                        <p class="text-sm text-white/90">Still time for that evening run. Want me to remind you in 30 min?</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Content -->
                    <div class="order-1 lg:order-2">
                        <p class="text-xs uppercase tracking-widest text-gray-400 mb-3">Proactive Coaching</p>
                        <h3 class="text-4xl md:text-5xl font-serif mb-6 leading-[1.1] tracking-[-0.02em]">Your AI coach<br>checks in daily</h3>
                        <p class="text-gray-400 leading-relaxed text-lg">
                            Get personalized nudges and motivation when you need it most. Pia learns your patterns and knows exactly when to step in with encouragement or a gentle reminder.
                        </p>
                    </div>
                </div>
            </div>

            <!-- Card 4: Identity-Based Habits -->
            <div class="bg-[#1C1C1C] rounded-[2rem] p-12 md:p-24 text-white relative overflow-hidden">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <!-- Content -->
                    <div>
                        <p class="text-xs uppercase tracking-widest text-gray-400 mb-3">Identity-Based Habits</p>
                        <h3 class="text-4xl md:text-5xl font-serif mb-6 leading-[1.1] tracking-[-0.02em]">Build streaks.<br>Don't break the chain.</h3>
                        <p class="text-gray-400 leading-relaxed text-lg">
                            Connect your habits to the identity you want to build. Track your progress, celebrate wins, and get back on track quickly if you miss a day. Become the person who shows up, consistently.
                        </p>
                    </div>

                    <!-- Visual: Streak visualization -->
                    <div class="flex justify-center items-center min-h-[400px]">
                        <div class="w-full max-w-[320px]">
                            <div class="bg-white/5 rounded-2xl p-5 border border-white/10">
                                <div class="flex items-center gap-3 mb-5">
                                    <div class="w-12 h-12 rounded-xl bg-primary-500 flex items-center justify-center">
                                        <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M13 10V3L4 14h7v7l9-11h-7z"/></svg>
                                    </div>
                                    <div>
                                        <p class="text-base font-medium text-white">Daily Exercise</p>
                                        <p class="text-sm text-primary-400">"I am someone who moves every day"</p>
                                    </div>
                                </div>

                                <!-- Streak calendar -->
                                <div class="grid grid-cols-7 gap-1.5 mb-5">
                                    {#each Array(28) as _, i}
                                        <div class="aspect-square rounded-md {i < 21 ? 'bg-primary-500' : i < 24 ? 'bg-primary-500/40' : 'bg-white/10'}"></div>
                                    {/each}
                                </div>

                                <div class="flex items-center justify-between pt-4 border-t border-white/10">
                                    <div class="flex items-center gap-2">
                                        <span class="text-2xl font-serif text-primary-400">21</span>
                                        <span class="text-sm text-white/50">day streak</span>
                                    </div>
                                    <span class="text-sm text-white/40">Personal best!</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Card 5: GTD - Next Actions -->
            <div class="bg-[#1C1C1C] rounded-[2rem] p-12 md:p-24 text-white relative overflow-hidden">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <!-- Visual: Focused task view -->
                    <div class="flex justify-center items-center min-h-[400px] order-2 lg:order-1">
                        <div class="w-full max-w-[320px]">
                            <!-- Background tasks (faded) -->
                            <div class="space-y-2 opacity-30 mb-4">
                                <div class="bg-white/10 rounded-xl p-3 border border-white/5">
                                    <span class="text-sm text-white/50">Review quarterly report</span>
                                </div>
                                <div class="bg-white/10 rounded-xl p-3 border border-white/5">
                                    <span class="text-sm text-white/50">Call with Sarah</span>
                                </div>
                            </div>

                            <!-- Focused task -->
                            <div class="bg-white/10 rounded-2xl p-6 border border-white/20">
                                <p class="text-xs uppercase tracking-widest text-white/40 mb-4">Next Action</p>
                                <div class="flex items-start gap-4">
                                    <div class="w-6 h-6 rounded-lg border-2 border-primary-400 flex-shrink-0 mt-0.5"></div>
                                    <div>
                                        <p class="text-lg font-medium text-white mb-3">Write plan for A2A & MCP implementation</p>
                                        <div class="flex items-center gap-3 text-sm text-white/40">
                                            <span>~45 min</span>
                                            <span class="px-2 py-1 bg-primary-500/20 rounded-lg text-primary-400">Work</span>
                                        </div>
                                    </div>
                                </div>

                                <div class="mt-5 pt-4 border-t border-white/10 flex items-center justify-between">
                                    <span class="text-sm text-white/50">1 of 4 tasks today</span>
                                    <div class="flex gap-1.5">
                                        <div class="w-2 h-2 rounded-full bg-primary-500"></div>
                                        <div class="w-2 h-2 rounded-full bg-white/20"></div>
                                        <div class="w-2 h-2 rounded-full bg-white/20"></div>
                                        <div class="w-2 h-2 rounded-full bg-white/20"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Content -->
                    <div class="order-1 lg:order-2">
                        <p class="text-xs uppercase tracking-widest text-gray-400 mb-3">Built on Getting Things Done</p>
                        <h3 class="text-4xl md:text-5xl font-serif mb-6 leading-[1.1] tracking-[-0.02em]">Stop staring at<br>endless lists</h3>
                        <p class="text-gray-400 leading-relaxed text-lg">
                            Actimate uses the proven GTD methodology to show you only what matters right now. The 'Next Actions' view displays one task at a time, helping you focus and avoid overwhelm.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Founder Section -->
    <section class="py-24 md:py-32 bg-[#FCFAF7]">
        <div class="max-w-4xl mx-auto px-6 text-center">
            <p class="text-sm uppercase tracking-[0.2em] text-primary-500 font-medium mb-6">Built by someone who gets it</p>
            <h2 class="text-4xl md:text-5xl lg:text-6xl font-serif leading-[1.1] tracking-[-0.02em] mb-8">
                From personal struggle<br/>to powerful solution.
            </h2>
            <p class="text-gray-600 leading-relaxed text-lg max-w-2xl mx-auto mb-10">
                Actimate was created by Kevin Jordan, who built it to solve his own challenges with ADHD while juggling ambitious goals, building companies, and raising a young family. If you've ever felt overwhelmed by your schedule, Actimate was built for you.
            </p>
            <div class="flex justify-center">
                <AppButtons />
            </div>
        </div>
    </section>

    <!-- Testimonial -->
    <section class="py-24 md:py-32 max-w-7xl mx-auto px-6">
        <div class="mb-12">
            <p class="text-sm uppercase tracking-[0.2em] text-primary-500 font-medium">What early users say</p>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-16">
            <!-- Large quote -->
            <div class="lg:col-span-7">
                <blockquote class="text-3xl md:text-4xl lg:text-5xl font-serif leading-[1.15] tracking-[-0.02em]">
                    "Actimate is different—it doesn't just remind me to do things, it actually helps me <span class="italic text-gray-400">make time</span> for them."
                </blockquote>
            </div>

            <!-- Attribution -->
            <div class="lg:col-span-5 flex flex-col justify-end">
                <p class="text-gray-500 leading-relaxed mb-8">
                    As someone with ADHD, I've tried every productivity app out there. The AI coaching feels like having a supportive accountability partner who understands my brain.
                </p>
                <div class="flex items-center gap-4">
                    <div class="w-12 h-12 rounded-full bg-gray-100 flex items-center justify-center text-gray-400 font-serif text-lg">S</div>
                    <div>
                        <p class="font-medium">Sarah M.</p>
                        <p class="text-sm text-gray-400">Product Manager, Early Access User</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section class="py-24 md:py-32 bg-[#1C1C1C] text-white">
        <div class="max-w-7xl mx-auto px-6 text-center">
            <h2 class="text-4xl md:text-5xl lg:text-6xl font-serif leading-[1.1] tracking-[-0.02em] mb-6">
                Ready to make<br/><span class="italic text-primary-500">real progress</span>?
            </h2>
            <p class="text-gray-400 text-lg mb-10 max-w-lg mx-auto">
                Turn your chaotic schedule into intentional progress. Download Actimate today.
            </p>
            <div class="flex justify-center">
                <AppButtons />
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="pt-24 pb-12 px-6">
        <div class="max-w-7xl mx-auto flex flex-col items-center text-center">
            <div class="mb-16">
                <!-- Big Logo -->
                 <div class="relative inline-block">
                    <span class="text-[120px] md:text-[180px] font-serif leading-none">Actimate</span>
                    <span class="text-[120px] md:text-[180px] font-serif leading-none text-primary-500">.</span>
                 </div>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-4 gap-8 mb-16 text-sm text-gray-600">
                <div class="flex flex-col gap-3 text-left md:text-center">
                    <span class="font-bold text-gray-900 uppercase tracking-widest text-xs mb-2">Product</span>
                    <a href="#">Features</a>
                    <a href="#">How It Works</a>
                    <a href="#">Pricing</a>
                </div>
                <div class="flex flex-col gap-3 text-left md:text-center">
                    <span class="font-bold text-gray-900 uppercase tracking-widest text-xs mb-2">Resources</span>
                    <a href="#">Blog</a>
                    <a href="#">ADHD Guide</a>
                    <a href="#">FAQ</a>
                </div>
                 <div class="flex flex-col gap-3 text-left md:text-center">
                    <span class="font-bold text-gray-900 uppercase tracking-widest text-xs mb-2">Company</span>
                    <a href="#">About</a>
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
                    2025 ActimateAI LLC
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
    /* Principle card subtle padding */
    .principle-card {
        padding-bottom: 2rem;
    }

    /* Phone Frame Styles */
    .phone-frame {
        position: relative;
        width: 340px;
        height: 700px;
        border-radius: 52px;
        padding: 10px;
        background: #1a1a1a;
        box-shadow: 0 8px 40px -8px rgba(0, 0, 0, 0.15);
    }

    /* Dynamic Island */
    .phone-frame::before {
        content: '';
        position: absolute;
        top: 16px;
        left: 50%;
        transform: translateX(-50%);
        width: 100px;
        height: 32px;
        background: #000;
        border-radius: 18px;
        z-index: 50;
    }

    .phone-screen {
        width: 100%;
        height: 100%;
        background: #FAFAFA;
        border-radius: 44px;
        overflow: hidden;
        position: relative;
    }

    /* Phone positioning for different screen sizes */
    @media (max-width: 1023px) {
        .phone-frame {
            width: 100%;
            height: auto;
            aspect-ratio: 340 / 700;
            border-radius: 46px;
            padding: 9px;
        }

        .phone-screen {
            border-radius: 38px;
        }

        .phone-frame::before {
            width: 25%;
            max-width: 100px;
            height: 28px;
            top: 14px;
        }
    }

    /* Phone Frame for Features Section */
    .phone-frame-feature {
        position: relative;
        width: 100%;
        max-width: 340px;
        aspect-ratio: 340 / 700;
        border-radius: 52px;
        padding: 10px;
        background: #2a2a2a;
        box-shadow: 0 8px 40px -8px rgba(0, 0, 0, 0.3);
        margin: 0 auto;
    }

    /* Dynamic Island for feature phone */
    .phone-frame-feature::before {
        content: '';
        position: absolute;
        top: 16px;
        left: 50%;
        transform: translateX(-50%);
        width: 100px;
        height: 32px;
        background: #000;
        border-radius: 18px;
        z-index: 50;
    }

    .phone-screen-feature {
        width: 100%;
        height: 100%;
        background: #FAFAFA;
        border-radius: 44px;
        overflow: hidden;
        position: relative;
    }

    @media (max-width: 1023px) {
        .phone-frame-feature {
            border-radius: 46px;
            padding: 9px;
        }

        .phone-screen-feature {
            border-radius: 38px;
        }

        .phone-frame-feature::before {
            width: 25%;
            max-width: 100px;
            height: 28px;
            top: 14px;
        }
    }
</style>

