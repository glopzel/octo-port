<script>
    import Hamburger from "./Hamburger.svelte";

    export let sidebar = false;
</script>

<header class="flex items-center text-gray-600">
	<nav class="flex">
		<Hamburger bind:open={sidebar}/>
	</nav>
</header>

