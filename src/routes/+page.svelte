<script lang="ts">
    import AppButtons from "$lib/components/AppButtons.svelte";
    import PhoneMockup from "$lib/components/PhoneMockup.svelte";
    import { onMount } from 'svelte';

    // Carousel state
    let currentSlide = $state(0);
    let autoplayInterval: ReturnType<typeof setInterval> | null = null;

    // Principle items
    const principles = [
        {
            number: "1.",
            title1: "Proactive",
            title2: "accountability.",
            numberStyle: "-webkit-text-stroke: 1px rgba(255,255,255,0.5); color: transparent;"
        },
        {
            number: "2.",
            title1: "Identity-based",
            title2: "goals.",
            numberStyle: "color: #FF6D22;"
        },
        {
            number: "3.",
            title1: "Progress over",
            title2: "perfection.",
            numberStyle: "color: #FFFFFF;"
        }
    ];

    // Navigation functions
    function goToSlide(index: number) {
        currentSlide = index;
        resetAutoplay();
    }

    function nextSlide() {
        currentSlide = (currentSlide + 1) % principles.length;
        resetAutoplay();
    }

    function prevSlide() {
        currentSlide = (currentSlide - 1 + principles.length) % principles.length;
        resetAutoplay();
    }

    function resetAutoplay() {
        if (autoplayInterval) {
            clearInterval(autoplayInterval);
        }
        startAutoplay();
    }

    function startAutoplay() {
        autoplayInterval = setInterval(() => {
            currentSlide = (currentSlide + 1) % principles.length;
        }, 5000);
    }

    onMount(() => {
        startAutoplay();
        return () => {
            if (autoplayInterval) {
                clearInterval(autoplayInterval);
            }
        };
    });
</script>

