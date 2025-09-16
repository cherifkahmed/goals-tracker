<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	import logo from '$lib/assets/record-svgrepo-com.svg';

	let { children } = $props();
</script>

<nav>
    <h1>Goals Tracker <img alt="." src={logo} style="width: 30px; height: 30px;"/> </h1>
</nav>

<style>

nav {
    overflow: hidden;
    background-color: palevioletred;
}
</style>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}
