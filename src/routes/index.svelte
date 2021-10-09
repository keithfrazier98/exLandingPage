<script context="module">
	export const prerender = true;
	import App from './app.svelte';
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<section>
	<App />
</section>

<style>
	:global(body) {
		padding: 0;
		margin: 0;
		background-color: black;
	}
</style>
