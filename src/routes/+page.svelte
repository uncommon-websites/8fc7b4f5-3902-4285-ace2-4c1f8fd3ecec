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
            tag: "INFRASTRUCTURE",
            title: "NVIDIA compute access, not just video lectures",
            metric: "GPU",
            metricLabel: "Backed training",
            gradient: "from-primary-500 to-primary-600"
        },
        {
            tag: "PRACTITIONERS",
            title: "OpenAI team access, not outdated curricula",
            metric: "Live",
            metricLabel: "Frontier access",
            gradient: "from-gray-900 to-gray-800"
        },
        {
            tag: "WORKFLOW",
            title: "Embedded in operations, not theoretical knowledge",
            metric: "90d",
            metricLabel: "To deployment",
            gradient: "from-primary-600 to-primary-700"
        },
        {
            tag: "VALIDATED",
            title: "Government-deployed, not pilot-stage promises",
            metric: "5k+",
            metricLabel: "Gov employees",
            gradient: "from-gray-800 to-black"
        },
        {
            tag: "MEASURABLE",
            title: "3x output gains, not completion certificates",
            metric: "3x",
            metricLabel: "Proven results",
            gradient: "from-primary-500 to-primary-600"
        },
        {
            tag: "STRATEGIC",
            title: "Competitive defense, not professional development",
            metric: "Q1",
            metricLabel: "Cohort closing",
            gradient: "from-gray-900 to-gray-800"
        }
    ];

    const testimonials = [
        {
            quote: "AI Fluency Company transformed our workforce from AI-curious to AI-capable in months. The productivity gains are measurable and transformative.",
            name: "Dr. Ahmed Al-Mansoori",
            role: "Director of Digital Transformation, Government Ministry",
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
            role: "Head of Innovation, Regional Healthcare Authority",
            avatar: "MR"
        },
        {
            quote: "Every professional deserves AI fluency. This program ensures our workforce isn't left behind as AI reshapes every industry.",
            name: "Fatima Hassan",
            role: "Chief Human Resources Officer, Enterprise Technology",
            avatar: "FH"
        },
        {
            quote: "The 1000x leverage principle changed how we think about productivity. AI isn't replacing us—it's amplifying our capabilities exponentially.",
            name: "David Park",
            role: "Engineering Director, Global South Tech Hub",
            avatar: "DP"
        },
        {
            quote: "Those who delay risk irrelevance. AI Fluency Company gave us the competitive edge before market pressures forced reactive responses.",
            name: "Layla Abdullah",
            role: "CEO, Regional Technology Consulting",
            avatar: "LA"
        }
    ];

    const partnershipServices = [
        "NVIDIA GPU compute for hands-on training (not simulations)",
        "OpenAI practitioners teaching current techniques (not 2023 content)",
        "X.AI implementation insights (not generic best practices)",
        "!ntropy and Basis strategic advisory (not consultant theory)",
        "Government ministry deployment experience (not pilot promises)",
        "90-day capability building (not 6-month certification programs)",
        "Ongoing frontier access (not static course content)"
    ];

    const comparisons = [
        {
            tag: "MARKET POSITION",
            left: "Competitors deploying AI capability while you evaluate options",
            right: "Market leadership secured through early workforce transformation"
        },
        {
            tag: "PRODUCTIVITY",
            left: "Linear output growth constrained by headcount",
            right: "3x output multiplication without hiring (government-validated)"
        },
        {
            tag: "TALENT",
            left: "Top performers leaving for AI-capable organizations",
            right: "Retention through capability building, attraction through differentiation"
        },
        {
            tag: "COST STRUCTURE",
            left: "Rising labor costs to maintain current output levels",
            right: "6-month ROI through productivity gains (enterprise-proven)"
        },
        {
            tag: "STRATEGIC RISK",
            left: "Falling behind as AI reshapes industry economics",
            right: "Defensive positioning against competitive displacement"
        }
    ];

    const faqs = [
        "Why NVIDIA partnership matters for training outcomes",
        "How this differs from Coursera or Scale AI",
        "Typical ROI timeline for enterprise deployments",
        "90-day deployment methodology explained",
        "Government validation and case study access",
        "Sector-specific customization options",
        "Q1 2025 cohort availability and enrollment",
        "Workforce displacement vs. capability building",
        "Executive briefing format and calendar access"
    ];

