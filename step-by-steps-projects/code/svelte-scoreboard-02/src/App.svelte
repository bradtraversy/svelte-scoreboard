<script>
	import Navbar from './Navbar.svelte';
	import Player from './Player.svelte';
	
	let players = [
		{
			name: 'John Doe',
			points: 53
		},
		{
			name: 'Sam Smith',
			points: 45
		},
		{
			name: 'Sara Wilson',
			points: 34
		}
	];
</script>

<Navbar />
<div class="container">
	{#if players.length === 0}
		<p>No players</p>
	{/if}
</div>

