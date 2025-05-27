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
    title: "Real-world impact",
    description: "Every decision supports the people doing the work—technicians, dispatchers, and customers."
  },
  {
    title: "We show up when it matters",
    description: "Our CEO is on-site for every onboarding, and we stay close with hands-on, human support."
  },
  {
    title: "Listen first, then build",
    description: "We shape our product and service by listening to dispatchers and technicians, not the tech press."
  },
  {
    title: "Outcomes, not hype",
    description: "We measure success in sales booked, flips closed, and dispatcher stress reduced—not buzzwords."
  },
  {
    title: "Teamwork & humility",
    description: "We share wins and challenges, learn daily, and know the best ideas often come from the field."  
  }
];
</script>

<SecondaryHero
	title="AI dispatching for home services"
	subtitle="Smarter routes. Higher sales. Happier customers."
	imageSrc="/generated/image-a-team-collaborating-in-a-modern-office-.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"George Eliadis was working closely with home service businesses when he saw the same mess in dispatch over and over—boards redlined, calls being assigned by gut feel, overloaded dispatchers making dozens of tradeoffs a day, and lost revenue from pairing the wrong tech with the wrong call. George had a simple idea: what if there was a way to do it better? Not just faster scheduling, but smarter dispatching—using GPS, skill sets, drive time, job type, and close rates to send the right tech every time. That idea became Probook.",
		"We started with one goal: take the stress off dispatchers and the missed money off the table. And from day one, it's been about trust—because even the smartest system only works if dispatchers use it. When you launch with Probook, our CEO shows up in person and dives in with your team. We don’t expect blind trust—we earn it. Dispatchers keep control, and with either Copilot or Autopilot running, their board stays lean and smart. And after launch, we stay close, with 24/7 support and regular check-ins with a real human you already know.",
		"We're not just building tech—we're building dispatch that works for the field, the office, and the bottom line. Our mission’s always been simple: less stress, more sales, better service. Probook is built for the real humans in your office—not just the IT team. And that mission won't change."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
	stakeholderType="team"
	title="Our founder."
	subtitle="Hands-on leadership, every step of the way."
	stakeholders={[
	  {
		name: "George Eliadis",
		position: "CEO & Founder",
		bio: "George Eliadis built Probook in 2024 to bring AI-powered dispatching to home services. He personally supports every launch, working hands-on with dispatcher teams in person to drive real results from day one.",
		image: "/generated/image-a-professional-headshot-of-a-male-founde.webp"
	  }
	]}
/>




<!-- CTA Section -->
<CallToAction
  title="Start dispatching like the top teams"
  subtitle="See your board with Probook in action"
  description="Meet with us for a quick walkthrough. Our CEO will help you launch in person—then you get 24/7 support, twice-weekly meetings, and proven results in sales, flips, and dispatcher efficiency. Book a demo and make every job the right job."
  callsToAction={[
    { href: "/book-demo", label: "Book a demo", variant: "primary" },
    { href: "/contact", label: "Talk to George", variant: "secondary" }
  ]}
  imageSrc="/uploaded/dispatch-smiling-team-huddle.webp"
/>
