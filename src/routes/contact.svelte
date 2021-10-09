<script>
	import Header from '$lib/Header.svelte';
    import {fly} from 'svelte/transition'
    import Footer from '$lib/Footer.svelte'

</script>

<Header />
<div in:fly={{ y: +200, duration:1500 }}>
	<div>
		<form>
			<label for="name"> Full Name </label>
			<input name="name" type="text" placeholder="" />
			<label for="email"> Email </label>
			<input name="email" type="email" placeholder="" />
			<label for="message"> Message </label>
			<textarea type="text" rows="10" />
            <button>Send!</button>
		</form>
	</div>
</div>
<Footer/>
<style>
	div > div{
		display: flex;
		flex-direction: row;
        background-image: url("../static/cosmos.png");
		border-radius: 20px;
		justify-content: center;
		height: fit-content;
		width: 40%;
		padding: 20px;
	}
    button{
        height: 40px;
        border: none;
        color: white;
        background-color: black;
        border-radius: 5px;
        margin-top: 10px;
        background-image: url("../static/autumn.jpg");
    }

    div{
        display: flex;
        flex-direction: row;
        justify-content: center;
        padding: 20px;
        height: 60vh;
    }
	form {
        color:white;
		display: flex;
		flex-direction: column;
		width: 90%;
		height: 60%;
        align-self: center;

	}

	:global(body) {
		padding: 0;
		margin: 0;
		background-color: black;
	}
</style>
