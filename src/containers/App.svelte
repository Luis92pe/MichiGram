<script>
    import { onMount } from 'svelte'
	import Header from "../components/Header.svelte";
	import Main from "../components/Main.svelte";
	import Timeline from "../components/Timeline.svelte";
	import Sidenav from "../components/Sidenav.svelte";

	let data = {}
    const API = 'https://kittygram-api.now.sh/'

    onMount(async () => {
    	try {
		    const response = await fetch(API)
            data = await response.json()
		    console.log(data)
	    } catch (e) {
		    console.log(e)
	    }

    })


</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Lato:wght@300;400&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

    :global(body) {
        background-color: #fafafa;
        color: rgba(38,38,38,0.7);
        font-family: 'Lato', 'Helvetica';
        margin: 0;
        padding: 0;
    }
    :global(h1,h2,h3) {
        margin: 0;
        padding: 0;
    }
</style>

<Header />
<Main>
    <Timeline posts={data.posts}  />
    <Sidenav {...data.user} />
</Main>
