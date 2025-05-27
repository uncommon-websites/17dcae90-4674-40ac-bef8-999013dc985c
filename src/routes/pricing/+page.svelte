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
      name: "Darnell Watkins",
      position: "Owner",
      company: "Blue Skies HVAC",
      quote:
        "With Probook, we've cut dispatch time in half and boosted sales by 14% in just three months. It paid for itself within the first quarter. Can't imagine running my team without it.",
      image: "/generated/image-a-professional-headshot-of-a-black-male-.webp",
    },
    {
      name: "Marisa Gutierrez",
      position: "Lead Dispatcher",
      company: "Pipeline Pros Plumbing",
      quote:
        "Probook was up and running in days. Our new techs learned the board fast, and our call flips are up 17%. Makes my job (and day) so much easier!",
      image: "/generated/image-a-professional-headshot-of-a-latina-fema.webp",
    },
    {
      name: "Kenji Yamazaki",
      position: "Operations Manager",
      company: "WiredWorks Electric",
      quote:
        "We used to need three dispatchers for 30 techs. Now, one person can handle it when we're on Autopilot. The ROI is hard to beat, and everyone trusts the assignments.",
      image: "/generated/image-a-professional-headshot-of-an-east-asian.webp",
    },
  ]}
/>

<CallToAction
  title="Ready to take dispatch off your plate?"
  subtitle="Let AI handle dispatching so your team can handle the work."
  description="Start with a no-pressure demo and launch in days. Our CEO will fly out for your 2-day onboardingsupport, and we offer 24/7 on-call help in Teams, Slack, or whatever you use. Probook12% more sales, 19% more flips, real-time integration with ServiceTitan. See what relief feels like."
  imageSrc="/generated/image-a-happy-home-services-dispatcher-at-work.webp"
  callsToAction={[
    { href: '/book-demo', label: 'Book your demo', variant: 'primary' },
    { href: '/contact', label: 'Talk to us', variant: 'secondary' }
  ]}
/>
