<script lang="ts">
	import { onMount } from 'svelte';

    // Data for sections
    const navLinks = ["Programs", "Impact", "Partners", "About"];
    
    const logos = [
        { name: "NVIDIA", width: 120 },
        { name: "OpenAI", width: 100 },
        { name: "X.AI", width: 80 },
        { name: "!ntropy", width: 90 },
        { name: "Basis", width: 80 }
    ];

    const features = [
        {
            tag: "ROLE-SPECIFIC TRAINING",
            title: "Customized AI programs for every professional role",
            image: "phone",
            color: "bg-gray-100"
        },
        {
            tag: "1000X LEVERAGE PRINCIPLE",
            title: "Transform AI from tool to force multiplier",
            image: "video",
            color: "bg-gray-100"
        },
        {
            tag: "WORKFLOW INTEGRATION",
            title: "Practical AI implementation in daily operations",
            image: "search",
            color: "bg-gray-100"
        },
        {
            tag: "MEASURABLE IMPACT",
            title: "40% faster tasks, 3x output, 12x code productivity",
            image: "editor",
            color: "bg-gray-100"
        },
        {
            tag: "PROFESSIONAL CERTIFICATION",
            title: "Recognized credentials for AI-capable professionals",
            image: "admin",
            color: "bg-gray-100"
        },
        {
            tag: "CONTINUOUS COMMUNITY",
            title: "Exclusive forums and ongoing learning support",
            image: "analytics",
            color: "bg-gray-100"
        }
    ];

    const testimonials = [
        {
            quote: "AI Fluency Company transformed our workforce from AI-curious to AI-capable in months. The productivity gains are measurable and transformative.",
            name: "Dr. Ahmed Al-Mansoori",
            role: "Director of Digital Transformation, Abu Dhabi Government",
            avatar: "AM"
        },
        {
            quote: "This isn't theoretical training. Our team now uses AI daily, multiplying output while reducing routine work. The ROI is undeniable.",
            name: "Sarah Chen",
            role: "Chief Operating Officer, MENA Financial Services",
            avatar: "SC"
        },
         {
            quote: "The partnership with NVIDIA and OpenAI practitioners gives us confidence we're learning from the frontier, not following outdated curricula.",
            name: "Mohammed Al-Rashid",
            role: "Head of Innovation, Healthcare Authority",
            avatar: "MR"
        },
        {
            quote: "Every professional deserves AI fluency. This program ensures our workforce isn't left behind as AI reshapes every industry.",
            name: "Fatima Hassan",
            role: "Chief Human Resources Officer",
            avatar: "FH"
        },
        {
            quote: "The 1000x leverage principle changed how we think about productivity. AI isn't replacing us—it's amplifying our capabilities exponentially.",
            name: "David Park",
            role: "Engineering Director",
            avatar: "DP"
        },
        {
            quote: "Those who delay risk irrelevance. AI Fluency Company gave us the competitive edge before market pressures forced reactive responses.",
            name: "Layla Abdullah",
            role: "CEO, Technology Consulting",
            avatar: "LA"
        }
    ];

    const partnershipServices = [
        "Strategic partnership with NVIDIA for AI infrastructure",
        "Direct access to OpenAI practitioners",
        "Partnership with X.AI for advanced implementation",
        "Advisory connections with !ntropy and Basis",
        "Frontier AI research lab expertise",
        "Executive briefings for government ministries",
        "Continuous learning community access"
    ];

    const comparisons = [
        {
            tag: "WORKFORCE READINESS",
            left: "85 million jobs displaced by 2025, workforce unprepared for AI-driven economy",
            right: "Every professional AI-capable, positioned for 97 million new human-AI collaboration roles"
        },
        {
            tag: "PRODUCTIVITY IMPACT",
            left: "Manual workflows, one-size-fits-all output, competitive disadvantage",
            right: "40% faster tasks, 3x output multiplication, 12x code productivity with AI augmentation"
        },
        {
            tag: "COMPETITIVE POSITION",
            left: "Reactive responses as competitors surge ahead, risk of market irrelevance",
            right: "Early adoption advantage, market leadership, future-proofed workforce"
        },
        {
            tag: "ECONOMIC EQUITY",
            left: "Two-tier economy: those with AI fluency thrive, others lose economic value",
            right: "Democratized AI capability, downside protection, inclusive economic participation"
        },
        {
            tag: "IMPLEMENTATION APPROACH",
            left: "Generic online courses, theoretical knowledge, no workflow integration",
            right: "Role-specific training, hands-on capability building, practical workflow redesign"
        }
    ];

    const faqs = [
        "What is AI fluency training and who needs it?",
        "How does this differ from online courses like Coursera?",
        "What are the measurable productivity outcomes?",
        "How long does the training program take?",
        "What's the ROI for organizations investing in AI fluency?",
        "How do you ensure practical application, not just theory?",
        "What professional certifications are offered?",
        "Can programs be customized for specific industries?",
        "How do you address workforce displacement fears?"
    ];

