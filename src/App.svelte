<script>
	import {Router, Route} from "svelte-navigator"
	import Articles from "./pages/articles.svelte";
	import Colls from "./pages/colls.svelte";
	import Doc from "./pages/doc.svelte";
	import Subjects from "./pages/subjects.svelte";



</script>

<Router>
	<Route path="/" component={Colls} />
	<Route path="/:collection" component={Subjects} />
	<Route path="/:collection/:subject" component={Articles} />
	<Route path="/:collection/:subject/:doc" component={Doc} />
</Router>