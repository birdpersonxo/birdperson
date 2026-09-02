<script lang="ts">
    import "../lib/styles/main.scss";
    import "../lib/styles/font.css";

	import favicon from '$lib/assets/favicon.svg';
	import {Header} from "../lib/components";

	let { children } = $props();
	let contentEl: HTMLElement;

	// in your +layout or root component's onMount
	import Lenis from 'lenis';
	import { onMount } from "svelte";

	onMount(() => {
		const lenis = new Lenis({
			wrapper: contentEl,
			duration: 0.8,
		});

		function raf(time: number) {
			lenis.raf(time);
			requestAnimationFrame(raf);
		}
		requestAnimationFrame(raf);

		return () => lenis.destroy();
	});
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="main-wrapper">
   	<main class="content" bind:this={contentEl}>
        <Header/>
		{@render children()}
	</main>
</div>

<style lang="scss">
	:global(a) {
		text-decoration: none;
		color: var(--text-color);
	}

	:global(body),
	:global(html) {
		margin: 0;
		padding: 0;
		width: 100%;
		height: 100%;
		overflow: hidden;
		font-family: 'Neue Montreal', sans-serif;
		font-family: 'PP Mori', sans-serif;
		font-family:
			'PP Mori', ui-sans-serif, system-ui, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
			'Segoe UI Symbol', 'Noto Color Emoji';
		font-size: 14px;
		background-color: var(--bg-color);
		color: var(--text-color);
	}

	.content {
		margin-top: var(--header-height);
		height: calc(100vh - var(--header-height));
		overflow-y: auto;
		scroll-snap-type: y mandatory;
		scroll-behavior: smooth; /* see note below */
	}

</style>
