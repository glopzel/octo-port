<script>
    import Sidebar from "./Sidebar.svelte";
    import Navbar from "./Navbar.svelte";

    let open = false;
</script>

<Sidebar bind:open/>
<Navbar bind:sidebar={open}/>