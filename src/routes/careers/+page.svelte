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
    title: "Founder-led onboarding",
    description: "Get 2-day in-person training directly from our CEO. We're hands-on from day one, and you connect with the heart of Probook early.",
    icon: IconBriefcase
  },
  {
    title: "Direct impact, daily growth",
    description: "See your work drive revenue, efficiency, and customer success for real companies. Grow your skills with real customers and a team that cares.",
    icon: IconUsers
  },
  {
    title: "Support at startup speed",
    description: "Twice-weekly check-ins, 24/7 direct access to founders, and a culture that solves problems quickly. You’re never on your own here.",
    icon: IconHeart
  }
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
    name: "Alicia Thompson",
    position: "Software Engineer",
    company: "Engineering",
    quote:
      "At Probook, I feel empowered to bring my ideas to life within a team that truly cares. The honest feedback, real mentorship, and everyday collaboration make it feel like I’m building something meaningful—and growing every day.",
    image: "/generated/image-a-black-female-engineer-smiling-with-con.webp"
  },
  {
    name: "Ravi Patel",
    position: "Customer Experience Specialist",
    company: "Support",
    quote:
      "Joining Probook’s support team opened doors I never expected. We openly share wins and challenges, and leadership trusts us to suggest improvements. Everyone's voice counts here, no matter your role.",
    image: "/generated/image-a-south-asian-male-customer-support-repr.webp"
  },
  {
    name: "Susan Lawrence",
    position: "VP of Operations",
    company: "Leadership",
    quote:
      "I've worked in larger companies, but nothing compares to the transparency and energy here. You’re encouraged to try new things, fail fast, and get right back up. The environment is ambitious but kind—we lift each other up every day.",
    image: "/generated/image-a-white-senior-woman-in-a-leadership-rol.webp"
  }
];

	const processSteps = [
  {
    step: 1,
    title: "Apply online",
    description: "Send us your resume and a few sentences on why you want to join Probook."
  },
  {
    step: 2,
    title: "Intro call",
    description: "We'll reach out within 3-5 days for a brief conversation about your background and what you're looking for."
  },
  {
    step: 3,
    title: "Skills discussion",
    description: "Meet the team to discuss a real scenario or problem in your discipline—collaborative and practical."
  },
  {
    step: 4,
    title: "Final chat & offer",
    description: "Wrap up with the CEO or team lead, review the details, and get clear next steps. Expect a decision in as little as a week."
  }
];

	const values = [
  {
    icon: IconHeart,
    title: "Customer-obsessed",
    description: "Every decision starts with the needs of our dispatchers and techs. We build with them—not just for them."
  },
  {
    icon: IconUsers,
    title: "Move fast, stay real",
    description: "We bias to action, try new things, and always own the outcome. Honest feedback and humility guide every step."
  },
  {
    icon: IconGlobe,
    title: "Hands-on at every level",
    description: "From CEO onboarding to high-frequency support, everyone’s connected and involved. No ivory towers here."
  }
];
</script>

<!-- Hero Section -->

<SecondaryHero
	title="Rebuilding home services with smarter tools"
	subtitle="Join a team using AI to make real-world impact"
	imageSrc="/generated/image-a-diverse-group-of-people-collaborating-.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Shape the future of home services technology, grow alongside founders, and make a visible impact every day." />

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
