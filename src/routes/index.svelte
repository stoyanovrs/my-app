<script context="module">
	export const prerender = true;
</script>

<script>
	import Counter from '$lib/Counter.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<div class="welcome">
		<picture>
			<source srcset="/images/image-hero-mobile.webp" type="image/webp" />
			<img src="/images/image-hero-mobile.png" alt="Welcome" />
		</picture>
	</div>
	<div class="headline">
		<h1>Make remote work</h1>
		<p>Get your team in sync, no matter your location. Streamline processes, create team rituals, and watch productivity soar.</p>
		<button>Learn more</button>
	</div>
</section>

<style lang="scss">
	
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
		
		.welcome {
		position: relative;
		width: 100%;
		height: auto;
		padding: 0 0 1rem 0;
		}

		.welcome img {
			width: 100%;
			height: 100%;
			display: block;
		}
		.headline {
			display: flex;
			flex: 1;
			justify-content: center;
			align-items: center;
			flex-direction: column;
			p {
			text-align: center;
			margin: 0 0.5rem 2rem 0;
			font-size: 20px;
			font-weight: 500;
			}
		}
	}

	

	
</style>
