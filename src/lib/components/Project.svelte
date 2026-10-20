<script lang="ts">
	import { type ProjectBanner } from './types';
	let { img, href, heading, content }: ProjectBanner = $props();
</script>

<a class="project" {href}>
	<div class="img">
		<img src={img} alt="hero" />
	</div>
	<div class="heading">
		<!-- <div class="main">2D Global Illumination in COPs</div>
		<div class="sub">
			After learning more about real-time lighting techniques, I wanted to tackle 2D Screen-Space
			Global Illumination (GI).
		</div> -->
		<div class="main">{heading}</div>
		<div class="sub">
			{content}
		</div>
	</div>
</a>

<style lang="scss">
	.project {
		flex: 1;
		min-width: 0;
		transition: 1ms;

		.img {
			width: 100%;
			aspect-ratio: 16 / 7;

			img {
				width: 100%;
				height: 100%;
				object-fit: cover;
			}
		}

		.heading {
			.main {
				font-size: 22px;
				font-weight: 500;
				padding: 6px;
			}
		}

		&:hover {
			.main {
				color: #888;
			}
		}
	}
</style>
