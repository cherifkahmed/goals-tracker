<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<nav>
    <h1>Goals Tracker</h1>
</nav>

<style>

nav {
    overflow: hidden;
    background-color: darkgoldenrod;
}
</style>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}
