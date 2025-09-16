<script lang="ts">
	import goals from '$lib/goals.json';
	let goal_description = $state(0);
</script>

<div class="grid-container">
	<h1>Goals</h1>
	<h1>working</h1>
	<h1>updates</h1>
	{#each goals as goal, i (goal.id)}
		<div>
			<button onclick={()=> goal_description = i}>{goal.name}</button>
			
		</div>

		<div>
			<button onclick={()=> goal_description = i}>{goal.works}</button>
		</div>

		<div>
			<button onclick={()=> goal_description = i}>{goal.updates}</button>
		</div>
	{/each}
</div>


{#each goals as goal, i (goal.id)}
    {#if i === goal_description}
    	<div>{goal.name}</div>
    {/if}
{/each}

<style>
	.grid-container {
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
	}
	li {
	    list-style: none;
	}
</style>
