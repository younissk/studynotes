<script>
	import { getCollectionIndex, subjects, collectionIntro } from '../fb';
	import Styledbutton from '../components/button.svelte';
	let pathsArray = window.location.pathname.split('/').filter((el) => el != '');

	getCollectionIndex(pathsArray[0]);

	function getRandomColor() {
		var letters = '0123456789ABCDEF';
		var color = '';
		for (var i = 0; i < 6; i++) {
			color += letters[Math.floor(Math.random() * 16)];
		}
		return color;
	}
</script>

<main>
	<h1>{pathsArray[0].replace('_', ' ')}</h1>

	<p>
		{$collectionIntro}
	</p>

	<div class="buttons">
		{#each $subjects as subject}
			<Styledbutton
				path={pathsArray[0] + '/' + subject.name}
				color={getRandomColor()}
				name={subject.name}
				src={subject.icon}
			/>
		{/each}
	</div>
</main>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@300&display=swap');
	h1 {
		color: #f02d35;
	}

	p {
		font-weight: bolder;
		width: 70vw;
	}

	* {
		font-family: 'ubuntu', sans-serif;
		letter-spacing: 0.3vw;
	}
	main {
		margin: 50px;
	}

	.buttons {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
		margin: 20px 0px;
	}
</style>