</script>

<div class="font-sans text-gray-900 bg-white selection:bg-primary-200 selection:text-black">
    <!-- Navbar -->
    <nav class="sticky top-0 z-50 bg-white/80 backdrop-blur-md border-b border-gray-100">
        <div class="max-w-[1400px] mx-auto px-6 h-16 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <!-- Logo Mark -->
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-primary-600">
                    <path d="M12 2C12 2 8 6 8 12C8 18 12 22 12 22C12 22 16 18 16 12C16 6 12 2 12 2Z" fill="currentColor"/>
                    <path d="M2 12C2 12 6 8 12 8C18 8 22 12 22 12C22 12 18 16 12 16C6 16 2 12 2 12Z" fill="currentColor" opacity="0.6"/>
                </svg>
                <span class="font-medium text-lg tracking-tight">AI Fluency Company</span>
            </div>

            <div class="hidden md:flex items-center gap-8 text-sm font-medium text-gray-600">
                {#each navLinks as link}
                    <a href="#" class="hover:text-black transition-colors">{link}</a>
                {/each}
            </div>

            <button class="bg-black text-white px-5 py-2 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
                Schedule Briefing
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="pt-20 pb-16 px-6 text-center overflow-hidden">
        <div class="max-w-4xl mx-auto mb-12">
            <h1 class="font-serif text-6xl md:text-7xl lg:text-[5rem] leading-[1.1] mb-6 font-normal tracking-tight">
                Transform UAE professionals into <span class="text-primary-600">AI-capable</span> workers
            </h1>
            <p class="text-lg md:text-xl text-gray-600 max-w-2xl mx-auto mb-8 leading-relaxed">
                Role-specific training and workflow integration starting with Abu Dhabi government. Capturing the $4B+ Global South market through measurable 1000x productivity gains.
            </p>
            <button class="bg-black text-white px-8 py-3 rounded-full text-base font-medium hover:bg-gray-800 transition-colors">
                Schedule Executive Briefing
            </button>
        </div>

        <!-- Hero Image Collage Mockup -->
        <div class="relative max-w-[1400px] mx-auto h-[400px] md:h-[600px] mt-12 select-none pointer-events-none">
            <!-- We will build a CSS composition of screens -->
            <div class="relative w-full h-full flex justify-center items-end">
                
                <!-- Left Laptop -->
                <div class="absolute left-[-10%] bottom-0 w-[60%] md:w-[45%] z-10 transform -translate-x-10 translate-y-10">
                     <div class="bg-gray-900 rounded-t-xl p-1 shadow-2xl border border-gray-800 aspect-[16/10] overflow-hidden">
                        <!-- Screen Content -->
                        <div class="bg-gray-800 w-full h-full rounded-lg relative overflow-hidden">
                            <div class="absolute inset-0 bg-gradient-to-br from-blue-900 to-black opacity-80"></div>
                            <div class="p-4 text-white">
                                <div class="text-xs text-gray-400 mb-2">Space Tech</div>
                                <div class="h-2 w-20 bg-gray-600 rounded mb-4"></div>
                                <div class="grid grid-cols-2 gap-4">
                                    <div class="h-20 bg-gray-700/50 rounded"></div>
                                    <div class="h-20 bg-gray-700/50 rounded"></div>
                                </div>
                            </div>
                        </div>
                     </div>
                </div>

                <!-- Center Laptop (Main) -->
                <div class="absolute bottom-0 z-20 w-[70%] md:w-[50%] transform translate-y-5">
                    <div class="bg-black rounded-t-2xl p-2 shadow-2xl border border-gray-800 aspect-[16/10]">
                        <div class="bg-white w-full h-full rounded-xl overflow-hidden relative">
                            <!-- Mock UI -->
                            <div class="flex h-full">
                                <div class="w-1/3 bg-gray-50 p-4 border-r border-gray-100">
                                    <div class="h-8 w-8 bg-gray-200 rounded-full mb-4"></div>
                                    <div class="h-2 w-20 bg-gray-200 rounded mb-2"></div>
                                    <div class="h-2 w-16 bg-gray-200 rounded mb-6"></div>
                                    <div class="space-y-2">
                                        <div class="h-8 w-full bg-white border border-gray-200 rounded shadow-sm"></div>
                                        <div class="h-8 w-full bg-transparent rounded"></div>
                                    </div>
                                </div>
                                <div class="w-2/3 p-4">
                                    <div class="h-32 bg-gray-100 rounded-lg mb-4 flex items-center justify-center">
                                        <div class="w-12 h-12 bg-gray-300 rounded-full"></div>
                                    </div>
                                    <div class="h-4 w-3/4 bg-gray-100 rounded mb-2"></div>
                                    <div class="h-4 w-1/2 bg-gray-100 rounded"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Right Phone/Tablet -->
                <div class="absolute right-[-5%] bottom-10 w-[25%] md:w-[15%] z-30 transform translate-x-5">
                    <div class="bg-black rounded-[2rem] p-2 shadow-2xl border border-gray-800 aspect-[9/19]">
                        <div class="bg-white w-full h-full rounded-[1.5rem] overflow-hidden p-2 flex flex-col">
                             <div class="h-4 w-20 bg-gray-100 rounded mx-auto mb-4 mt-2"></div>
                             <div class="flex-1 bg-gray-50 rounded-xl p-2">
                                <div class="h-16 bg-sana-lime/20 rounded-lg mb-2"></div>
                                <div class="h-16 bg-blue-50 rounded-lg mb-2"></div>
                             </div>
                        </div>
                    </div>
                </div>

                 <!-- Another Right Screen (Tablet?) -->
                <div class="absolute right-[10%] bottom-0 w-[40%] md:w-[30%] z-10 transform translate-x-10 translate-y-10">
                     <div class="bg-white rounded-t-xl p-1 shadow-2xl border border-gray-200 aspect-[4/3] overflow-hidden">
                        <div class="bg-gray-50 w-full h-full rounded-lg p-3">
                             <div class="flex gap-2 mb-3">
                                <div class="w-1/3 h-20 bg-white shadow-sm rounded-lg"></div>
                                <div class="w-1/3 h-20 bg-white shadow-sm rounded-lg"></div>
                                <div class="w-1/3 h-20 bg-white shadow-sm rounded-lg"></div>
                             </div>
                             <div class="h-32 bg-white shadow-sm rounded-lg"></div>
                        </div>
                     </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Logos Section -->
    <section class="py-16 border-b border-gray-100">
        <div class="max-w-[1400px] mx-auto px-6 text-center">
            <p class="text-sm text-gray-500 mb-10">Strategic partnerships with frontier AI leaders</p>
            <div class="flex flex-wrap justify-center items-center gap-12 md:gap-16 opacity-70 hover:opacity-100 transition-all duration-500">
                {#each logos as logo}
                    <div class="h-8 flex items-center justify-center">
                        <!-- Placeholder for logo text/svg -->
                        <span class="font-bold text-2xl tracking-tight">{logo.name}</span>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Our Approach Grid -->
    <section class="py-24 px-6 bg-gray-50">
        <div class="max-w-[1400px] mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Our Approach</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    Beyond generic online courses. We combine role-specific training with workflow integration to transform your workforce into AI-capable professionals with measurable productivity gains.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                {#each features as feature}
                    <div class="group bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition-shadow duration-300 flex flex-col h-[500px]">
                        <div class="p-8 pb-0 flex-1">
                            <span class="inline-block bg-primary-500 text-white text-[10px] font-bold tracking-wider px-2 py-1 rounded mb-4 uppercase">
                                {feature.tag}
                            </span>
                            <h3 class="font-serif text-2xl leading-tight mb-4">
                                {feature.title}
                            </h3>
                        </div>
                        <div class="h-[300px] bg-gray-100 relative overflow-hidden mt-4 mx-4 rounded-t-xl group-hover:translate-y-[-5px] transition-transform duration-500">
                            <!-- Mockup Content based on type -->
                            {#if feature.image === 'phone'}
                                <div class="absolute bottom-[-20px] left-1/2 transform -translate-x-1/2 w-[180px] h-[350px] bg-black rounded-[2rem] border-4 border-black shadow-xl overflow-hidden">
                                     <div class="bg-white w-full h-full p-3 pt-8">
                                        <div class="h-2 w-12 bg-gray-200 rounded mx-auto mb-4"></div>
                                        <div class="space-y-2">
                                            <div class="h-16 bg-primary-50 rounded-lg"></div>
                                            <div class="h-16 bg-gray-50 rounded-lg"></div>
                                        </div>
                                     </div>
                                </div>
                            {:else if feature.image === 'video'}
                                <div class="absolute inset-0 p-4 flex items-end justify-center">
                                    <div class="w-full h-[90%] bg-gray-800 rounded-t-lg shadow-lg relative overflow-hidden">
                                        <div class="absolute inset-0 flex items-center justify-center text-white/20">
                                            <svg width="48" height="48" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 14.5v-9l6 4.5-6 4.5z"/></svg>
                                        </div>
                                        <div class="absolute bottom-4 left-4 flex gap-2">
                                            <div class="w-8 h-8 bg-gray-600 rounded-full"></div>
                                            <div class="w-8 h-8 bg-gray-600 rounded-full"></div>
                                        </div>
                                    </div>
                                </div>
                            {:else if feature.image === 'search'}
                                 <div class="absolute bottom-[-40px] right-[-20px] w-full h-full bg-white shadow-lg rounded-tl-2xl p-6 border border-gray-100">
                                     <div class="flex items-center gap-3 mb-4 border-b pb-4">
                                         <div class="w-8 h-8 bg-primary-500 rounded-full"></div>
                                         <div class="h-2 w-32 bg-gray-200 rounded"></div>
                                     </div>
                                     <div class="space-y-3">
                                         <div class="h-2 w-full bg-gray-100 rounded"></div>
                                         <div class="h-2 w-5/6 bg-gray-100 rounded"></div>
                                         <div class="h-2 w-4/6 bg-gray-100 rounded"></div>
                                     </div>
                                 </div>
                            {:else}
                                <div class="absolute inset-4 bg-white shadow-sm rounded-lg border border-gray-100 flex items-center justify-center">
                                    <div class="text-gray-300">UI Mockup</div>
                                </div>
                            {/if}
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-24 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Trusted by forward-thinking <br/> organizations</h2>
                <p class="text-lg text-gray-600 leading-relaxed mb-10">
                    From government ministries to private enterprises, leaders choose AI fluency <br/> to future-proof their workforce and gain competitive advantage.
                </p>
            </div>

            <div class="columns-1 md:columns-2 lg:columns-3 gap-6 space-y-6">
                {#each testimonials as testimonial}
                    <div class="break-inside-avoid bg-gray-50 p-8 rounded-2xl">
                        <p class="text-lg leading-relaxed mb-6">"{testimonial.quote}"</p>
                        <div class="flex items-center gap-3">
                            <div class="w-10 h-10 bg-gray-300 rounded-full flex items-center justify-center text-sm font-bold text-gray-600">
                                {testimonial.avatar}
                            </div>
                            <div>
                                <div class="font-medium">{testimonial.name}</div>
                                <div class="text-sm text-gray-500">{testimonial.role}</div>
                            </div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Partnership Section -->
    <section class="py-24 px-6 bg-white border-t border-gray-100">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Strategic partnerships <br/> with frontier AI leaders</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    Our partnerships with NVIDIA, OpenAI, and X.AI ensure you're learning <br/> from the cutting edge, not following outdated curricula.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="bg-gray-50 p-12 rounded-3xl h-full">
                    <h3 class="font-serif text-2xl mb-8">Partnership ecosystem</h3>
                    <ul class="space-y-4">
                        {#each partnershipServices as service}
                            <li class="flex items-center gap-3">
                                <div class="w-5 h-5 rounded-full bg-primary-500 flex items-center justify-center shrink-0">
                                    <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg>
                                </div>
                                <span class="text-gray-700">{service}</span>
                            </li>
                        {/each}
                    </ul>
                </div>
                <div class="h-full min-h-[500px] rounded-3xl overflow-hidden relative">
                    <!-- Placeholder image for people collaborating -->
                    <div class="absolute inset-0 bg-gray-200">
                        <div class="w-full h-full bg-[url('https://images.unsplash.com/photo-1522071820081-009f0129c71c?q=80&w=2070&auto=format&fit=crop')] bg-cover bg-center grayscale opacity-80 hover:grayscale-0 transition-all duration-700"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Impact Stories Section -->
    <section class="py-24 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
            <div class="flex justify-between items-end mb-12">
                <p class="text-lg text-gray-600 max-w-xl">AI fluency transformation across government and enterprise. See the measurable impact.</p>
                <div class="flex gap-2">
                    <button class="w-10 h-10 rounded-full border border-gray-200 flex items-center justify-center hover:bg-gray-50">
                        ←
                    </button>
                    <button class="w-10 h-10 rounded-full bg-black text-white flex items-center justify-center hover:bg-gray-800">
                        →
                    </button>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Card 1 -->
                <div class="aspect-[4/5] relative rounded-2xl overflow-hidden group cursor-pointer">
                    <div class="absolute inset-0 bg-gradient-to-br from-primary-900 to-gray-900">
                        <!-- Mock Background Image -->
                        <div class="absolute inset-0 opacity-50 bg-gradient-to-t from-black via-transparent to-transparent"></div>
                        <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1549317661-bd32c8ce0db2?q=80&w=2070&auto=format&fit=crop')] bg-cover bg-center mix-blend-overlay opacity-30"></div>
                    </div>
                    <div class="absolute inset-0 p-8 flex flex-col justify-between text-white">
                        <div>
                            <h3 class="font-serif text-3xl leading-tight mb-4">Abu Dhabi Ministry achieves 3x productivity gain</h3>
                            <div class="text-xs text-gray-300 uppercase tracking-wider">Employees: 5000+ <br/> Sector: Government</div>
                        </div>
                        <div class="font-bold text-xl">Abu Dhabi Government</div>
                    </div>
                </div>

                <!-- Card 2 -->
                <div class="aspect-[4/5] relative rounded-2xl overflow-hidden group cursor-pointer">
                    <div class="absolute inset-0 bg-gradient-to-br from-gray-900 to-primary-900">
                         <div class="absolute inset-0 opacity-50 bg-gradient-to-t from-black via-transparent to-transparent"></div>
                         <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1542744173-8e7e53415bb0?q=80&w=2070&auto=format&fit=crop')] bg-cover bg-center mix-blend-overlay opacity-30"></div>
                    </div>
                    <div class="absolute inset-0 p-8 flex flex-col justify-between text-white">
                        <div>
                            <h3 class="font-serif text-3xl leading-tight mb-4">Financial services firm reduces task time by 40%</h3>
                            <div class="text-xs text-gray-300 uppercase tracking-wider">Employees: 2500 <br/> Sector: Financial Services</div>
                        </div>
                        <div class="font-bold text-xl">MENA Finance Corp</div>
                    </div>
                </div>

                <!-- Card 3 -->
                <div class="aspect-[4/5] relative rounded-2xl overflow-hidden group cursor-pointer">
                    <div class="absolute inset-0 bg-gradient-to-br from-primary-900 to-gray-900">
                         <div class="absolute inset-0 opacity-50 bg-gradient-to-t from-black via-transparent to-transparent"></div>
                         <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?q=80&w=2070&auto=format&fit=crop')] bg-cover bg-center mix-blend-overlay opacity-30"></div>
                    </div>
                    <div class="absolute inset-0 p-8 flex flex-col justify-between text-white">
                        <div>
                            <h3 class="font-serif text-3xl leading-tight mb-4">Healthcare authority achieves 12x code productivity</h3>
                            <div class="text-xs text-gray-300 uppercase tracking-wider">Employees: 3500 <br/> Sector: Healthcare</div>
                        </div>
                        <div class="font-bold text-xl">Healthcare Authority</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Comparison Section -->
    <section class="py-24 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">The urgency is real. <br/> The choice is yours.</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    85 million jobs displaced by 2025. 97 million new roles requiring AI fluency. <br/> Those who delay risk irrelevance as competitors surge ahead.
                </p>
            </div>

            <div class="border-t border-gray-100">
                <div class="grid grid-cols-3 py-4 text-xs text-gray-400 uppercase tracking-wider border-b border-gray-100">
                    <div>Without AI Fluency</div>
                    <div class="text-center">→</div>
                    <div>With AI Fluency</div>
                </div>
                {#each comparisons as item}
                    <div class="grid grid-cols-1 md:grid-cols-[1fr_auto_1fr] gap-8 py-12 border-b border-gray-100 items-center group hover:bg-gray-50 transition-colors px-4 -mx-4 rounded-xl">
                        <div class="text-gray-500 leading-relaxed md:pr-8">
                            {item.left}
                        </div>
                        <div class="flex justify-center">
                            <span class="bg-primary-500 text-white text-[10px] font-bold tracking-wider px-2 py-1 rounded uppercase whitespace-nowrap">
                                {item.tag}
                            </span>
                        </div>
                        <div class="text-black font-medium leading-relaxed md:pl-8">
                            {item.right}
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Programs & Sectors Section -->
    <section class="py-24 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Sector-specific programs <br/> for every industry</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    From government ministries to private enterprises, we customize <br/> AI fluency training for your industry's unique workflows.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
                <!-- Target Sectors -->
                <div>
                    <div class="text-center mb-8">
                        <span class="bg-primary-500 text-white text-[10px] font-bold tracking-wider px-2 py-1 rounded uppercase">
                            TARGET SECTORS
                        </span>
                    </div>
                    <div class="grid grid-cols-3 gap-6">
                        {#each ['Government', 'Financial Services', 'Healthcare', 'Engineering', 'Construction', 'Technology', 'Education', 'Manufacturing', 'Consulting'] as sector}
                            <div class="aspect-square bg-gray-50 rounded-xl flex flex-col items-center justify-center p-4 hover:bg-primary-50 transition-colors border border-gray-100">
                                <div class="w-8 h-8 bg-primary-100 rounded-full mb-2"></div>
                                <span class="text-[11px] text-center text-gray-700 font-medium">{sector}</span>
                            </div>
                        {/each}
                    </div>
                </div>

                <!-- Training Components -->
                <div>
                    <div class="text-center mb-8">
                        <span class="bg-primary-500 text-white text-[10px] font-bold tracking-wider px-2 py-1 rounded uppercase">
                            TRAINING COMPONENTS
                        </span>
                    </div>
                    <div class="grid grid-cols-3 gap-6">
                         {#each ['Role-specific modules', 'Workflow integration', 'Hands-on practice', 'AI tool mastery', 'Productivity metrics', 'Certification paths', 'Community access', 'Continuous updates', 'Executive briefings'] as component}
                            <div class="aspect-square bg-gray-50 rounded-xl flex flex-col items-center justify-center p-2 hover:bg-primary-50 transition-colors border border-gray-100">
                                <div class="w-6 h-6 border-2 border-primary-300 rounded mb-2"></div>
                                <span class="text-[10px] text-center text-gray-700 font-medium leading-tight">{component}</span>
                            </div>
                        {/each}
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Mission Section -->
    <section class="py-24 px-6">
        <div class="max-w-[1400px] mx-auto grid grid-cols-1 lg:grid-cols-2 min-h-[600px]">
            <div class="bg-white relative flex items-center justify-center p-12 overflow-hidden">
                <div class="flex gap-4 transform -rotate-6 scale-90">
                    <div class="w-64 h-80 bg-primary-600 flex items-center justify-center text-white font-bold text-3xl shadow-2xl">NVIDIA Partnership</div>
                    <div class="w-64 h-80 bg-black flex items-center justify-center text-white font-bold text-3xl shadow-2xl z-10 -mt-12">OpenAI Practitioners</div>
                    <div class="w-64 h-80 bg-primary-500 flex items-center justify-center text-white font-bold text-3xl shadow-2xl">X.AI Partnership</div>
                </div>
            </div>
            <div class="bg-primary-950 p-12 lg:p-24 flex flex-col justify-center text-white">
                <p class="font-serif text-3xl md:text-4xl leading-tight mb-8">
                    Our mission: democratize AI capability for 4B+ humans in the Global South, ensuring no one loses economic value in the AI transformation.
                </p>
                <p class="font-serif text-3xl md:text-4xl leading-tight">
                    Starting with Abu Dhabi, we're positioning the region as the global leader in AI fluency. Our goal: every professional AI-capable within 3 years.
                </p>
            </div>
        </div>
    </section>

    <!-- Bottom CTA -->
    <section class="py-32 px-6 text-center bg-white">
        <div class="max-w-4xl mx-auto">
            <h2 class="font-serif text-6xl md:text-7xl mb-6">The AI revolution <br/> waits for no one.</h2>
            <p class="text-xl text-gray-600 mb-10">Position your workforce for the future. Start today.</p>
            <button class="bg-black text-white px-8 py-3 rounded-full text-base font-medium hover:bg-gray-800 transition-colors">
                Schedule Executive Briefing
            </button>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="py-24 px-6 bg-white border-t border-gray-100">
        <div class="max-w-[1400px] mx-auto">
            <h2 class="font-serif text-5xl mb-16">FAQ</h2>
            <div class="space-y-4">
                {#each faqs as faq}
                    <div class="border-b border-gray-100 py-6 flex justify-between items-center cursor-pointer group hover:bg-gray-50 px-4 -mx-4 rounded-lg transition-colors">
                        <span class="text-lg font-medium">{faq}</span>
                        <div class="w-8 h-8 rounded-full bg-black text-white flex items-center justify-center group-hover:bg-gray-800 transition-colors">
                            <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><line x1="12" y1="5" x2="12" y2="19"></line><line x1="5" y1="12" x2="19" y2="12"></line></svg>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-24 px-6 bg-white border-t border-gray-100">
        <div class="max-w-[1400px] mx-auto grid grid-cols-1 md:grid-cols-4 gap-12">
            <div class="col-span-1 md:col-span-1">
                <div class="flex items-center gap-2 mb-8">
                     <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-primary-600">
                        <path d="M12 2C12 2 8 6 8 12C8 18 12 22 12 22C12 22 16 18 16 12C16 6 12 2 12 2Z" fill="currentColor"/>
                        <path d="M2 12C2 12 6 8 12 8C18 8 22 12 22 12C22 12 18 16 12 16C6 16 2 12 2 12Z" fill="currentColor" opacity="0.6"/>
                    </svg>
                    <span class="font-medium text-xl tracking-tight">AI Fluency Company</span>
                </div>
                <div class="text-sm text-gray-500 mb-4">Join our newsletter</div>
                <div class="flex gap-2 border-b border-gray-200 pb-2 mb-8">
                    <input type="email" placeholder="Email address" class="w-full outline-none text-sm" />
                    <button class="text-gray-400 hover:text-black">→</button>
                </div>
                <div class="text-xs text-gray-400">© AI Fluency Company 2025</div>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-3 gap-8 col-span-1 md:col-span-3">
                <div>
                    <h4 class="text-xs font-bold text-gray-400 uppercase tracking-wider mb-6">Programs</h4>
                    <ul class="space-y-3 text-sm text-gray-600">
                        <li><a href="#" class="hover:text-black">Government Sector</a></li>
                        <li><a href="#" class="hover:text-black">Financial Services</a></li>
                        <li><a href="#" class="hover:text-black">Healthcare</a></li>
                        <li><a href="#" class="hover:text-black">Engineering</a></li>
                        <li><a href="#" class="hover:text-black">Construction</a></li>
                        <li><a href="#" class="hover:text-black">Technology</a></li>
                        <li><a href="#" class="hover:text-black">Education</a></li>
                        <li><a href="#" class="hover:text-black">Certification Paths</a></li>
                        <li><a href="#" class="hover:text-black">Custom Programs</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-xs font-bold text-gray-400 uppercase tracking-wider mb-6">Resources</h4>
                    <ul class="space-y-3 text-sm text-gray-600">
                        <li><a href="#" class="hover:text-black">Impact Stories</a></li>
                        <li><a href="#" class="hover:text-black">ROI Calculator</a></li>
                        <li><a href="#" class="hover:text-black">Research & Insights</a></li>
                        <li><a href="#" class="hover:text-black">Community Forum</a></li>
                        <li><a href="#" class="hover:text-black">Executive Briefings</a></li>
                        <li><a href="#" class="hover:text-black">Pilot Programs</a></li>
                        <li><a href="#" class="hover:text-black">FAQ</a></li>
                        <li><a href="#" class="hover:text-black">Contact</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-xs font-bold text-gray-400 uppercase tracking-wider mb-6">Company</h4>
                    <ul class="space-y-3 text-sm text-gray-600">
                        <li><a href="#" class="hover:text-black">Mission</a></li>
                        <li><a href="#" class="hover:text-black">Partnerships</a></li>
                        <li><a href="#" class="hover:text-black">NVIDIA Partnership</a></li>
                        <li><a href="#" class="hover:text-black">OpenAI Practitioners</a></li>
                        <li><a href="#" class="hover:text-black">Advisory Board</a></li>
                        <li><a href="#" class="hover:text-black">Press</a></li>
                        <li><a href="#" class="hover:text-black">Careers</a></li>
                        <li><a href="#" class="hover:text-black">Legal</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>

</div>

