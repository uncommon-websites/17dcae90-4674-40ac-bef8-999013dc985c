<!--
@component Pricing

Please update features according to the company's product offering. Do not remove this comment.
-->
<script lang="ts">
	// Types
	type PricingTier = {
		name: string;
		monthlyPrice?: number | null;
		yearlyPrice?: number | null;
		description: string;
		features: string[];
		cta: {
			label: string;
			href: string;
		};
		highlight?: boolean;
	};

	type PricingFeature = {
		name: string;
		tiers: {
			[key: string]: boolean | string;
		};
	};

	// Components
	import Button from "$lib/components/ui/Button.svelte";
	import SectionHeader from "./SectionHeader.svelte";
	import IconCheck from "~icons/lucide/check";
	import IconX from "~icons/lucide/x";
	import NumberFlow from "@number-flow/svelte";
	import LogoScroller from "./LogoScroller.svelte";

	// Props
	const {
		title = "Straightforward pricing, built for growth",
		subtitle = "Choose the level of automation that fits your dispatch operation",
		tierNames = ["Copilot", "Autopilot", "Enterprise"],
		features = [
		{
			name: "Level of automation",
			tiers: {
				Copilot: "AI recommends, dispatcher decides",
				Autopilot: "Fully automated, dispatcher supervises",
				Enterprise: "Custom workflow automations"
			}
		},
		{
			name: "ServiceTitan integration",
			tiers: {
				Copilot: true,
				Autopilot: true,
				Enterprise: true
			}
		},
		{
			name: "Tech-to-dispatcher ratio",
			tiers: {
				Copilot: "9:1",
				Autopilot: "20:1",
				Enterprise: "Custom"
			}
		},
		{
			name: "Board reshuffling",
			tiers: {
				Copilot: "Manual, with AI suggestions",
				Autopilot: "Automatic, real-time",
				Enterprise: "Custom triggers and automations"
			}
		},
		{
			name: "Performance dashboard",
			tiers: {
				Copilot: true,
				Autopilot: true,
				Enterprise: "Advanced analytics"
			}
		},
		{
			name: "Onboarding & launch",
			tiers: {
				Copilot: "2-day in-person with CEO",
				Autopilot: "2-day in-person, tailored for large teams",
				Enterprise: "Multi-location onboarding"
			}
		},
		{
			name: "Ongoing support",
			tiers: {
				Copilot: "24/7 chat, 1-min median response",
				Autopilot: "Priority routing, live check-ins",
				Enterprise: "Dedicated CSM, priority escalation"
			}
		},
		{
			name: "Custom integrations",
			tiers: {
				Copilot: false,
				Autopilot: false,
				Enterprise: true
			}
		},

			{
				name: "Level of automation",
				tiers: {
					Copilot: "AI recommends, dispatcher decides",
					Autopilot: "Fully automated, dispatcher supervises",
					Enterprise: "Custom workflow automations"
				}
			},
			{
				name: "ServiceTitan integration",
				tiers: {
					Copilot: true,
					Autopilot: true,
					Enterprise: true
				}
			},
			{
				name: "Tech-to-dispatcher ratio",
				tiers: {
					Copilot: "9:1",
					Autopilot: "20:1",
					Enterprise: "Custom"
				}
			},
			{
				name: "Board reshuffling",
				tiers: {
					Copilot: "Manual, with AI suggestions",
					Autopilot: "Automatic, real-time",
					Enterprise: "Custom triggers and automations"
				}
			},
			{
				name: "Performance dashboard",
				tiers: {
					Copilot: true,
					Autopilot: true,
					Enterprise: "Advanced analytics"
				}
			},
			{
				name: "Onboarding & launch",
				tiers: {
					Copilot: "2-day in-person with CEO",
					Autopilot: "2-day in-person, tailored for large teams",
					Enterprise: "Multi-location onboarding"
				}
			},
			{
				name: "Ongoing support",
				tiers: {
					Copilot: "24/7 chat, 1-min median response",
					Autopilot: "Priority routing, live check-ins",
					Enterprise: "Dedicated CSM, priority escalation"
				}
			},
			{
				name: "Custom integrations",
				tiers: {
					Copilot: false,
					Autopilot: false,
					Enterprise: true
				}
			}
		],
		tiers = [
		{
			name: "Copilot",
			monthlyPrice: 399,
			yearlyPrice: 349, // 15% savings billed annually
			description: "AI-powered dispatch recommendations. Your team stays in control.",
			features: [
				"Smart AI technician-job pairing",
				"One-click send from ServiceTitan",
				"7-day technician review dashboard",
				"Manual board with data-backed suggestions",
				"24/7 on-call & chat support",
				"2-day launch onsite with our CEO"
			],
			cta: {
				label: "Book Copilot demo",
				href: "/demo?plan=copilot"
			}
		},
		{
			name: "Autopilot",
			monthlyPrice: 699,
			yearlyPrice: 599, // ~15% savings billed annually
			description: "Fully automated AI dispatch. Scale your techs, not your dispatch team.",
			features: [
				"Full board automation & live reshuffling",
				"1 dispatcher for 20–25+ techs",
				"Real-time ServiceTitan integration",
				"Performance & coverage optimization",
				"Priority support and twice-weekly check-ins",
				"Onsite launch tailored for high-volume teams"
			],
			cta: {
				label: "Book Autopilot demo",
				href: "/demo?plan=autopilot"
			},
			highlight: true
		},
		{
			name: "Enterprise",
			monthlyPrice: null,
			yearlyPrice: null,
			description: "For operations with advanced needs: multi-location, custom integrations, or industry scale.",
			features: [
				"Everything in Autopilot",
				"Custom integrations & workflow automations",
				"Dedicated CSM & executive review",
				"Multi-location rollout",
				"Advanced analytics & reporting"
			],
			cta: {
				label: "Contact sales",
				href: "/contact"
			}
		},

			{
				name: "Copilot",
				monthlyPrice: 399,
				yearlyPrice: 349, // 15% savings billed annually
				description: "AI-powered dispatch recommendations. Your team stays in control.",
				features: [
					"Smart AI technician-job pairing",
					"One-click send from ServiceTitan",
					"7-day technician review dashboard",
					"Manual board with data-backed suggestions",
					"24/7 on-call & chat support",
					"2-day launch onsite with our CEO"
				],
				cta: {
					label: "Book Copilot demo",
					href: "/demo?plan=copilot"
				}
			},
			{
				name: "Autopilot",
				monthlyPrice: 699,
				yearlyPrice: 599, // ~15% savings billed annually
				description: "Fully automated AI dispatch. Scale your techs, not your dispatch team.",
				features: [
					"Full board automation & live reshuffling",
					"1 dispatcher for 20–25+ techs",
					"Real-time ServiceTitan integration",
					"Performance & coverage optimization",
					"Priority support and twice-weekly check-ins",
					"Onsite launch tailored for high-volume teams"
				],
				cta: {
					label: "Book Autopilot demo",
					href: "/demo?plan=autopilot"
				},
				highlight: true
			},
			{
				name: "Enterprise",
				monthlyPrice: null,
				yearlyPrice: null,
				description: "For operations with advanced needs: multi-location, custom integrations, or industry scale.",
				features: [
					"Everything in Autopilot",
					"Custom integrations & workflow automations",
					"Dedicated CSM & executive review",
					"Multi-location rollout",
					"Advanced analytics & reporting"
				],
				cta: {
					label: "Contact sales",
					href: "/contact"
				}
			}
		]
	}: {
		title?: string;
		subtitle?: string;
		tiers?: PricingTier[];
		features?: PricingFeature[];
		tierNames?: string[];
		caption?: string;
	} = $props();

	// State
	let annual = $state(true);
