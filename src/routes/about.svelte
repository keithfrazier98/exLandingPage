<script>
	import Header from '$lib/Header.svelte';
</script>

<Header />
<div>
	<div>
		<h3>About Me</h3>
		<p>
			Hello! Im John Doe and Im a super geek. Catch me on a saturday evening deep in a book about
			dragons and elves, or creating my latest design. I love drawing, painting, art in general.
			Pair that with my infatuation with computers and you get "John Doe: Graphic Designer
			Extraordinaire". I was born like this, what can I say? I sleep all night and I geek all day.
			Reach out and we can talk, collab, conspire, argue over sci-fi, or just play video games.
		</p>
	</div>
</div>

<style>
	div {
		width: 100%;
		display: flex;
		flex-direction: column;
	}
	h3 {
        font-size:50px;
        color:white;
		align-self: center;
        font-family: "Gemunu Libre", sans-serif;

	}

	div > div {
		width: 70%;
		align-self: center;
	}

	p {
        color:white;
		font-family: 'Gemunu Libre', sans-serif;
	}

    :global(body){
        background-color:black
    }
</style>
