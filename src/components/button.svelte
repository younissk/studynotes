<script>
	export let src = '';
	export let name = 'test';
	export let color = 'FBD283';
	export let path = '/Web_Development';
</script>

<a href="/{path}">
	<div class="button" style="background-color: #{color};">
		{#if src !== ''}
			<img {src} alt={name} class="icon" />
		{/if}
		<h3>{name}</h3>
	</div>
</a>

<style>
	a {
		font-family: 'ubuntu', sans-serif;
		text-decoration: none;
		color: black;
		font-weight: bolder;
	}

	.button {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-evenly;
		margin: 0px 10px 10px 0px;
		padding: 15px 0px;
		border-radius: 15px;
	}

	h3 {
		margin: 0px;
		padding: 0px;
		font-size: 16px;
	}

	img {
		width: 10%;
	}
</style>
