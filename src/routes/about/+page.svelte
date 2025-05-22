<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Innovation",
			description: "Constantly challenging the status quo to create better solutions."
		},
		{
			title: "Integrity",
			description: "Building trust through transparent actions and honest communication."
		},
		{
			title: "Impact",
			description: "Measuring our success by the positive change we create for our clients."
		}
	];
</script>

<SecondaryHero
	title="Keep your best workers longer"
	subtitle="Matched savings and engagement tools that reduce turnover"
	imageSrc="/mockups/airport-screen-1747939575702.png"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"Tanda started with a simple question: why are essential jobs so hard to retain, even when the work is steady and the need is constant? Jesse Chor, Chris Chan, Mike Emery, and Glen Wong had spent years building products at companies like Expedia, Yahoo, and Splunk — but came back to a deeper challenge they all felt strongly about: how to help the people doing the hardest work feel invested, valued, and financially stable. In 2023, they founded Tanda to do just that.",
		"The idea grew from something familiar: community-based savings. Many of their own families had relied on matched savings or hand-rolled support systems to get through uncertainty or plan for the future. Tanda takes that familiar system and brings it to the workplace — giving essential workers a better way to save for goals like certifications, tools, or emergencies, while helping employers directly contribute. It’s built for workers on the floor, in the field, or behind the line — not behind a desk.",
		"For companies in construction, manufacturing, and restaurants, hiring is hard and turnover is harder. Tanda helps teams stay consistent by meeting employees where it really matters: reducing stress from day one and offering benefits people actually use. Along the way, we've earned early support from investors like Sequoia and Initialized — and with every deployment, we're proving that frontline teams don’t need more forms or flyers. They need real tools built around real life, designed for retention that works."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Meet our founders."
  subtitle="Leaders committed to helping frontline workers thrive."
  stakeholders={[
    {
      name: "Jesse Chor",
      position: "Founder & CEO",
      bio: "Jesse led teams at Expedia before starting Tanda, where he’s passionate about building solutions for essential workers.",
      image: "/generated/image-a-professional-male-founder-captured-in-.webp"
    },
    {
      name: "Chris Chan",
      position: "Co-Founder, Product",
      bio: "Chris specializes in product strategy, ensuring Tanda meets the real needs of companies and workers alike.",
      image: "/generated/image-a-professional-asian-male-founder-depict.webp"
    },
    {
      name: "Mike Emery",
      position: "Co-Founder, Engineering",
      bio: "Mike is an expert in building resilient, scalable technology to power programs frontline teams depend on.",
      image: "/generated/image-a-professional-caucasian-male-founder-sh.webp"
    },
    {
      name: "Glen Wong",
      position: "Co-Founder, Engineering",
      bio: "Glen brings engineering leadership from Yahoo and Splunk, focused on empowering essential employees.",
      image: "/generated/image-a-professional-asian-male-founder-wearin.webp"
    }
  ]}
/>

<StakeholderGrid
  stakeholderType="investor"
  title="Backed by world-class investors."
  subtitle="Sequoia and Initialized support Tanda's mission to transform retention for essential industries."
  stakeholders={[
    {
      name: "Sequoia",
      image: "https://cdn.brandfetch.io/sequoiacap.com/w/400/h/400/logo"
    },
    {
      name: "Initialized",
      image: "https://cdn.brandfetch.io/initialized.com/w/400/h/400/logo"
    }
  ]}
/>

<!-- CTA Section -->
<CallToAction
	title="Ready to collaborate?"
	subtitle="Let's create something amazing"
	description="Join the companies already leveraging our expertise to transform their digital presence and achieve their business goals."
/>
