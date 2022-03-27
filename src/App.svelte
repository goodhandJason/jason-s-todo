<script>
	import Todo from './Todo.svelte'
</script>

<main>
	<h1>Jason's To-do App!</h1>
	<Todo />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		background-image: url("/img/background_pattern.png");
		/* background-color: #4EF4A8; */
		width: 60%;
		border: #EEBA0B 1.2rem solid;			
		border-radius: 1.2rem;
	}
	h1 {
		color: #5889d1;
		text-transform: uppercase;		
		font-size: 4em;		
		font-weight: 900;
		-webkit-text-stroke: 3px black;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>