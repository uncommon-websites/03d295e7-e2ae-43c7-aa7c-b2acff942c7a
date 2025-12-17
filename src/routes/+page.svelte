<script lang="ts">
    import AppButtons from "$lib/components/AppButtons.svelte";
    import PhoneMockup from "$lib/components/PhoneMockup.svelte";
</script>

<div class="w-full overflow-hidden">
    <!-- Header -->
    <header class="max-w-7xl mx-auto w-full py-6 px-6 flex items-center justify-between">
        <div class="flex items-center gap-2.5">
            <div class="w-7 h-7 text-primary-500">
                <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196ZM11.5077 14.7121L11.493 14.6986C11.9061 14.739 12.3232 14.6897 12.7143 14.5543C13.1053 14.4188 13.4605 14.2007 13.7542 13.9154C14.0477 13.6302 14.2726 13.285 14.4121 12.905C14.5518 12.525 14.6028 12.1196 14.5615 11.718L14.5762 11.7315C14.5351 11.2591 14.6007 10.7838 14.7681 10.3385C14.9356 9.89327 15.2011 9.48893 15.5459 9.15368C15.8908 8.8185 16.3068 8.56042 16.7648 8.39767C17.2228 8.23481 17.7118 8.17111 18.1978 8.21099L18.1832 8.19749C18.7645 8.25059 19.3485 8.12801 19.8556 7.84656C20.3627 7.56511 20.7681 7.13845 21.0165 6.62479C21.265 6.11114 21.3444 5.53548 21.2439 4.97634C21.1435 4.4172 20.868 3.9018 20.4551 3.50044C20.0422 3.09909 19.512 2.8313 18.9368 2.73364C18.3616 2.63596 17.7695 2.71315 17.241 2.95467C16.7126 3.19618 16.2737 3.59027 15.9842 4.08319C15.6946 4.57609 15.5685 5.14383 15.6232 5.70895L15.6093 5.6947C15.6504 6.16712 15.585 6.64259 15.4175 7.08788C15.2501 7.53318 14.9846 7.93758 14.6398 8.27287C14.2949 8.60805 13.8789 8.86612 13.4208 9.02888C12.9627 9.19163 12.4736 9.25523 11.9876 9.21526L12.0015 9.22951C11.5885 9.18908 11.1713 9.23836 10.7803 9.37381C10.3893 9.50919 10.034 9.72744 9.74039 10.0127C9.44674 10.2979 9.22199 10.6431 9.08234 11.0231C8.94276 11.4031 8.89176 11.8085 8.93304 12.2101L8.91915 12.1966C8.96005 12.6689 8.89439 13.1443 8.72688 13.5895C8.5593 14.0346 8.29389 14.4389 7.94908 14.7741C7.60425 15.1093 7.18835 15.3673 6.73039 15.5302C6.27242 15.693 5.78342 15.7569 5.29749 15.7171L5.31138 15.7306C4.73003 15.6775 4.14599 15.8001 3.63892 16.0815C3.13186 16.363 2.72644 16.7896 2.478 17.3033C2.22954 17.817 2.15013 18.3926 2.25061 18.9518C2.35109 19.5109 2.62657 20.0263 3.03945 20.4276C3.45234 20.829 3.98253 21.0968 4.55773 21.1944C5.13293 21.2921 5.72512 21.2149 6.25353 20.9734C6.78193 20.7319 7.22085 20.3379 7.51038 19.8449C7.79994 19.352 7.92601 18.7843 7.87139 18.2191L7.88605 18.2326C7.845 17.7602 7.91058 17.2849 8.07809 16.8396C8.24551 16.3944 8.511 15.99 8.85581 15.6548C9.20069 15.3196 9.61664 15.0615 10.0746 14.8988C10.5327 14.7359 11.0217 14.6722 11.5077 14.7121ZM17.1996 10.7633C16.9071 11.0493 16.6832 11.3944 16.5437 11.7741C16.4042 12.1538 16.3526 12.5587 16.3925 12.9601L16.3786 12.9466C16.4197 13.419 16.3541 13.8944 16.1866 14.3396C16.0191 14.7849 15.7537 15.1892 15.4089 15.5244C15.064 15.8596 14.648 16.1177 14.19 16.2804C13.732 16.4433 13.2429 16.507 12.757 16.4671L12.7708 16.4806C12.1896 16.4281 11.6057 16.551 11.0989 16.8328C10.5921 17.1145 10.1871 17.5414 9.93902 18.0551C9.69097 18.5689 9.61188 19.1444 9.71265 19.7035C9.81349 20.2625 10.0892 20.7777 10.5022 21.1788C10.9152 21.5799 11.4454 21.8474 12.0205 21.9448C12.5957 22.0423 13.1877 21.9649 13.716 21.7234C14.2443 21.4817 14.683 21.0877 14.9724 20.5947C15.2618 20.1018 15.3878 19.5342 15.3332 18.9692L15.3478 18.9827C15.3068 18.5103 15.3723 18.0349 15.5398 17.5896C15.7073 17.1444 15.9728 16.7401 16.3176 16.4048C16.6625 16.0696 17.0784 15.8115 17.5364 15.6488C17.9945 15.486 18.4835 15.4222 18.9695 15.4621L18.9548 15.4486C19.4296 15.4901 19.9076 15.4144 20.3444 15.2286C20.7811 15.0427 21.1625 14.7527 21.4533 14.3854C21.744 14.0181 21.9347 13.5854 22.0075 13.1274C22.0805 12.6694 22.0332 12.2009 21.8703 11.7653C21.7073 11.3298 21.4339 10.9413 21.0754 10.6358C20.7168 10.3303 20.2848 10.1178 19.8192 10.0179C19.3536 9.91795 18.8697 9.93385 18.4121 10.0641C17.9546 10.1945 17.5383 10.4349 17.2019 10.7633H17.1996Z"
                        fill="currentColor"
                    />
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
                Turn <span class="italic">chaotic</span><br/>
                schedules into<br/>
                <span class="text-primary-500">intentional</span><br/>
                progress.
            </h2>
            <p class="text-gray-500 max-w-xl leading-[1.7] text-lg">
                Actimate combines AI-powered calendar integration with proactive accountability coaching to help you achieve your goals—even with ADHD or a packed schedule.
            </p>
            <div>
                <AppButtons />
            </div>
        </div>
        
        <div class="relative flex justify-center lg:justify-end items-center py-8">
            <!-- Single Phone -->
            <div class="phone-frame">
                <div class="phone-screen">
                    <!-- Status Bar with Dynamic Island space -->
                    <div class="h-10"></div>

                    <!-- Content -->
                    <div class="px-4 pt-1">
                        <!-- Header -->
                        <div class="text-center mb-4">
                            <h3 class="text-base font-semibold text-gray-900">Today</h3>
                            <p class="text-[10px] text-gray-400 mt-0.5">Thursday, October 9</p>
                        </div>

                        <!-- View Tabs -->
                        <div class="flex justify-center gap-5 mb-4">
                            <span class="text-[10px] text-primary-500 font-medium pb-1 border-b border-primary-500">Day</span>
                            <span class="text-[10px] text-gray-400">Week</span>
                            <span class="text-[10px] text-gray-400">Month</span>
                        </div>

                        <!-- AI Coach Card -->
                        <div class="flex items-center gap-2.5 bg-gradient-to-r from-primary-50 to-orange-50 rounded-xl p-3 mb-4">
                            <div class="w-7 h-7 bg-primary-500 rounded-lg flex items-center justify-center flex-shrink-0">
                                <svg class="w-3.5 h-3.5 text-white" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                            </div>
                            <div>
                                <span class="text-xs font-medium text-gray-900">Plan your day with Pia</span>
                                <p class="text-[9px] text-gray-500">Your AI accountability coach</p>
                            </div>
                        </div>

                        <!-- Tasks Section -->
                        <div class="mb-4">
                            <div class="flex items-center justify-between mb-2">
                                <span class="text-xs font-semibold text-gray-900">Tasks</span>
                                <span class="text-[10px] text-gray-400">2 remaining</span>
                            </div>
                            <div class="space-y-2">
                                <div class="flex items-center gap-2.5 p-2.5 bg-white rounded-xl border border-gray-100">
                                    <div class="w-4 h-4 rounded border-2 border-primary-500 flex-shrink-0"></div>
                                    <span class="text-xs text-gray-800">Write product roadmap</span>
                                </div>
                                <div class="flex items-center gap-2.5 p-2.5 bg-white rounded-xl border border-gray-100">
                                    <div class="w-4 h-4 rounded border-2 border-gray-300 flex-shrink-0"></div>
                                    <span class="text-xs text-gray-800">Review team proposals</span>
                                </div>
                            </div>
                        </div>

                        <!-- Scheduled -->
                        <div>
                            <span class="text-xs font-semibold text-gray-900 block mb-2">Scheduled</span>
                            <div class="flex items-center gap-2.5 p-2.5 bg-white rounded-xl border border-gray-100">
                                <div class="w-4 h-4 rounded border-2 border-gray-300 flex-shrink-0"></div>
                                <div class="flex-1">
                                    <span class="text-xs text-gray-800">Workout</span>
                                    <span class="text-[10px] text-primary-500 ml-1.5">2:00 PM</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- FAB -->
                    <div class="absolute bottom-20 right-4">
                        <div class="w-10 h-10 bg-primary-500 rounded-xl flex items-center justify-center shadow-lg shadow-primary-500/25">
                            <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M12 5v14m-7-7h14"/></svg>
                        </div>
                    </div>

                    <!-- Bottom Nav -->
                    <div class="absolute bottom-0 left-0 right-0 flex justify-around items-center py-3 px-4 bg-white/95 backdrop-blur-sm border-t border-gray-100">
                        <div class="flex flex-col items-center gap-0.5">
                            <svg class="w-5 h-5 text-primary-500" fill="currentColor" viewBox="0 0 24 24"><rect x="3" y="4" width="18" height="18" rx="2"/></svg>
                            <span class="text-[8px] text-primary-500 font-medium">Timeline</span>
                        </div>
                        <div class="flex flex-col items-center gap-0.5">
                            <svg class="w-5 h-5 text-gray-400" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24"><path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
                            <span class="text-[8px] text-gray-400">Habits</span>
                        </div>
                        <div class="flex flex-col items-center gap-0.5">
                            <svg class="w-5 h-5 text-gray-400" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24"><path d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"/></svg>
                            <span class="text-[8px] text-gray-400">Goals</span>
                        </div>
                        <div class="flex flex-col items-center gap-0.5">
                            <svg class="w-5 h-5 text-gray-400" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24"><path d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"/></svg>
                            <span class="text-[8px] text-gray-400">AI</span>
                        </div>
                    </div>

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
                    <!-- Visual: Pia Avatar with Chat Bubbles -->
                    <div class="relative flex justify-center items-center min-h-[400px] order-2 lg:order-1">
                        <div class="relative">
                            <!-- Central avatar -->
                            <div class="w-36 h-36 rounded-full bg-gradient-to-br from-primary-400 to-primary-600 flex items-center justify-center shadow-lg">
                                <svg class="w-16 h-16 text-white" viewBox="0 0 24 24" fill="currentColor">
                                    <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                                </svg>
                            </div>

                            <!-- Chat bubbles -->
                            <div class="absolute -top-6 -right-24 bg-white/10 rounded-2xl rounded-br-sm px-4 py-3 text-sm text-white/90 border border-white/5">
                                How's the workout going?
                            </div>
                            <div class="absolute top-1/2 -translate-y-1/2 -right-32 bg-white/5 rounded-2xl px-3 py-2 text-xs text-white/60 border border-white/5">
                                9:00 AM check-in
                            </div>
                            <div class="absolute -bottom-4 -left-20 bg-primary-500/20 rounded-2xl rounded-bl-sm px-4 py-3 text-sm text-white/90 border border-primary-500/10">
                                You've got this!
                            </div>
                            <div class="absolute top-4 -left-16 bg-white/5 rounded-2xl px-3 py-2 text-xs text-white/60 border border-white/5">
                                Following up...
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
</style>

