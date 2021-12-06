<script>
	import {createEventDispatcher} from 'svelte'

	let player = {
		name: '',
		points: 0
	};

		const dispatch = createEventDispatcher();

	const onSubmit = () => {
		dispatch('addPlayer', player);
			player = {
			name: '',
			points: 0
		};
	};
</script>

<form on:submit|preventDefault={onSubmit} class="grid-3">
	<input type="text" placeholder="Player Name" bind:value={player.name} />
	<input type="number" placeholder="Player Points" bind:value={player.points} />
	<button class="btn btn-primary">Add Player</button>
</form>