<script>
	import Index from './pages/index.svelte';
	import { Router, Route } from "svelte-navigator";
	import Navbar from './components/navbar.svelte';
</script>

<Router>
	<Navbar />
	<main>
		<Route path="">
			<Index />
		</Route>
	</main>	
</Router>
