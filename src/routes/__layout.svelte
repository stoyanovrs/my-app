<script>
	import Header from '$lib/header/Header.svelte';
	import Footer from '$lib/footer/Footer.svelte';
	import '../lib/app.scss';
</script>

<Header />

<main>
	<slot />
</main>

<Footer />
	

<style>
	
</style>
