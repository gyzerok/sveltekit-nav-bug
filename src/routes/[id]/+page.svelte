<script>
	import { goto, pushState } from '$app/navigation';
	import { page } from '$app/stores';

	$effect(() => console.log('params', $page.params));
	$effect(() => console.log('state', $page.state));
</script>

<button onclick={() => goto('/bug', { state: { rnd: Math.random() } })}>goto</button>
<button onclick={() => pushState('/test', { rnd: Math.random() })}>pushState</button>

<button onclick={() => console.log('page', $page)}>Log $page</button>
