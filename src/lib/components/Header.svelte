<div class="header-wrapper">
	<div class="header">
		<a class="logo" href="/">
			<b>DEEPAK</b> RAJAN
		</a>
		<div class="links">
			<a class="link" href="/projects"> projects </a>
			<a class="link" href="/projects"> gallery </a>
			<a class="link" href="/projects"> store </a>
			<a class="link" href="/projects"> blog </a>
			<a class="link" href="/projects"> profile </a>
		</div>
	</div>
</div>

<style lang="scss">
	a:hover {
		text-decoration: underline;
	}
	.header-wrapper {
		font-size: 20px;
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: var(--header-height);
		z-index: 100;
		display: flex;
		align-items: center;
		border: none;

		.header {
			width: 100%;
			height: 100%;
			box-sizing: border-box;
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding: 0 20px;
		}

		.links {
			display: flex;
			align-items: center;
			gap: 40px;
			font-size: 16px;
			// text-transform: uppercase;
			// font-weight: 600;

			.light {
				font-weight: 500;
			}
		}
	}
</style>
