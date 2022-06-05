<script lang="ts">
	import { page } from '$app/stores';
    import Navbar  from '$lib/navbar/Navbar.svelte';
	import '../app.css';


</script>

<Navbar pathname={$page.url.pathname} />
<slot />
