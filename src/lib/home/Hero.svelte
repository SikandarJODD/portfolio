<script>
	import { ExternalLinkIcon, Linkedin } from 'lucide-svelte';
	import Button from './../components/ui/button/Button.svelte';
	import SmallBoxAlert from './SmallBoxAlert.svelte';
</script>

<div class="hero md:h-[90vh] md:bg-base-200">
	<div class="hero-content flex-col lg:flex-row">
		<img
			src="https://i.pinimg.com/564x/cd/b6/e1/cdb6e1bced383827aca51f6e4fee41cd.jpg"
			class="md:max-w-sm rounded-lg shadow-2xl"
			alt="Sikandar.S.Bhide"
		/>
		<div class="lg:pl-16 md:flex md:flex-col md:items-start">
			<SmallBoxAlert />
			<h1 class="text-5xl font-bold">SvelteKit Developer</h1>
			<div class="py-6 max-w-2xl prose">
				<p class="prose-a:underline-offset-2">
					I am Pursing B.E in Computer at <a href="https://pvppcoe.ac.in" target="_blank">VPPCOE</a
					>. I Love Books Related to Mythology, Hindu Gods and Goddesses.
					<a href="/">Sudha Murthy</a>
					is my favourite author of all times. <i> --- Jai Shri Ram</i>
				</p>
			</div>
			<div class="gap-2 flex">
				<Button
					href="https://github.com/SikandarJODD"
					target="_blank"
					variant="outline"
					class="border-slate-600 border hover:bg-zinc-200"
					>Github <ExternalLinkIcon size="15" class="ml-2" /></Button
				>
				<Button
					href="https://www.linkedin.com/in/sikandar-bhide/"
					variant="outline"
					class="border-slate-600 border hover:bg-zinc-200"
					target="_blank"
				>
					LinkedIn <ExternalLinkIcon size="15" class="ml-2" />
				</Button>
			</div>
		</div>
	</div>
</div>
