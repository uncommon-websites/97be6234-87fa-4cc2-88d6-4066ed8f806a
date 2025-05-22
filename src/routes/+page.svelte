<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CustomerCardHero from "$lib/components/layout/hero-sections/CustomerCardHero.svelte";
</script>

<CustomerCardHero
  centered={false}
  title="Keep your best workers longer"
  subtitle="Reduce turnover with a benefit your teams actually use—matched savings goals built for essential workers."
  customers={[
    {
      name: "Maria Gonzalez",
      position: "Construction Site Manager",
      imageSrc: "/generated/image-a-female-construction-site-manager-weari.webp"
    },
    {
      name: "Tom Nguyen",
      position: "Manufacturing Plant Supervisor",
      imageSrc: "/generated/image-a-male-plant-supervisor-stands-confident.webp"
    },
    {
      name: "Rebecca Smith",
      position: "Restaurant General Manager",
      imageSrc: "/generated/image-a-female-restaurant-general-manager-stan.webp"
    },
    {
      name: "Carlos Hernandez",
      position: "Crew Lead",
      imageSrc: "/generated/image-a-male-crew-lead-in-a-construction-unifo.webp"
    },
    {
      name: "Priya Patel",
      position: "HR Director",
      imageSrc: "/generated/image-a-female-hr-director-in-business-attire-.webp"
    }
  ]}
/>
<LogoScroller
	label="Trusted by industry leaders"
	logoUrls={[
		"https://logo.clearbit.com/turnerconstruction.com",
		"https://logo.clearbit.com/bechtel.com",
		"https://logo.clearbit.com/honeywell.com",
		"https://logo.clearbit.com/mcdonalds.com"
	]}
/>

<Summary
	title="What we do"
	text="Tanda helps companies retain and engage essential workers with personalized benefits focused on financial wellness. Our platform makes it easy for your teams to set savings goals, earn employer matches, and feel truly valued at work."
/>

<Testimonials
	testimonials={[
		{
			name: "Eduardo Montes",
			position: "Site Manager, Mesa Ridge Construction",
			quote: "Tanda cut our admin time on incentives and bonuses. Now, I’m on-site with the crew—not buried in paperwork.",
			image: "/generated/image-a-male-construction-site-manager-in-a-sa.webp"
		},
		{
			name: "Mabel Choi",
			position: "HR Manager, Paragon Manufacturing",
			quote: "We used to stress every exit interview. With Tanda, retention’s up and scheduling headaches are down. The team actually feels heard.",
			image: "/generated/image-a-female-hr-manager-with-a-warm-smile-en.webp"
		},
		{
			name: "Tariq Ford",
			position: "Crew Lead, Urban Fork Diner",
			quote: "We spend less bringing in new hires. Peer bonuses keep the team happy, and regulars are seeing the same faces again.",
			image: "/generated/image-a-male-crew-lead-in-a-casual-uniform-pos.webp"
		}
	]}
/>

<Features
	title="What makes Tanda different"
	subtitle="Everything you need to keep essential workers loyal—and thriving."
	features={[
		{
			title: "Personalized matched savings",
			description: "Let employees choose meaningful savings goals—like certifications or emergencies—and match their progress to keep them motivated."
		},
		{
			title: "Peer and manager recognition",
			description: "Make great work visible with instant shout-outs and rewards straight from any device—no logins required."
		},
		{
			title: "Real-time pulse surveys",
			description: "Spot problems early with SMS-driven check-ins and feedback before issues spiral into turnover."
		},
		{
			title: "Data-driven retention insights",
			description: "Unlock actionable analytics on turnover, morale, and compensation so you can make smarter HR decisions."
		},
		{
			title: "Built for high-turnover industries",
			description: "Tailored for construction, manufacturing, and restaurants—no one-size-fits-all solutions here."
		},
		{
			title: "Enterprise impact, proven ROI",
			description: "Achieve up to 10x return over traditional benefits by minimizing churn and boosting engagement from day one."
		}
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world impact for every industry we serve"
	useCases={[
		{
			title: "Retain your best crews in construction",
			description: "Match savings on safety certifications, tools, and more. Reduce turnover by aligning employee goals to project milestones, keeping crews stable from bid to build.",
			image: "/generated/image-a-group-of-construction-workers-gathered.webp",
			link: {
				href: "/use-cases/construction-retention",
				label: "Learn more"
			}
		},
		{
			title: "Reduce manufacturing turnover where it matters most",
			description: "Personalized financial wellness tools and team engagement for plants. Retain skilled operators and cut costly first-90-day churn with real-time insights and matched savings.",
			image: "/generated/image-in-a-bustling-manufacturing-plant-a-dive.webp",
			link: {
				href: "/use-cases/manufacturing-engagement",
				label: "Learn more"
			}
		},
		{
			title: "Build restaurant loyalty with life goal benefits",
			description: "Help FOH and BOH staff save for what matters most. Combine flexible savings plans, manager recognition, and peer bonuses to keep your team strong and stable.",
			image: "/generated/image-restaurant-staff-gathered-in-a-cozy-and-.webp",
			link: {
				href: "/use-cases/restaurant-loyalty",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction
  title="Keep your crew. Cut the churn."
  subtitle="Retention starts before resignation."
  description="Tanda helps construction, manufacturing, and restaurant teams keep skilled workers with matched savings goals and real-time engagement insight. Give essential employees a benefit that matters—before they think about leaving."
  imageSrc="/generated/image-a-cheerful-construction-worker-wearing-a.webp"
  callsToAction={[
    { href: "/demo", label: "See it in action", variant: "primary" },
    { href: "/contact", label: "Talk to our team", variant: "secondary" }
  ]}
/>
