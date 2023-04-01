<script>
	export let open = false

	const closeNav = () => {
		open = false
	}
</script>

<aside class="absolute w-full h-full shadow-lg" class:open>
	<nav class="p-12">
		<a on:click={() => closeNav()} class="block nav-link" href="/#home">Home</a>
		<a on:click={() => closeNav()} class="block nav-link" href="/#about">About</a>
		<a on:click={() => closeNav()} class="block nav-link" href="/#projects">Projects</a>
		<a on:click={() => closeNav()} class="block nav-link" href="/#contact">Contact</a>
		<a on:click={() => closeNav()} class="block nav-link" href="/cv">CV</a>
	</nav>
</aside>

<style>
	aside {
		left: -100%;
		transition: left 0.3s ease-in-out;
		background: var(--background-main);
		position: fixed;
		z-index: 19;
	}

	nav {
		display: flex;
		flex-direction: column;
		justify-content: center;
		gap: 2em;
		height: 100%;
	}

    .nav-link {
		padding: 0.2em;
		border-radius: 5px;
        font-size: 1.2rem;
		font-weight: bold;
		text-align: center;
		border: 2px solid var(--color-text);
		transition: var(--hover-effect);
    }

	.nav-link:hover {
		border: 2px solid var(--hover-color);
		color: var(--hover-color);
		/* color: #9D4DFF;
		border: 2px solid #9D4DFF; */
		/* background: #66C5FF; */
	}
	
	.open {
		left: 0
	}

    @media (min-width: 50em){
        aside {
            left: 0;
            width: var(--side-nav-space);
			border-right: 2px dashed var(--color-text);
        }
    }
</style>