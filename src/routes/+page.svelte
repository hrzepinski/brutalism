<script>
	import '../app.css';
	import Button from '../lib/components/Button/Button.svelte';
</script>

<svg style="width: 100%; height: 100%; position: absolute; z-index: -1;">
	<filter id="roughpaper" x="0%" y="0%" width="100%" height="100%">
		<feTurbulence type="fractalNoise" baseFrequency="0.3" result="noise" numOctaves="2" />

		<feDiffuseLighting in="noise" lighting-color="white" surfaceScale="2">
			<feDistantLight azimuth="20" elevation="90" />
		</feDiffuseLighting>
	</filter>

	<rect x="0" y="0" width="100%" height="100%" filter="url(#roughpaper)" fill="none" /></svg
>
<div class="container mx-auto gradient-body">
	<h1 class="text-3xl font-bold underline">Welcome to SvelteKit</h1>
	<Button class="shadow-md " kind="tertiary">Button</Button>
</div>

<style>
</style>