<div class="w-full overflow-hidden">
    <!-- Header -->
    <header class="w-full py-8 flex flex-col items-center justify-center text-center">
        <div class="flex items-center gap-3">
            <div class="w-8 h-8 text-primary-500">
                <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196ZM11.5077 14.7121L11.493 14.6986C11.9061 14.739 12.3232 14.6897 12.7143 14.5543C13.1053 14.4188 13.4605 14.2007 13.7542 13.9154C14.0477 13.6302 14.2726 13.285 14.4121 12.905C14.5518 12.525 14.6028 12.1196 14.5615 11.718L14.5762 11.7315C14.5351 11.2591 14.6007 10.7838 14.7681 10.3385C14.9356 9.89327 15.2011 9.48893 15.5459 9.15368C15.8908 8.8185 16.3068 8.56042 16.7648 8.39767C17.2228 8.23481 17.7118 8.17111 18.1978 8.21099L18.1832 8.19749C18.7645 8.25059 19.3485 8.12801 19.8556 7.84656C20.3627 7.56511 20.7681 7.13845 21.0165 6.62479C21.265 6.11114 21.3444 5.53548 21.2439 4.97634C21.1435 4.4172 20.868 3.9018 20.4551 3.50044C20.0422 3.09909 19.512 2.8313 18.9368 2.73364C18.3616 2.63596 17.7695 2.71315 17.241 2.95467C16.7126 3.19618 16.2737 3.59027 15.9842 4.08319C15.6946 4.57609 15.5685 5.14383 15.6232 5.70895L15.6093 5.6947C15.6504 6.16712 15.585 6.64259 15.4175 7.08788C15.2501 7.53318 14.9846 7.93758 14.6398 8.27287C14.2949 8.60805 13.8789 8.86612 13.4208 9.02888C12.9627 9.19163 12.4736 9.25523 11.9876 9.21526L12.0015 9.22951C11.5885 9.18908 11.1713 9.23836 10.7803 9.37381C10.3893 9.50919 10.034 9.72744 9.74039 10.0127C9.44674 10.2979 9.22199 10.6431 9.08234 11.0231C8.94276 11.4031 8.89176 11.8085 8.93304 12.2101L8.91915 12.1966C8.96005 12.6689 8.89439 13.1443 8.72688 13.5895C8.5593 14.0346 8.29389 14.4389 7.94908 14.7741C7.60425 15.1093 7.18835 15.3673 6.73039 15.5302C6.27242 15.693 5.78342 15.7569 5.29749 15.7171L5.31138 15.7306C4.73003 15.6775 4.14599 15.8001 3.63892 16.0815C3.13186 16.363 2.72644 16.7896 2.478 17.3033C2.22954 17.817 2.15013 18.3926 2.25061 18.9518C2.35109 19.5109 2.62657 20.0263 3.03945 20.4276C3.45234 20.829 3.98253 21.0968 4.55773 21.1944C5.13293 21.2921 5.72512 21.2149 6.25353 20.9734C6.78193 20.7319 7.22085 20.3379 7.51038 19.8449C7.79994 19.352 7.92601 18.7843 7.87139 18.2191L7.88605 18.2326C7.845 17.7602 7.91058 17.2849 8.07809 16.8396C8.24551 16.3944 8.511 15.99 8.85581 15.6548C9.20069 15.3196 9.61664 15.0615 10.0746 14.8988C10.5327 14.7359 11.0217 14.6722 11.5077 14.7121ZM17.1996 10.7633C16.9071 11.0493 16.6832 11.3944 16.5437 11.7741C16.4042 12.1538 16.3526 12.5587 16.3925 12.9601L16.3786 12.9466C16.4197 13.419 16.3541 13.8944 16.1866 14.3396C16.0191 14.7849 15.7537 15.1892 15.4089 15.5244C15.064 15.8596 14.648 16.1177 14.19 16.2804C13.732 16.4433 13.2429 16.507 12.757 16.4671L12.7708 16.4806C12.1896 16.4281 11.6057 16.551 11.0989 16.8328C10.5921 17.1145 10.1871 17.5414 9.93902 18.0551C9.69097 18.5689 9.61188 19.1444 9.71265 19.7035C9.81349 20.2625 10.0892 20.7777 10.5022 21.1788C10.9152 21.5799 11.4454 21.8474 12.0205 21.9448C12.5957 22.0423 13.1877 21.9649 13.716 21.7234C14.2443 21.4817 14.683 21.0877 14.9724 20.5947C15.2618 20.1018 15.3878 19.5342 15.3332 18.9692L15.3478 18.9827C15.3068 18.5103 15.3723 18.0349 15.5398 17.5896C15.7073 17.1444 15.9728 16.7401 16.3176 16.4048C16.6625 16.0696 17.0784 15.8115 17.5364 15.6488C17.9945 15.486 18.4835 15.4222 18.9695 15.4621L18.9548 15.4486C19.4296 15.4901 19.9076 15.4144 20.3444 15.2286C20.7811 15.0427 21.1625 14.7527 21.4533 14.3854C21.744 14.0181 21.9347 13.5854 22.0075 13.1274C22.0805 12.6694 22.0332 12.2009 21.8703 11.7653C21.7073 11.3298 21.4339 10.9413 21.0754 10.6358C20.7168 10.3303 20.2848 10.1178 19.8192 10.0179C19.3536 9.91795 18.8697 9.93385 18.4121 10.0641C17.9546 10.1945 17.5383 10.4349 17.2019 10.7633H17.1996Z"
                        fill="currentColor"
                    />
                </svg>
            </div>
            <h1 class="text-4xl font-serif font-medium tracking-tight">Actimate</h1>
        </div>
        <p class="text-xs uppercase tracking-widest text-gray-500 mt-2 font-sans">AI-Powered Productivity Coaching</p>
    </header>

    <!-- Hero Section -->
    <section class="max-w-7xl mx-auto px-6 pt-12 pb-24 grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <div class="flex flex-col items-start space-y-8">
            <h2 class="text-6xl md:text-7xl font-serif leading-[1.1]">
                Turn chaotic<br/>
                schedules into<br/>
                intentional<br/>
                progress.
            </h2>
            <p class="text-gray-600 max-w-md leading-relaxed">
                Actimate combines AI-powered calendar integration with proactive accountability coaching to help you achieve your goals—even with ADHD or a packed schedule.
            </p>
            <div class="pt-2">
                <AppButtons />
            </div>
        </div>
        
        <div class="relative flex justify-center items-center">
            <!-- Abstract Background Shapes -->
            <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[500px] h-[500px] opacity-30 pointer-events-none">
                 <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-full fill-primary-100">
                    <path d="M44.7,-76.4C58.9,-69.2,71.8,-59.1,81.6,-46.6C91.4,-34.1,98.2,-19.2,95.8,-5.2C93.4,8.8,81.8,21.9,71.2,33.7C60.6,45.4,51,55.8,39.9,64.4C28.8,73,16.2,79.8,2.6,75.3C-11,70.8,-25.6,55,-38.7,42.5C-51.8,30,-63.4,20.8,-69.3,8.7C-75.2,-3.4,-75.4,-18.4,-68.8,-31.6C-62.2,-44.8,-48.8,-56.2,-35.4,-63.8C-22,-71.4,-8.6,-75.2,5.2,-84.2C19,-93.2,30.5,-107.4,44.7,-76.4Z" transform="translate(100 100)" />
                  </svg>
            </div>
            
            <PhoneMockup>
                <!-- Mockup Content -->
                <div class="flex flex-col h-full p-6 pt-16">
                    <div class="text-xs text-gray-500 uppercase tracking-widest mb-4">Today's Focus</div>
                    <h3 class="text-2xl font-serif mb-6">Launch product website</h3>
                    <div class="space-y-3 mb-6">
                        <div class="flex items-center gap-3 p-3 bg-white rounded-lg border border-gray-200">
                            <div class="w-4 h-4 rounded border-2 border-primary-500"></div>
                            <span class="text-sm">Review design mockups</span>
                            <span class="text-xs text-gray-400 ml-auto">2pm</span>
                        </div>
                        <div class="flex items-center gap-3 p-3 bg-white rounded-lg border border-gray-200">
                            <div class="w-4 h-4 rounded border-2 border-gray-300"></div>
                            <span class="text-sm">Write homepage copy</span>
                            <span class="text-xs text-gray-400 ml-auto">4pm</span>
                        </div>
                    </div>
                    <div class="mt-auto mb-12 p-4 bg-primary-50 rounded-lg border border-primary-200">
                        <p class="text-xs font-medium text-primary-900">💬 Check-in from your coach</p>
                        <p class="text-xs text-primary-700 mt-1">How's the website progress?</p>
                    </div>
                </div>
            </PhoneMockup>
        </div>
    </section>

    <!-- Dark Section (Principles) -->
    <section class="bg-[#1C1C1C] text-white py-24 overflow-hidden relative">
        <div class="max-w-7xl mx-auto px-6 mb-16">
            <p class="text-xl md:text-2xl font-serif max-w-lg leading-relaxed text-gray-300">
                Actimate is built on three core principles that turn scattered focus into consistent achievement.
            </p>
        </div>

        <div class="relative w-full overflow-hidden min-h-[280px] md:min-h-[320px] flex items-center">
            <div 
                class="flex transition-transform duration-700 ease-in-out px-6"
                style="transform: translateX(-{currentSlide * 100}%)"
            >
                {#each principles as principle, index}
                    <div class="w-full flex-shrink-0 flex justify-center items-center">
                        <div class="inline-flex items-baseline">
                            <span 
                                class="text-[120px] md:text-[180px] font-serif font-light transition-opacity duration-700"
                                style={principle.numberStyle}
                            >
                                {principle.number}
                            </span>
                            <div class="flex flex-col ml-4 md:ml-8">
                                <span class="text-5xl md:text-7xl font-serif whitespace-normal">{principle.title1}</span>
                                <span class="text-5xl md:text-7xl font-serif font-bold whitespace-normal">{principle.title2}</span>
                            </div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>

        <div class="max-w-7xl mx-auto px-6 mt-12 flex justify-between items-center">
            <!-- Navigation Arrows -->
            <button 
                onclick={prevSlide}
                class="text-white hover:text-primary-500 transition-colors p-2"
                aria-label="Previous slide"
            >
                <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M15 18L9 12L15 6" />
                </svg>
            </button>

            <!-- Dots Navigation -->
            <div class="flex gap-2">
                {#each principles as _, index}
                    <button
                        onclick={() => goToSlide(index)}
                        class={[
                            'w-3 h-3 rounded-full transition-all duration-300',
                            currentSlide === index ? 'bg-white scale-110' : 'bg-gray-600 hover:bg-gray-400'
                        ]}
                        aria-label="Go to slide {index + 1}"
                    ></button>
                {/each}
            </div>

            <button 
                onclick={nextSlide}
                class="text-white hover:text-primary-500 transition-colors p-2"
                aria-label="Next slide"
            >
                <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M9 18L15 12L9 6" />
                </svg>
            </button>
        </div>
    </section>

    <!-- Why we're different -->
    <section class="py-32 max-w-6xl mx-auto px-6">
        <div class="text-center mb-12">
            <h2 class="text-4xl md:text-5xl font-serif mb-6">Built for how ADHD brains actually work</h2>
            <p class="text-gray-600 max-w-2xl mx-auto leading-relaxed">
                Actimate isn't another productivity app that assumes you'll just "try harder." It's built on proven systems (GTD + Atomic Habits) with an AI partner that provides the external accountability your brain needs.
            </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mt-20">
            <!-- Card 1: One thing at a time -->
            <div class="p-8 flex items-start gap-6 hover:bg-gray-50 transition-all duration-300 rounded-xl">
                <div class="flex-1">
                    <h3 class="text-2xl font-serif mb-4">One thing at a time</h3>
                    <p class="text-gray-600 leading-relaxed">
                        No overwhelming lists. Actimate shows you the single next action for each goal—so you always know exactly what to do.
                    </p>
                </div>
                <div class="w-16 h-16 text-primary-500 flex-shrink-0">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="w-full h-full">
                        <circle cx="12" cy="12" r="10"></circle>
                        <circle cx="12" cy="12" r="6"></circle>
                        <circle cx="12" cy="12" r="2"></circle>
                    </svg>
                </div>
            </div>

            <!-- Card 2: Accountability that actually works -->
            <div class="p-8 flex items-start gap-6 hover:bg-gray-50 transition-all duration-300 rounded-xl">
                <div class="flex-1">
                    <h3 class="text-2xl font-serif mb-4">Accountability that actually works</h3>
                    <p class="text-gray-600 leading-relaxed">
                        Pia, your AI accountability partner, checks in on your progress and follows up when you go quiet. No judgment, just support.
                    </p>
                </div>
                <div class="w-16 h-16 text-primary-500 flex-shrink-0">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="w-full h-full">
                        <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path>
                        <circle cx="9" cy="7" r="4"></circle>
                        <path d="M23 21v-2a4 4 0 0 0-3-3.87"></path>
                        <path d="M16 3.13a4 4 0 0 1 0 7.75"></path>
                    </svg>
                </div>
            </div>

            <!-- Card 3: Everything connected -->
            <div class="p-8 flex items-start gap-6 hover:bg-gray-50 transition-all duration-300 rounded-xl">
                <div class="flex-1">
                    <h3 class="text-2xl font-serif mb-4">Everything connected</h3>
                    <p class="text-gray-600 leading-relaxed">
                        Goals, habits, tasks, and calendar in one place. Pia sees the full picture and helps you stay consistent across all of it.
                    </p>
                </div>
                <div class="w-16 h-16 text-primary-500 flex-shrink-0">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="w-full h-full">
                        <path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path>
                        <path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path>
                    </svg>
                </div>
            </div>

            <!-- Card 4: Streaks you want to protect -->
            <div class="p-8 flex items-start gap-6 hover:bg-gray-50 transition-all duration-300 rounded-xl">
                <div class="flex-1">
                    <h3 class="text-2xl font-serif mb-4">Streaks you want to protect</h3>
                    <p class="text-gray-600 leading-relaxed">
                        Visual progress tracking, milestone celebrations, and streak counters give your brain the dopamine hits it needs to keep going.
                    </p>
                </div>
                <div class="w-16 h-16 text-primary-500 flex-shrink-0">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="w-full h-full">
                        <circle cx="12" cy="8" r="7"></circle>
                        <polyline points="8.21 13.89 7 23 12 20 17 23 15.79 13.88"></polyline>
                    </svg>
                </div>
            </div>

            <!-- Card 5: Identity-based goals -->
            <div class="p-8 flex items-start gap-6 hover:bg-gray-50 transition-all duration-300 rounded-xl">
                <div class="flex-1">
                    <h3 class="text-2xl font-serif mb-4">Identity-based goals</h3>
                    <p class="text-gray-600 leading-relaxed">
                        Based on James Clear's Atomic Habits: link your habits to who you want to become, not just what you want to do.
                    </p>
                </div>
                <div class="w-16 h-16 text-primary-500 flex-shrink-0">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="w-full h-full">
                        <polygon points="3 11 22 2 13 21 11 13 3 11"></polygon>
                    </svg>
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
            <h2 class="text-4xl font-serif">Actimate is designed to help you<br>make progress on what matters.</h2>
            <p class="text-gray-500 mt-4 max-w-md">
                Our core features combine AI-powered scheduling with proactive accountability to keep you on track.
            </p>
        </div>

        <div class="max-w-6xl mx-auto px-6 space-y-8">
            <!-- Card 1 -->
            <div class="bg-[#1C1C1C] rounded-[2rem] p-12 md:p-20 text-white relative overflow-hidden flex flex-col md:flex-row items-center gap-12">
                <div class="relative z-10 w-full md:w-1/2 flex justify-center">
                     <PhoneMockup>
                         <div class="p-6 flex flex-col h-full bg-white text-black">
                             <div class="text-xs text-gray-500 uppercase tracking-widest mb-4">This Week</div>
                             <h4 class="text-xl font-serif mb-4">Your Schedule</h4>
                             <div class="space-y-2">
                                 <div class="p-3 bg-primary-50 rounded-lg border border-primary-200">
                                     <span class="text-sm font-medium">Product Planning</span>
                                     <p class="text-xs text-gray-500 mt-1">Mon 9:00 AM - 10:30 AM</p>
                                 </div>
                                 <div class="p-3 bg-gray-50 rounded-lg border border-gray-200">
                                     <span class="text-sm">Team Meeting</span>
                                     <p class="text-xs text-gray-500 mt-1">Mon 2:00 PM - 3:00 PM</p>
                                 </div>
                             </div>
                         </div>
                     </PhoneMockup>
                </div>
                <div class="w-full md:w-1/2 relative z-10">
                    <p class="text-xs uppercase tracking-widest text-gray-400 mb-2">Smart Scheduling</p>
                    <h3 class="text-4xl md:text-5xl font-serif mb-6">AI finds time<br>for your goals</h3>
                    <p class="text-gray-400 leading-relaxed">
                        Our AI analyzes your calendar and automatically schedules time for your most important goals. No more hoping you'll find time—Actimate makes it happen.
                    </p>
                </div>
                <!-- Abstract BG -->
                <div class="absolute left-0 bottom-0 w-1/2 h-full bg-white opacity-5 rounded-full blur-3xl translate-y-1/2 -translate-x-1/4"></div>
            </div>

             <!-- Card 2 -->
            <div class="bg-[#1C1C1C] rounded-[2rem] p-12 md:p-20 text-white relative overflow-hidden flex flex-col md:flex-row-reverse items-center gap-12">
                <div class="relative z-10 w-full md:w-1/2 flex justify-center">
                     <PhoneMockup>
                         <div class="p-6 flex flex-col h-full bg-white text-black">
                             <div class="bg-primary-500 text-white p-4 rounded-xl mb-4">
                                 <p class="text-sm font-medium">💪 Great progress today!</p>
                                 <p class="text-xs opacity-90 mt-1">You completed 3 of 3 scheduled goals.</p>
                             </div>
                             <div class="mt-4 p-4 bg-gray-50 rounded-lg">
                                 <p class="text-xs text-gray-500 mb-2">Tomorrow's Focus</p>
                                 <p class="text-sm font-medium">Product roadmap review</p>
                             </div>
                         </div>
                     </PhoneMockup>
                </div>
                <div class="w-full md:w-1/2 relative z-10">
                    <p class="text-xs uppercase tracking-widest text-gray-400 mb-2">Proactive Coaching</p>
                    <h3 class="text-4xl md:text-5xl font-serif mb-6">Your AI coach<br>checks in</h3>
                    <p class="text-gray-400 leading-relaxed">
                        Actimate doesn't just schedule—it actively coaches you. Get timely check-ins, encouragement, and accountability when you need it most.
                    </p>
                </div>
            </div>

             <!-- Card 3 -->
            <div class="bg-[#1C1C1C] rounded-[2rem] p-12 md:p-20 text-white relative overflow-hidden flex flex-col md:flex-row items-center gap-12">
                <div class="relative z-10 w-full md:w-1/2 flex justify-center">
                     <PhoneMockup>
                         <div class="p-6 flex flex-col h-full bg-white text-black">
                             <div class="text-xs text-gray-500 uppercase tracking-widest mb-4">Connected Calendars</div>
                             <div class="space-y-3">
                                 <div class="flex items-center gap-3 p-3 bg-white rounded-lg border border-gray-200">
                                     <div class="w-8 h-8 bg-blue-100 rounded flex items-center justify-center text-xs">📅</div>
                                     <span class="text-sm">Google Calendar</span>
                                     <span class="text-xs text-green-600 ml-auto">✓ Synced</span>
                                 </div>
                             </div>
                         </div>
                     </PhoneMockup>
                </div>
                <div class="w-full md:w-1/2 relative z-10">
                    <p class="text-xs uppercase tracking-widest text-gray-400 mb-2">Calendar Integration</p>
                    <h3 class="text-4xl md:text-5xl font-serif mb-6">Works with<br>your calendar</h3>
                    <p class="text-gray-400 leading-relaxed">
                        Seamlessly integrates with Google Calendar, Outlook, and Apple Calendar. Actimate works within your existing workflow.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- How It Works -->
    <section class="py-24 bg-[#FCFAF7]">
        <div class="max-w-7xl mx-auto px-6">
            <h2 class="text-3xl font-serif mb-12">How Actimate Works</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Step 1 -->
                <div class="bg-white p-8 rounded-xl aspect-[4/5] flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-8 h-8 bg-primary-100 rounded-full flex items-center justify-center text-xs font-bold text-primary-600">01</div>
                    <h3 class="text-2xl font-serif">Set Your Goals</h3>
                    <div class="text-xs text-gray-400 uppercase tracking-widest">Connect & Define</div>
                </div>
                 <!-- Step 2 -->
                <div class="bg-white p-8 rounded-xl aspect-[4/5] flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-8 h-8 bg-primary-100 rounded-full flex items-center justify-center text-xs font-bold text-primary-600">02</div>
                    <h3 class="text-2xl font-serif">AI Schedules Time</h3>
                    <div class="text-xs text-gray-400 uppercase tracking-widest">Automatic Planning</div>
                </div>
                 <!-- Step 3 -->
                <div class="bg-white p-8 rounded-xl aspect-[4/5] flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-8 h-8 bg-primary-100 rounded-full flex items-center justify-center text-xs font-bold text-primary-600">03</div>
                    <h3 class="text-2xl font-serif">Get Coached</h3>
                    <div class="text-xs text-gray-400 uppercase tracking-widest">Stay Accountable</div>
                </div>
                 <!-- Step 4 -->
                <div class="bg-white p-8 rounded-xl aspect-[4/5] flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-8 h-8 bg-primary-100 rounded-full flex items-center justify-center text-xs font-bold text-primary-600">04</div>
                    <h3 class="text-2xl font-serif">Make Progress</h3>
                    <div class="text-xs text-gray-400 uppercase tracking-widest">Achieve Your Goals</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Founder Section -->
    <section class="py-32 max-w-5xl mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
            <div>
                <p class="text-xs uppercase tracking-widest text-gray-500 mb-4">Built by someone who gets it</p>
                <h2 class="text-4xl font-serif mb-6">From personal struggle to powerful solution</h2>
                <p class="text-gray-600 leading-relaxed mb-8">
                    Actimate was created by Kevin Jordan, who built it to solve his own challenges with ADHD while juggling ambitious goals, building companies, and raising a young family. If you've ever felt overwhelmed by your schedule, Actimate was built for you.
                </p>
                <AppButtons />
            </div>
            <div class="flex justify-center relative">
                <!-- Founder Illustration -->
                <div class="w-64 h-64 relative">
                    <svg viewBox="0 0 200 200" class="w-full h-full stroke-black fill-none stroke-[1.5]">
                        <circle cx="100" cy="80" r="30" />
                        <path d="M70,110 L70,170" />
                        <path d="M130,110 L130,170" />
                        <path d="M70,130 L50,150" />
                        <path d="M130,130 L150,150" />
                        <path d="M70,110 L130,110 L130,170 L70,170 Z" />
                    </svg>
                    <div class="absolute -z-10 top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-80 h-80 bg-primary-100 rounded-full opacity-50 blur-2xl"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonial -->
    <section class="bg-[#1C1C1C] text-white py-32">
        <div class="max-w-7xl mx-auto px-6 grid grid-cols-1 lg:grid-cols-2 gap-16">
            <div>
                <h2 class="text-2xl font-serif mb-12">What early users are saying</h2>
                <h3 class="text-5xl md:text-7xl font-serif leading-tight">Finally making<br>real progress.</h3>
            </div>
            <div class="flex flex-col justify-end">
                <p class="text-gray-400 text-lg leading-relaxed mb-8">
                    "As someone with ADHD, I've tried every productivity app out there. Actimate is different—it doesn't just remind me to do things, it actually helps me make time for them. The AI coaching feels like having a supportive accountability partner who understands my brain."
                </p>
                <div>
                    <p class="font-bold">Sarah M.</p>
                    <p class="text-sm text-gray-500">Product Manager, Early Access User</p>
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
                    Ready to turn your chaotic schedule into intentional progress?
                </p>
                <AppButtons />
            </div>
            <div class="flex justify-center relative z-10">
                 <PhoneMockup>
                     <div class="flex flex-col items-center justify-center h-full bg-white p-6">
                         <div class="w-16 h-16 text-primary-500 mb-4">
                             <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                 <path
                                     fill-rule="evenodd"
                                     clip-rule="evenodd"
                                     d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196ZM11.5077 14.7121L11.493 14.6986C11.9061 14.739 12.3232 14.6897 12.7143 14.5543C13.1053 14.4188 13.4605 14.2007 13.7542 13.9154C14.0477 13.6302 14.2726 13.285 14.4121 12.905C14.5518 12.525 14.6028 12.1196 14.5615 11.718L14.5762 11.7315C14.5351 11.2591 14.6007 10.7838 14.7681 10.3385C14.9356 9.89327 15.2011 9.48893 15.5459 9.15368C15.8908 8.8185 16.3068 8.56042 16.7648 8.39767C17.2228 8.23481 17.7118 8.17111 18.1978 8.21099L18.1832 8.19749C18.7645 8.25059 19.3485 8.12801 19.8556 7.84656C20.3627 7.56511 20.7681 7.13845 21.0165 6.62479C21.265 6.11114 21.3444 5.53548 21.2439 4.97634C21.1435 4.4172 20.868 3.9018 20.4551 3.50044C20.0422 3.09909 19.512 2.8313 18.9368 2.73364C18.3616 2.63596 17.7695 2.71315 17.241 2.95467C16.7126 3.19618 16.2737 3.59027 15.9842 4.08319C15.6946 4.57609 15.5685 5.14383 15.6232 5.70895L15.6093 5.6947C15.6504 6.16712 15.585 6.64259 15.4175 7.08788C15.2501 7.53318 14.9846 7.93758 14.6398 8.27287C14.2949 8.60805 13.8789 8.86612 13.4208 9.02888C12.9627 9.19163 12.4736 9.25523 11.9876 9.21526L12.0015 9.22951C11.5885 9.18908 11.1713 9.23836 10.7803 9.37381C10.3893 9.50919 10.034 9.72744 9.74039 10.0127C9.44674 10.2979 9.22199 10.6431 9.08234 11.0231C8.94276 11.4031 8.89176 11.8085 8.93304 12.2101L8.91915 12.1966C8.96005 12.6689 8.89439 13.1443 8.72688 13.5895C8.5593 14.0346 8.29389 14.4389 7.94908 14.7741C7.60425 15.1093 7.18835 15.3673 6.73039 15.5302C6.27242 15.693 5.78342 15.7569 5.29749 15.7171L5.31138 15.7306C4.73003 15.6775 4.14599 15.8001 3.63892 16.0815C3.13186 16.363 2.72644 16.7896 2.478 17.3033C2.22954 17.817 2.15013 18.3926 2.25061 18.9518C2.35109 19.5109 2.62657 20.0263 3.03945 20.4276C3.45234 20.829 3.98253 21.0968 4.55773 21.1944C5.13293 21.2921 5.72512 21.2149 6.25353 20.9734C6.78193 20.7319 7.22085 20.3379 7.51038 19.8449C7.79994 19.352 7.92601 18.7843 7.87139 18.2191L7.88605 18.2326C7.845 17.7602 7.91058 17.2849 8.07809 16.8396C8.24551 16.3944 8.511 15.99 8.85581 15.6548C9.20069 15.3196 9.61664 15.0615 10.0746 14.8988C10.5327 14.7359 11.0217 14.6722 11.5077 14.7121ZM17.1996 10.7633C16.9071 11.0493 16.6832 11.3944 16.5437 11.7741C16.4042 12.1538 16.3526 12.5587 16.3925 12.9601L16.3786 12.9466C16.4197 13.419 16.3541 13.8944 16.1866 14.3396C16.0191 14.7849 15.7537 15.1892 15.4089 15.5244C15.064 15.8596 14.648 16.1177 14.19 16.2804C13.732 16.4433 13.2429 16.507 12.757 16.4671L12.7708 16.4806C12.1896 16.4281 11.6057 16.551 11.0989 16.8328C10.5921 17.1145 10.1871 17.5414 9.93902 18.0551C9.69097 18.5689 9.61188 19.1444 9.71265 19.7035C9.81349 20.2625 10.0892 20.7777 10.5022 21.1788C10.9152 21.5799 11.4454 21.8474 12.0205 21.9448C12.5957 22.0423 13.1877 21.9649 13.716 21.7234C14.2443 21.4817 14.683 21.0877 14.9724 20.5947C15.2618 20.1018 15.3878 19.5342 15.3332 18.9692L15.3478 18.9827C15.3068 18.5103 15.3723 18.0349 15.5398 17.5896C15.7073 17.1444 15.9728 16.7401 16.3176 16.4048C16.6625 16.0696 17.0784 15.8115 17.5364 15.6488C17.9945 15.486 18.4835 15.4222 18.9695 15.4621L18.9548 15.4486C19.4296 15.4901 19.9076 15.4144 20.3444 15.2286C20.7811 15.0427 21.1625 14.7527 21.4533 14.3854C21.744 14.0181 21.9347 13.5854 22.0075 13.1274C22.0805 12.6694 22.0332 12.2009 21.8703 11.7653C21.7073 11.3298 21.4339 10.9413 21.0754 10.6358C20.7168 10.3303 20.2848 10.1178 19.8192 10.0179C19.3536 9.91795 18.8697 9.93385 18.4121 10.0641C17.9546 10.1945 17.5383 10.4349 17.2019 10.7633H17.1996Z"
                                     fill="currentColor"
                                 />
                             </svg>
                         </div>
                         <h1 class="text-3xl font-serif">Actimate</h1>
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
    /* Custom stroke text utility */
    .stroke-text {
        -webkit-text-stroke: 1px rgba(255, 255, 255, 0.5);
        color: transparent;
    }
</style>

