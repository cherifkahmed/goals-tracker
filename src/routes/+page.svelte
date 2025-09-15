<script lang="ts">
	import goals from '$lib/goals.json';
</script>

<div class="grid-container">
	<h1>Goals</h1>
	<h1>working</h1>
	<h1>updates</h1>
	{#each goals as goal, i (goal.id)}
		<div>
			<li>{i + 1} {goal.name}</li>
		</div>

		<div>
			<li>{goal.works}</li>
		</div>

		<div>
			<li>{goal.updates}</li>
		</div>
	{/each}
</div>

<style>
	.grid-container {
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
	}
	li {
	    list-style: none;
	}
</style>