</script>

<section class="section-py section-px container mx-auto">
	<div class="flex flex-col items-baseline justify-between lg:flex-row">
		<SectionHeader {title} {subtitle} />

		<div class="mb-8 flex justify-center">
			<div class="inline-flex items-center rounded-full bg-gray-100 p-0.5 dark:bg-gray-800">
				<Button
					variant="ghost"
					size="sm"
					class=" {!annual ? 'bg-white shadow-sm dark:bg-gray-700' : ''}"
					onclick={() => (annual = false)}
				>
					Monthly
				</Button>
				<Button
					variant="ghost"
					size="sm"
					rounded
					class={annual ? "bg-white shadow-sm dark:bg-gray-700" : ""}
					onclick={() => (annual = true)}
				>
					Annual <span class="text-primary-600 dark:text-primary-400 text-footnote">Save 20%</span>
				</Button>
			</div>
		</div>
	</div>

	<div class="bb grid gap-6 md:grid-cols-2 lg:grid-cols-3">
		{#each tiers as tier}
			<div
				class="flex flex-col rounded-xl bg-white p-6 ring ring-gray-200 transition-all duration-300 dark:bg-gray-800 dark:ring-gray-700"
				class:ring-2={tier.highlight}
				class:ring-primary={tier.highlight}
				class:dark:ring-primary-700={tier.highlight}
				class:translate-y-[-4px]={tier.highlight}
			>
				<div class="mb-8">
					<h3 class="text-title3 mb-4 dark:text-white">{tier.name}</h3>
					<div class="mt-2 flex items-baseline">
						{#if tier.monthlyPrice === null && tier.yearlyPrice === null}
							<span class="text-title2 dark:text-white">Custom</span>
						{:else}
							<NumberFlow
								class="text-title2 [&::part\(suffix\)]:text-caption dark:text-white"
								format={{
									style: "currency",
									currency: "USD",
									trailingZeroDisplay: "stripIfInteger"
								}}
								value={annual ? tier.yearlyPrice : tier.monthlyPrice}
								suffix="/month"
							/>
						{/if}
					</div>
					<p class="text-callout text-emphasis-medium mt-3 dark:text-gray-300">
						{tier.description}
					</p>
				</div>

				<div class="mb-8 flex-grow">
					<ul class="space-y-3">
						{#each tier.features as feature}
							<li class="flex items-center gap-2">
								<IconCheck class="text-primary-600 dark:text-primary-400 size-5 flex-shrink-0" />
								<span class="text-body text-emphasis-medium dark:text-gray-300">{feature}</span>
							</li>
						{/each}
					</ul>
				</div>

				<div class="mt-auto">
					<Button
						href={tier.cta.href}
						variant={tier.highlight ? "primary" : "secondary"}
						class="w-full"
					>
						{tier.cta.label}
					</Button>
				</div>
			</div>
		{/each}
	</div>
	<div class="mt-32">
		<!-- Responsive table wrapper with horizontal scroll on mobile -->
		<!-- <div class=" hidden overflow-x-auto px-4 sm:mx-0 sm:block sm:px-0">
			<table
				class="w-full min-w-full border-separate border-spacing-0 border-gray-200 text-left dark:border-gray-700"
			>
				<thead>
					<tr>
						<th
							class="sticky left-0 min-w-[120px] border-b border-gray-200 bg-white dark:border-gray-700 dark:bg-gray-900"
						>
							<span class="sr-only">Feature</span>
						</th>
						{#each tierNames as tierName}
							<th
								class="text-headline min-w-[100px] border-b border-gray-200 p-4 text-start font-normal dark:border-gray-700"
							>
								{tierName}
							</th>
						{/each}
					</tr>
				</thead>
				<tbody>
					{#each features as feature}
						<tr>
							<td class="text-caption">
								{feature.name}
							</td>
							{#each tierNames as tierName}
								<td
									class="min-w-[100px] border-b border-gray-200 p-4 text-start text-gray-600 dark:border-gray-700 dark:text-gray-300"
								>
									{#if typeof feature.tiers[tierName] === "boolean"}
										{#if feature.tiers[tierName]}
											<IconCheck
												class="text-primary-600 dark:text-primary-400 mx-auto size-5 sm:mx-0"
											/>
										{:else}
											<IconX class="mx-auto size-5 text-gray-400 sm:mx-0" />
										{/if}
									{:else}
										{feature.tiers[tierName]}
									{/if}
								</td>
							{/each}
						</tr>
					{/each}
				</tbody>
			</table>
		</div> -->

		<!-- Mobile feature comparison (alternative view for very small screens) -->
		<div>
			<!-- Universal pricing comparison for mobile -->
			<div class="overflow-x-auto">
				<table class="w-full border-collapse">
					<!-- Sticky header with tier names -->
					<thead class="border-border sticky top-0 z-10 border-b">
						<tr>
							<th class="min-w-[120px] py-3 text-left">
								<span class="sr-only">Feature</span>
							</th>
							{#each tierNames as tierName, i}
								<th class="text-caption min-w-[100px] py-3 text-left dark:text-white">
									{tierName}
								</th>
							{/each}
						</tr>
					</thead>
					<tbody class="divide-border divide-y">
						{#each features as feature}
							<tr>
								<td class="text-body py-3 pr-8 font-medium lg:pr-0 dark:text-white">
									{feature.name}
								</td>
								{#each tierNames as tierName, i}
									<td class="py-3">
										{#if typeof feature.tiers[tierName] === "boolean"}
											{#if feature.tiers[tierName]}
												<IconCheck class="text-primary-900 dark:text-primary-400 size-5" />
											{:else}
												<IconX class="size-5 text-gray-400" />
											{/if}
										{:else}
											<span class="text-callout font-medium text-gray-700 dark:text-gray-300">
												{feature.tiers[tierName]}
											</span>
										{/if}
									</td>
								{/each}
							</tr>
						{/each}
					</tbody>
				</table>
			</div>
		</div>
	</div>
	<LogoScroller />
</section>

<style lang="postcss">
	@reference '../../../app.css';

	:global(number-flow-svelte)::part(suffix) {
		@apply text-sm text-gray-400 dark:text-gray-500;
	}
</style>
