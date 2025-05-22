<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
  {
    title: "Real impact, fast",
    description: "Solve real-world problems for the teams that keep the world running—construction, manufacturing, and restaurants.",
    icon: IconBriefcase,
  },
  {
    title: "Work with world-class founders",
    description: "Join leaders from Expedia, Yahoo, and Splunk and build for scale, backed by Sequoia and Initialized.",
    icon: IconUsers,
  },
  {
    title: "High trust, high agency",
    description: "Make decisions that move the business. Shape our early direction with lots of ownership and growth.",
    icon: IconHeart,
  },
];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Maria Gutierrez",
    position: "Operations Associate",
    company: "Construction Team",
    quote:
      "From my first week, everyone made me feel welcome and supported. My manager checked in often, and mentors helped me grow quickly. It’s a place where everyone has your back.",
    image:
      "/generated/image-a-hispanic-woman-dressed-in-construction.webp"
  },
  {
    name: "Darius Carter",
    position: "Engineering Manager",
    company: "Product & Technology",
    quote:
      "At Tanda, mentorship and growth go hand-in-hand with bold projects. Leadership truly listens and invests in your development, pushing you to reach your full potential.",
    image:
      "/generated/image-a-black-man-wearing-a-smart-casual-outfi.webp"
  },
  {
    name: "Vivian Liu",
    position: "Head of People",
    company: "People Operations",
    quote:
      "There’s a spirit of inclusion here you can feel every day. I’ve never worked anywhere that cares so deeply about making an impact for employees and the customers we serve.",
    image:
      "/generated/image-an-east-asian-woman-dressed-in-business-.webp"
  }
];

	const processSteps = [
  {
    step: 1,
    title: "Submit your application",
    description: "Apply online—each application is reviewed by our team.",
  },
  {
    step: 2,
    title: "Intro call",
    description: "Quick chat with a team member to get to know each other.",
  },
  {
    step: 3,
    title: "Skills interview",
    description: "A hands-on challenge or role-specific interview so you can show your strengths.",
  },
  {
    step: 4,
    title: "Meet the founders",
    description: "Talk with Jesse or a co-founder to align on fit and impact.",
  },
  {
    step: 5,
    title: "Offer & feedback",
    description: "References and a decision, usually within a week. We'll keep you updated the whole time—no ghosting.",
  },
];

	const values = [
  {
    icon: IconHeart,
    title: "No ego, just impact",
    description: "We focus on making essential jobs better—what matters is the result, not your title.",
  },
  {
    icon: IconUsers,
    title: "Clear is kind",
    description: "We value direct feedback, honesty, and transparency. Simplicity makes us stronger.",
  },
  {
    icon: IconGlobe,
    title: "Frontline voices matter",
    description: "We listen to people closest to the work and build together—from every background and experience.",
  },
];
</script>

<!-- Hero Section -->

<SecondaryHero
  title="Personalized care for essential workers"
  subtitle="Join a team where impact meets purpose. Experience a culture built on camaraderie, support, and meaningful work that helps companies and their people thrive."
  imageSrc="/generated/image-a-diverse-group-of-people-are-working-to.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
