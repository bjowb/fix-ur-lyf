<script lang="ts">
	import AppLayout from '../layout/applayout.svelte';
	import '../app.css';
	let { children } = $props();
</script>

<AppLayout />
{@render children()}
