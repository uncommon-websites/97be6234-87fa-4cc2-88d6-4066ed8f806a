<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "Olivia Parrish",
      position: "HR Director",
      company: "BuildSouth Construction",
      quote:
        "Retention improved by 28% in six months. Tanda costs far less than hiring replacements, and our team likes it way more than another generic perk.",
      image:
        "/generated/image-a-professional-headshot-of-a-black-woman.webp"
    },
    {
      name: "Leo Nguyen",
      position: "Plant Manager",
      company: "Fulton Manufacturing",
      quote:
        "I was nervous about adding a new system, but our supervisors rolled it out in one day. In two weeks, 70% of team members were already saving. Zero friction.",
      image:
        "/generated/image-a-professional-headshot-of-a-southeast-a.webp"
    },
    {
      name: "Carla Estevez",
      position: "General Manager",
      company: "Yellow Lantern Diner",
      quote:
        "Since using the peer recognition tools, the energy on the floor has completely changed. Staff satisfaction scores are up, and people actually want to pick up more shifts.",
      image:
        "/generated/image-a-professional-headshot-of-a-hispanic-wo.webp"
    }
  ]}
/>

<CallToAction
  title="Retention starts with real impact"
  subtitle="Show your team that their goals matter"
  description="Tanda helps you engage and retain essential workers with personalized savings goals and financial wellness benefits—proven to reduce turnover and increase loyalty. See why companies like yours are already lowering churn and boosting loyalty with benefits workers actually use."
  imageSrc="/generated/image-a-happy-essential-worker-in-a-constructi.webp"
  callsToAction={[{
    href: "/demo",
    label: "Book your demo",
    variant: "primary"
  }]}
/>
