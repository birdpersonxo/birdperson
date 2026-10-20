<script lang="ts"></script>

<div class="header">
	<div class="header-img">
		<img src="/k1.png" />
	</div>
	<div class="header-title-wrapper">
		<div class="top">
			<div class="header-title">
				<div>dGroom</div>
				<div><b>Deformer 2.0</b></div>
			</div>
			<div class="header-content">
				This dGroom Deformer tool allows you to easily deform grooms with generated or existing
				guides, making your workflow smoother and more efficient. 16 hda's. Features: Guide
				Generation , Level of detail and Style Blending
			</div>
		</div>
		<div class="bottom">
			<button class="button">Purchase</button>
			<button class="button">Documentation</button>
		</div>
	</div>
</div>

<div class="body">Studio Customer</div>

<style lang="scss">
	.header-title-wrapper {
		display: flex;
		flex-direction: column;
		height: 100%;
	}

	.header-content {
		width: 500px;
	}

	.bottom {
		margin-top: auto;
		display: flex;
		gap: 10px;
		width: 100%;
	}

	.button {
		width: 100%;
		border: none;
		background-color: #000;
		padding: 10px;
		border-radius: 2px;
		color: #fff;
		font-size: 20px;
		cursor: pointer;
	}
	.body {
		padding: 20px;
	}
	.header {
		width: 100%;
		display: grid;
		grid-template-columns: 1.4fr 1fr;
		gap: 20px;

		.header-img {
			width: 100%;
			height: 420px;
			img {
				width: 100%;
				height: 100%;
				object-fit: cover;
			}
		}

		.header-title {
			width: 100%;
			font-size: 80px;
		}
	}
</style>
