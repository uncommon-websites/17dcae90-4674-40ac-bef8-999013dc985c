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
  centered={true}
  title="Dispatching that works for real teams"
  subtitle="Probook helps home service companies get more jobs sold, reduce dispatcher workload, and assign the right tech every time—no constant babysitting required."
  customers={[
    {
      name: "Jamie, Dispatcher at TR Miller Heating & Cooling",
      position: "Dispatcher",
      imageSrc: "/generated/image-a-smiling-woman-dispatcher-in-a-modern-h.webp",
      testimonial: "We’re doing more jobs per day with fewer calls back and less hassle. It just lines up the day right."
    },
    {
      name: "Chris, Service Manager at Auchinachie Plumbing • Heating • Air",
      position: "Service Manager",
      imageSrc: "/generated/image-a-male-service-technician-in-a-plumbing-.webp",
      testimonial: "Probook freed up my dispatcher to manage twice the number of techs. It’s doing the thinking for you."
    },
    {
      name: "Beth, Owner at Lion Home Service",
      position: "Owner",
      imageSrc: "/generated/image-a-friendly-woman-dispatcher-in-an-electr.webp",
      testimonial: "Our average ticket is up, and our team actually trusts the board now. That’s the difference."
    },
    {
      name: "Eric, Ops Lead at Blake Brothers Plumbing & Electric",
      position: "Ops Lead",
      imageSrc: "/generated/image-a-male-hvac-service-manager-in-an-operat.webp",
      testimonial: "Once we hit Autopilot, our board just worked. We went from 10 to 20 techs on one dispatcher, no sweat."
    },
    {
      name: "Natalie, Operations Manager at True Service Pros",
      position: "Operations Manager",
      imageSrc: "/generated/image-a-female-operations-manager-in-a-home-se.webp",
      testimonial: "Probook made our dispatching process effortless and let us grow without adding more staff."
    },
  ]}
/>

<LogoScroller
	label="Trusted by industry leaders"
	logoUrls={[
		'https://logo.clearbit.com/ars.com',
		'https://logo.clearbit.com/rotorooter.com',
		'https://logo.clearbit.com/benfranklinplumbing.com',
		'https://logo.clearbit.com/mistersparky.com'
	]}
/>

<Summary
	title="What we do"
	text="Probook uses AI to assign the best technician to every job, making dispatching easy for home services companies. Companies boost sales, manage more techs with fewer dispatchers, and deliver better customer service—with less guesswork."
/>

<Testimonials
	testimonials={[
		{
			name: "Russell DeLaughter",
			position: "General Manager",
			company: "TR Miller Heating & Cooling",
			quote: "Probook gave our dispatchers clarity. There’s no more arguing over jobs—and revenue’s up. We’re saving hours every week from fewer callbacks and less board chaos.",
			image: "/generated/image-a-male-hvac-general-manager-in-a-bustlin.webp"
		},
		{
			name: "Samantha Daly",
			position: "Operations Director",
			company: "Lion Home Service",
			quote: "We saw an instant flip in sales. Risk of missed jobs is way down, and Probook makes decisions faster—and better—than a human can. No more gambling with our schedule.",
			image: "/generated/image-a-female-operations-director-in-a-vibran.webp"
		},
		{
			name: "Carlos Nguyen",
			position: "Dispatch Lead",
			company: "Auchinachie Plumbing • Heating • Air",
			quote: "I rely on Probook every single day. It’s like adding another dispatcher to my team—without the overhead. We scaled from managing 10 to 20+ techs per dispatcher and cut overtime costs by a third.",
			image: "/generated/image-a-male-dispatch-lead-at-a-busy-hvac-disp.webp"
		}
	]}
/>

<Features
	title="The features that matter"
	subtitle="Smarter dispatch, measurable results, real support."
	features={[
	  {
	    title: "AI-powered dispatching",
	    description: "Assigns the best tech to every call, boosting sales and customer trust."
	  },
	  {
	    title: "Autopilot and Copilot modes",
	    description: "Let AI run the board or get instant, data-backed recommendations—your team stays in control."
	  },
	  {
	    title: "Real-time ServiceTitan integration",
	    description: "Keeps schedules, jobs, and job details in perfect sync—no double entry or lag."
	  },
	  {
	    title: "Hands-on launch and support",
	    description: "CEO flies out for 2-day onboarding, with 24/7 live support and weekly coaching."
	  },
	  {
	    title: "Proven performance gains",
	    description: "Average increases: 12% in sales, 19% in flips, 20:1 tech-dispatcher ratio."
	  },
	  {
	    title: "Built for dispatchers, by dispatchers",
	    description: "Trusted by top home services companies—easy to use, transparent, and dispatcher-approved."
	  },
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world applications for your business needs"
	useCases={[
		{
			title: "Maximize revenue on every call",
			description:
				"Probook analyzes past jobs and tech performance to ensure the right technician is sent for every job—boosting ticket size, flip rate, and close percentage.",
			image: "/generated/image-a-cheerful-dispatcher-in-a-contemporary-.webp",
			link: {
				href: "/use-cases/maximize-revenue",
				label: "Learn more"
			}
		},
		{
			title: "Scale dispatch without new hires",
			description:
				"One dispatcher can now manage up to 20 or more technicians—no extra staff, just smarter assignments and fewer headaches.",
			image: "/generated/image-technicians-engaged-in-a-spirited-discus.webp",
			link: {
				href: "/use-cases/scale-dispatch",
				label: "Learn more"
			}
		},
		{
			title: "Shorten drive time, wow customers",
			description:
				"Reduce wasted miles by pairing techs with nearby jobs—so customers get faster arrival and better service, every time.",
			image: "/generated/image-a-service-van-parked-in-front-of-a-subur.webp",
			link: {
				href: "/use-cases/customer-satisfaction",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction
  title="Ready to optimize your dispatch?"
  subtitle="Talk to real experts—fast setup, ongoing support"
  description="Book a demo to see how Probook can help your home service team boost revenue, reduce dispatcher workload, and deliver a smoother operation. Enjoy personal onboarding with our CEO, 24/7 support, and real results from day one."
  imageSrc="/generated/image-a-cheerful-hvac-technician-and-a-dispatc.webp"
  callsToAction={[
    {
      href: "/demo",
      label: "Book your demo",
      variant: "primary"
    },
    {
      href: "/contact",
      label: "Talk to our team",
      variant: "secondary"
    }
  ]}
/>