</script>

<div class="font-sans text-gray-900 bg-white selection:bg-primary-200 selection:text-black">
    <!-- Navbar -->
    <nav class="sticky top-0 z-50 bg-white/90 backdrop-blur-xl border-b border-gray-100">
        <div class="max-w-[1400px] mx-auto px-6 h-20 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <!-- Logo Mark -->
                <svg width="28" height="28" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-primary-600">
                    <path d="M12 2C12 2 8 6 8 12C8 18 12 22 12 22C12 22 16 18 16 12C16 6 12 2 12 2Z" fill="currentColor"/>
                    <path d="M2 12C2 12 6 8 12 8C18 8 22 12 22 12C22 12 18 16 12 16C6 16 2 12 2 12Z" fill="currentColor" opacity="0.6"/>
                </svg>
                <span class="font-semibold text-xl tracking-tight">AI Fluency Company</span>
            </div>

            <div class="hidden md:flex items-center gap-10 text-sm font-medium text-gray-600">
                {#each navLinks as link}
                    <a href="#" class="hover:text-black transition-colors duration-200">{link}</a>
                {/each}
            </div>

            <button class="bg-black text-white px-6 py-2.5 rounded-full text-sm font-semibold hover:bg-gray-800 transition-all duration-300 hover:scale-105">
                Schedule Briefing
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative pt-32 pb-24 px-6 text-center overflow-hidden bg-gradient-to-b from-gray-50 to-white">
        <!-- Subtle background pattern -->
        <div class="absolute inset-0 opacity-[0.03]" style="background-image: radial-gradient(circle at 1px 1px, rgb(0 0 0) 1px, transparent 0); background-size: 40px 40px;"></div>
        
        <div class="relative max-w-5xl mx-auto mb-20">
            <!-- Urgency Badge -->
            <div class="inline-flex items-center gap-2 bg-black text-white rounded-full px-4 py-2 mb-8">
                <div class="w-2 h-2 rounded-full bg-primary-400 animate-pulse"></div>
                <span class="text-sm font-medium">Q1 2025 cohort closing — 47 seats remaining</span>
            </div>

            <h1 class="font-serif text-7xl md:text-8xl lg:text-[6rem] leading-[0.95] mb-8 font-normal tracking-tight">
                Your competitors are already <span class="text-primary-600">AI-capable.</span> Are you?
            </h1>
            <p class="text-xl md:text-2xl text-gray-600 max-w-3xl mx-auto mb-12 leading-relaxed font-light">
                Abu Dhabi government ministries deployed workforce AI fluency at scale. NVIDIA-backed training delivering 3x output gains in 90 days.
            </p>
            
            <div class="flex flex-col sm:flex-row items-center justify-center gap-4 mb-6">
                <button class="bg-black text-white px-10 py-4 rounded-full text-base font-medium hover:bg-gray-800 transition-all duration-300 hover:scale-105">
                    Get Executive Briefing
                </button>
            </div>
            <p class="text-sm text-gray-500">30-minute strategic assessment • No sales pitch • Calendar link provided instantly</p>
        </div>

        <!-- Hero Image - Single Clean Screenshot -->
        <div class="relative max-w-[1200px] mx-auto mt-20">
            <div class="relative rounded-2xl overflow-hidden border border-gray-200 bg-white p-2">
                <img src="/generated/image-modern-ai-training-platform-dashboard-on-1766011053537-0.webp" alt="AI Training Platform Dashboard" class="w-full rounded-xl" />
            </div>
            <!-- Floating accent elements -->
            <div class="absolute -top-4 -right-4 w-24 h-24 bg-primary-500 rounded-full opacity-10 blur-3xl"></div>
            <div class="absolute -bottom-4 -left-4 w-32 h-32 bg-gray-900 rounded-full opacity-5 blur-3xl"></div>
        </div>
    </section>

    <!-- Logos Section -->
    <section class="py-20 border-y border-gray-100 bg-white">
        <div class="max-w-[1400px] mx-auto px-6 text-center">
            <p class="text-xs uppercase tracking-widest text-gray-400 mb-12 font-bold">Infrastructure partnerships</p>
            <div class="flex flex-wrap justify-center items-center gap-16 md:gap-20 opacity-60 hover:opacity-100 transition-all duration-500">
                {#each logos as logo}
                    <div class="h-8 flex items-center justify-center">
                        <span class="font-bold text-2xl tracking-tight text-gray-900">{logo.name}</span>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Our Approach Grid -->
    <section class="py-32 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-24">
                <h2 class="font-serif text-6xl md:text-7xl mb-8 tracking-tight">Our approach</h2>
                <p class="text-xl text-gray-600 leading-relaxed">
                    Beyond generic online courses. Role-specific training with measurable productivity gains.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                {#each features as feature, i}
                    <div class="group relative bg-white border border-gray-200 rounded-3xl p-10 hover:border-gray-300 transition-all duration-500 hover:scale-[1.02]">
                        <!-- Gradient background on hover -->
                        <div class="absolute inset-0 bg-gradient-to-br {feature.gradient} opacity-0 group-hover:opacity-5 rounded-3xl transition-opacity duration-500"></div>
                        
                        <div class="relative">
                            <!-- Tag -->
                            <div class="inline-flex items-center gap-2 mb-6">
                                <div class="w-1.5 h-1.5 rounded-full bg-primary-500"></div>
                                <span class="text-xs font-bold tracking-widest text-gray-400 uppercase">
                                    {feature.tag}
                                </span>
                            </div>

                            <!-- Title -->
                            <h3 class="font-serif text-2xl leading-tight mb-12 text-gray-900">
                                {feature.title}
                            </h3>

                            <!-- Metric Display -->
                            <div class="mt-auto pt-8 border-t border-gray-100">
                                <div class="flex items-end justify-between">
                                    <div>
                                        <div class="text-4xl font-bold text-gray-900 mb-1">{feature.metric}</div>
                                        <div class="text-sm text-gray-500">{feature.metricLabel}</div>
                                    </div>
                                    <div class="w-12 h-12 rounded-full bg-gradient-to-br {feature.gradient} opacity-10 group-hover:opacity-20 transition-opacity duration-500"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Case Studies Section -->
    <section class="py-32 px-6 bg-gray-50">
        <div class="max-w-[1400px] mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-24">
                <h2 class="font-serif text-6xl md:text-7xl mb-8 tracking-tight">Deployed at scale</h2>
                <p class="text-xl text-gray-600 leading-relaxed">
                    Government-validated results. Enterprise-proven methodology.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Case Study 1 -->
                <div class="bg-white p-10 rounded-3xl border border-gray-200 hover:border-gray-300 transition-all duration-300">
                    <div class="mb-8">
                        <div class="text-5xl font-bold text-gray-900 mb-2">3x</div>
                        <div class="text-sm text-gray-500 uppercase tracking-wider">Output multiplication</div>
                    </div>
                    <div class="mb-6">
                        <div class="font-semibold text-gray-900 mb-1">Abu Dhabi Government Ministry</div>
                        <div class="text-sm text-gray-600">5,000+ employees • 90-day deployment</div>
                    </div>
                    <p class="text-gray-700 leading-relaxed">Policy analysis tasks reduced from 8 hours to 2.5 hours. Document processing automated with 94% accuracy.</p>
                </div>

                <!-- Case Study 2 -->
                <div class="bg-white p-10 rounded-3xl border border-gray-200 hover:border-gray-300 transition-all duration-300">
                    <div class="mb-8">
                        <div class="text-5xl font-bold text-gray-900 mb-2">40%</div>
                        <div class="text-sm text-gray-500 uppercase tracking-wider">Faster task completion</div>
                    </div>
                    <div class="mb-6">
                        <div class="font-semibold text-gray-900 mb-1">MENA Financial Services</div>
                        <div class="text-sm text-gray-600">2,500 employees • Q3 2024 cohort</div>
                    </div>
                    <p class="text-gray-700 leading-relaxed">Risk assessment workflows accelerated. Compliance reporting time cut by half. Zero displacement.</p>
                </div>

                <!-- Case Study 3 -->
                <div class="bg-white p-10 rounded-3xl border border-gray-200 hover:border-gray-300 transition-all duration-300">
                    <div class="mb-8">
                        <div class="text-5xl font-bold text-gray-900 mb-2">12x</div>
                        <div class="text-sm text-gray-500 uppercase tracking-wider">Code productivity</div>
                    </div>
                    <div class="mb-6">
                        <div class="font-semibold text-gray-900 mb-1">Regional Healthcare Authority</div>
                        <div class="text-sm text-gray-600">3,500 employees • Ongoing deployment</div>
                    </div>
                    <p class="text-gray-700 leading-relaxed">Development cycles shortened. Technical documentation automated. Engineering teams scaling output without headcount.</p>
                </div>

                <!-- Case Study 4 -->
                <div class="bg-white p-10 rounded-3xl border border-gray-200 hover:border-gray-300 transition-all duration-300">
                    <div class="mb-8">
                        <div class="text-5xl font-bold text-gray-900 mb-2">70%</div>
                        <div class="text-sm text-gray-500 uppercase tracking-wider">Time savings</div>
                    </div>
                    <div class="mb-6">
                        <div class="font-semibold text-gray-900 mb-1">Global South Tech Hub</div>
                        <div class="text-sm text-gray-600">1,200 employees • Pilot program</div>
                    </div>
                    <p class="text-gray-700 leading-relaxed">Administrative overhead eliminated. Meeting summaries automated. Knowledge workers refocused on strategic work.</p>
                </div>

                <!-- Case Study 5 -->
                <div class="bg-white p-10 rounded-3xl border border-gray-200 hover:border-gray-300 transition-all duration-300">
                    <div class="mb-8">
                        <div class="text-5xl font-bold text-gray-900 mb-2">85%</div>
                        <div class="text-sm text-gray-500 uppercase tracking-wider">Adoption rate</div>
                    </div>
                    <div class="mb-6">
                        <div class="font-semibold text-gray-900 mb-1">Regional Technology Consulting</div>
                        <div class="text-sm text-gray-600">800 employees • Q4 2024 cohort</div>
                    </div>
                    <p class="text-gray-700 leading-relaxed">Daily AI usage across all departments. Client deliverables quality increased. Competitive positioning strengthened.</p>
                </div>

                <!-- Case Study 6 -->
                <div class="bg-white p-10 rounded-3xl border border-gray-200 hover:border-gray-300 transition-all duration-300">
                    <div class="mb-8">
                        <div class="text-5xl font-bold text-gray-900 mb-2">6mo</div>
                        <div class="text-sm text-gray-500 uppercase tracking-wider">ROI timeline</div>
                    </div>
                    <div class="mb-6">
                        <div class="font-semibold text-gray-900 mb-1">Enterprise Technology Corp</div>
                        <div class="text-sm text-gray-600">4,200 employees • Full deployment</div>
                    </div>
                    <p class="text-gray-700 leading-relaxed">Training investment recovered in 6 months. Ongoing productivity gains compounding. Market leadership secured.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Partnership Section -->
    <section class="py-32 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-3xl mx-auto mb-24">
                <h2 class="font-serif text-6xl md:text-7xl mb-8 tracking-tight">Strategic partnerships with frontier AI leaders</h2>
                <p class="text-xl text-gray-600 leading-relaxed">
                    Learning from the cutting edge, not following outdated curricula.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
                <div class="bg-gradient-to-br from-gray-50 to-white border border-gray-100 p-16 rounded-3xl h-full">
                    <h3 class="font-serif text-3xl mb-12 text-gray-900">Partnership ecosystem</h3>
                    <ul class="space-y-6">
                        {#each partnershipServices as service}
                            <li class="flex items-start gap-4 group">
                                <div class="w-6 h-6 rounded-full bg-primary-500 flex items-center justify-center shrink-0 mt-0.5 group-hover:scale-110 transition-transform duration-300">
                                    <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg>
                                </div>
                                <span class="text-gray-700 text-lg leading-relaxed">{service}</span>
                            </li>
                        {/each}
                    </ul>
                </div>
                <div class="h-full min-h-[600px] rounded-3xl overflow-hidden relative border border-gray-100">
                    <div class="absolute inset-0 bg-gray-200">
                        <img src="/generated/image-professional-training-session-with-instr-1766010978458-1.webp" alt="Professional training session" class="w-full h-full object-cover" />
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Competitive Intelligence Section -->
    <section class="py-32 px-6 bg-gray-50">
        <div class="max-w-[1400px] mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-24">
                <h2 class="font-serif text-6xl md:text-7xl mb-8 tracking-tight">While you're reading this</h2>
                <p class="text-xl text-gray-600 leading-relaxed">
                    Your competitors are already deploying AI capability at scale.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-16">
                <!-- Stat 1 -->
                <div class="bg-white p-12 rounded-3xl border border-gray-200">
                    <div class="text-6xl font-bold text-gray-900 mb-4">15,000+</div>
                    <div class="text-lg text-gray-600 mb-2">Professionals already trained across MENA region</div>
                    <div class="text-sm text-gray-500">Government ministries, financial services, healthcare, technology sectors</div>
                </div>

                <!-- Stat 2 -->
                <div class="bg-white p-12 rounded-3xl border border-gray-200">
                    <div class="text-6xl font-bold text-gray-900 mb-4">Q1 2026</div>
                    <div class="text-lg text-gray-600 mb-2">Current cohort closing soon</div>
                    <div class="text-sm text-gray-500">Limited availability across government and enterprise tracks</div>
                </div>

                <!-- Stat 3 -->
                <div class="bg-white p-12 rounded-3xl border border-gray-200">
                    <div class="text-6xl font-bold text-gray-900 mb-4">90 days</div>
                    <div class="text-lg text-gray-600 mb-2">From enrollment to measurable capability</div>
                    <div class="text-sm text-gray-500">Not 6-month certification programs. Rapid deployment methodology.</div>
                </div>

                <!-- Stat 4 -->
                <div class="bg-white p-12 rounded-3xl border border-gray-200">
                    <div class="text-6xl font-bold text-gray-900 mb-4">6 months</div>
                    <div class="text-lg text-gray-600 mb-2">Average ROI timeline for enterprise deployments</div>
                    <div class="text-sm text-gray-500">Training investment recovered through productivity gains</div>
                </div>
            </div>

            <div class="bg-gradient-to-br from-gray-900 to-black p-16 rounded-3xl text-white text-center">
                <p class="text-2xl font-serif mb-6">
                    "Those who delay risk irrelevance as competitors surge ahead."
                </p>
                <p class="text-gray-400">— Market reality, not marketing hyperbole</p>
            </div>
        </div>
    </section>

    <!-- Comparison Section -->
    <section class="py-32 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-4xl mx-auto mb-24">
                <h2 class="font-serif text-6xl md:text-7xl mb-8 tracking-tight">The urgency is real</h2>
                <p class="text-xl text-gray-600 leading-relaxed">
                    85 million jobs displaced by 2025. 97 million new roles requiring AI fluency. Those who delay risk irrelevance.
                </p>
            </div>

            <div class="border-t-2 border-gray-100">
                <div class="grid grid-cols-3 py-6 text-xs text-gray-400 uppercase tracking-widest border-b border-gray-100 font-bold">
                    <div>Without AI Fluency</div>
                    <div class="text-center"></div>
                    <div>With AI Fluency</div>
                </div>
                {#each comparisons as item, i}
                    <div class="grid grid-cols-1 md:grid-cols-[1fr_auto_1fr] gap-12 py-16 border-b border-gray-100 items-center group hover:bg-gray-50 transition-all duration-300 px-8 -mx-8 rounded-2xl">
                        <div class="text-gray-500 leading-relaxed text-lg md:pr-8">
                            {item.left}
                        </div>
                        <div class="flex justify-center">
                            <div class="flex flex-col items-center gap-3">
                                <div class="w-12 h-12 rounded-full bg-gradient-to-br from-primary-500 to-primary-600 flex items-center justify-center text-white font-bold text-xl">
                                    →
                                </div>
                                <span class="text-[10px] font-bold tracking-widest text-gray-400 uppercase text-center max-w-[100px]">
                                    {item.tag}
                                </span>
                            </div>
                        </div>
                        <div class="text-gray-900 font-semibold leading-relaxed text-lg md:pl-8">
                            {item.right}
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Programs & Sectors Section -->
    <section class="py-32 px-6 bg-gray-50">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-4xl mx-auto mb-24">
                <h2 class="font-serif text-6xl md:text-7xl mb-8 tracking-tight">Programs built for your sector</h2>
                <p class="text-xl text-gray-600 leading-relaxed">
                    Role-specific training delivering measurable results across six strategic industries.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-20">
                <!-- Target Sectors -->
                <div>
                    <div class="mb-12">
                        <h3 class="text-xs font-bold tracking-widest text-gray-400 uppercase mb-2">Strategic Sectors</h3>
                        <div class="w-16 h-1 bg-primary-500 rounded-full"></div>
                    </div>
                    <div class="grid grid-cols-2 gap-6">
                        {#each ['Government', 'Financial Services', 'Healthcare', 'Engineering & Construction', 'Technology', 'Education'] as sector}
                            <div class="aspect-square bg-white rounded-2xl flex flex-col items-center justify-center p-8 hover:bg-primary-50 hover:scale-105 transition-all duration-300 border border-gray-100 hover:border-primary-200 cursor-pointer group">
                                <div class="w-12 h-12 bg-gradient-to-br from-primary-500 to-primary-600 rounded-full mb-4 group-hover:scale-110 transition-transform duration-300"></div>
                                <span class="text-sm text-center text-gray-700 font-semibold leading-tight">{sector}</span>
                            </div>
                        {/each}
                    </div>
                </div>

                <!-- Training Components -->
                <div>
                    <div class="mb-12">
                        <h3 class="text-xs font-bold tracking-widest text-gray-400 uppercase mb-2">Training Components</h3>
                        <div class="w-16 h-1 bg-gray-900 rounded-full"></div>
                    </div>
                    <div class="grid grid-cols-3 gap-4">
                         {#each ['Role-specific modules', 'Workflow integration', 'Hands-on practice', 'AI tool mastery', 'Productivity metrics', 'Certification paths', 'Community access', 'Continuous updates', 'Executive briefings'] as component}
                            <div class="aspect-square bg-white rounded-2xl flex flex-col items-center justify-center p-4 hover:bg-gray-50 hover:scale-105 transition-all duration-300 border border-gray-100 hover:border-gray-300 cursor-pointer group">
                                <div class="w-8 h-8 border-2 border-gray-900 rounded-lg mb-3 group-hover:bg-gray-900 transition-colors duration-300"></div>
                                <span class="text-[11px] text-center text-gray-700 font-semibold leading-tight">{component}</span>
                            </div>
                        {/each}
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Mission Section -->
    <section class="py-32 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
            <div class="bg-gradient-to-br from-gray-900 to-black rounded-3xl overflow-hidden border border-gray-800">
                <div class="grid grid-cols-1 lg:grid-cols-2 min-h-[700px]">
                    <div class="relative flex items-center justify-center p-16 overflow-hidden bg-gradient-to-br from-primary-600/10 to-transparent">
                        <div class="flex gap-6 transform -rotate-6 scale-90">
                            <div class="w-56 h-72 bg-gradient-to-br from-primary-500 to-primary-600 rounded-2xl flex items-center justify-center text-white font-bold text-2xl p-8 text-center border border-primary-400">NVIDIA Partnership</div>
                            <div class="w-56 h-72 bg-gradient-to-br from-gray-800 to-gray-900 rounded-2xl flex items-center justify-center text-white font-bold text-2xl p-8 text-center z-10 -mt-12 border border-gray-700">OpenAI Practitioners</div>
                            <div class="w-56 h-72 bg-gradient-to-br from-primary-600 to-primary-700 rounded-2xl flex items-center justify-center text-white font-bold text-2xl p-8 text-center border border-primary-500">X.AI Partnership</div>
                        </div>
                    </div>
                    <div class="p-16 lg:p-20 flex flex-col justify-center text-white">
                        <div class="mb-8">
                            <div class="inline-block bg-white/10 backdrop-blur-sm rounded-full px-4 py-2 mb-6">
                                <span class="text-xs font-bold uppercase tracking-wider">Beyond MENA</span>
                            </div>
                        </div>
                        <p class="font-serif text-4xl md:text-5xl leading-tight mb-10">
                            Preventing economic displacement through capability building.
                        </p>
                        <p class="text-xl text-white/80 leading-relaxed">
                            Starting with UAE government deployment. Scaling across MENA and Global South markets. Target: every professional AI-capable within 3 years.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Bottom CTA -->
    <section class="py-40 px-6 text-center bg-gradient-to-b from-white to-gray-50">
        <div class="max-w-5xl mx-auto">
            <!-- Urgency indicator -->
            <div class="inline-flex items-center gap-3 bg-black text-white rounded-full px-6 py-3 mb-10">
                <div class="w-2.5 h-2.5 rounded-full bg-red-400 animate-pulse"></div>
                <span class="text-sm font-medium">Q1 2025 cohort closes March 15 — 47 seats remaining</span>
            </div>
            
            <h2 class="font-serif text-7xl md:text-8xl mb-10 tracking-tight leading-[0.95]">Don't let competitors outpace you</h2>
            <p class="text-2xl text-gray-600 mb-14 font-light">30-minute executive briefing. No sales pitch. Calendar link provided instantly.</p>
            <div class="flex flex-col sm:flex-row items-center justify-center gap-4 mb-8">
                <button class="bg-black text-white px-12 py-5 rounded-full text-lg font-medium hover:bg-gray-800 transition-all duration-300 hover:scale-105">
                    Get Executive Briefing
                </button>
            </div>
            <p class="text-sm text-gray-500">Join 15,000+ professionals already deployed across government and enterprise</p>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="py-32 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
            <div class="mb-20">
                <h2 class="font-serif text-6xl md:text-7xl mb-4 tracking-tight">Frequently asked questions</h2>
                <p class="text-xl text-gray-600">Everything you need to know about AI fluency training.</p>
            </div>
            <div class="space-y-2">
                {#each faqs as faq}
                    <div class="border border-gray-100 py-8 px-8 flex justify-between items-center cursor-pointer group hover:border-gray-300 hover:bg-gray-50 rounded-2xl transition-all duration-300">
                        <span class="text-lg font-medium text-gray-900 group-hover:text-black pr-8">{faq}</span>
                        <div class="w-10 h-10 rounded-full bg-black text-white flex items-center justify-center group-hover:bg-gray-800 group-hover:scale-110 transition-all duration-300 shrink-0">
                            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><line x1="12" y1="5" x2="12" y2="19"></line><line x1="5" y1="12" x2="19" y2="12"></line></svg>
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

