<script>
	import Header from '$lib/Header.svelte';
	import { slide } from 'svelte/transition';
	import Footer from '$lib/Footer.svelte'
	let more = false;
	let evenMore = false

	const setMore = (e)=>{
		more = true
	}

	const setEvenMore =()=>{
		evenMore = true
	}
</script>

<Header />
<div>
	<div>
		<h3>About Me</h3>
		<p in:slide={{ y: +200, duration: 1000 }}>
			Hello! I'm John Doe and I'm a super geek. Catch me on a Saturday evening deep in a book about
			dragons and elves, or creating my latest design. I love drawing, painting, art in general.
			Pair that with my infatuation with computers and you get "John Doe: Graphic Designer
			Extraordinaire". I was born like this, what can I say? I sleep all night and I geek all day.
			Reach out and we can talk, collab, conspire, argue over sci-fi, or just play video games.
		</p>
		<button on:click={setMore}>Tell Me More</button>
		{#if more}
		<p in:slide={{ y: +200, duration: 1000 }}>
			Oh, you want to know more? Well then, I love to cook. My favorite meal to cook is fried
			gnocchi with a delicious basil pesto alfredo sauce with just a HINT of lemon. Add some sauteed shrimp on
			top, with garlic bread on the side and you have the perfect meal. Oh, don't forget the wine!
			But enough about food, what about sports? Well, I don't like sports much, as I said, I'm a
			computer geek! We can play video games all day though, start with some Valorant, head over to
			Escape from Tarkov, and finish up with some Apex Legends. If you want to get crazy we can play
			some Split Gate.
		</p>
		<button on:click={setEvenMore}>For some reason I want to know more...</button>
		{/if}
		{#if evenMore}
		<p in:slide={{ y: +200, duration: 1000 }}>
			Really, do you have nothing better to do than listen to me ramble? Well, I can talk some more,
			lets talk about how awesome Svelte is. These transitions are amazing, implemented with like 4
			lines of code. And can we talk about the size? Svelte compiles your code into vanilla
			JavaScript, so there is no boilerplate framework bundled with your code. All this results in a
			smaller application than with any other framework. AMAZING.
		</p>
		{/if}

	</div>
</div>
<Footer/>
<style>
	div {
		width: 100%;
		display: flex;
		flex-direction: column;
		height: 60vh;
	}
	h3 {
		font-size: 50px;
		color: white;
		align-self: center;
		font-family: 'Gemunu Libre', sans-serif;
		text-shadow: -5px -5px 50px rgb(247, 119, 119);
	}

	div > div {
		width: 70%;
		align-self: center;
	}

	p {
		color: white;
		font-family: 'Gemunu Libre', sans-serif;
	}

	button{
		width: fit-content;
		height: 40px;
		background-image: url("/autumn.jpg");
		align-self: center;
		border: none;
		border-radius: 5px;
		color: rgb(130, 219, 145);
		text-shadow: 5px 5px 5px black;
		box-shadow: -5px 5px 50px rgb(255, 104, 104);
	}

	:global(body) {
		padding: 0;
		margin: 0;
		background-color: black;
	}
</style>
