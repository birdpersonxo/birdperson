<script lang="ts">
	import { Projects } from '$lib/components';
</script>

<div class="hero">
	<div class="banner">
		<img src="/k2.png" alt="hero" />
	</div>
	<div class="projects">
		<Projects />
	</div>
</div>

<style>
	.hero {
		position: relative;
		height: calc(200vh - (var(--header-height) * 2));
	}

	.banner {
		position: sticky;
		top: 0;
		height: calc(100vh - var(--header-height));
		box-sizing: border-box; /* padding no longer adds to the total height */
		z-index: 1;
		overflow: hidden;
		padding: 16px;
		padding-top: 0px;
	}
	.banner img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		display: block;
	}

	.projects {
		position: relative;
		height: calc(100vh - var(--header-height));
		z-index: 2;
		background-color: var(--bg-color);
	}
</style>
