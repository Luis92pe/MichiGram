<script>
	import Profile from "./Profile.svelte";
	import Stories from "./Stories.svelte";
	import Footer from "./Footer.svelte";

	export let nickname = null
	export let name = null
</script>

<style>
    .Sidenav {
        position: relative;
        padding: 4.5em 0 0 0;
    }
    .Sidenav-container {
        position: fixed;
    }
</style>

<div class="Sidenav">
    <div class="Sidenav-container">
        <Profile {nickname} {name}/>
        <Stories />
        <Footer />
    </div>
</div>
