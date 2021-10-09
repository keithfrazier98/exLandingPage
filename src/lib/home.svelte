<script>
	let autumn = '/autumn.jpg';
	let cosmos = '/cosmos.png';
	let dinner = '/dinner.png';
	let fisherman = '/fisherman.jpg';
	let hand = '/hand.jpg';
	let heart = '/heart.jpg';
	let plants = '/plants.jpg';
	let trees = '/trees.jpg';
	let wreath = '/wreath.jpg';
	import { fade } from 'svelte/transition';

</script>

<div>
	<img in:fade={{ duration: 1500 }} src={autumn} width="25%" alt="autumn" />
	<img in:fade={{ delay: 1000, duration: 1500 }} src={cosmos} width="25%" alt="cosmos" />
	<img in:fade={{ delay: 500, duration: 1500 }} src={dinner} width="25%" alt="dinner" />
	<img in:fade={{ delay: 2000, duration: 1500 }} src={fisherman} width="25%" alt="fisherman" />
	<img in:fade={{ delay: 1500, duration: 1500 }} src={hand} width="25%" alt="hand" />
	<img in:fade={{ delay: 500, duration: 1500 }} src={heart} width="25%" alt="heart" />
	<img in:fade={{ delay: 2500, duration: 1500 }} src={plants} width="25%" alt="plants" />
	<img in:fade={{ delay: 1000, duration: 1500 }} src={trees} width="25%" alt="trees" />
	<img in:fade={{ delay: 1500, duration: 1500 }} src={wreath} width="25%" alt="wreath" />
</div>

<style>
	img {
		margin: 20px;
		box-shadow: 10px 10px 100px rgb(56, 56, 56);
	}

	img:hover{
		transform: scale(1.1);
		transition: transform .2s
	}
	div {
		justify-content: center;
		display: flex;
		flex-wrap: wrap;
		width: 100vw;
	}
</style>
