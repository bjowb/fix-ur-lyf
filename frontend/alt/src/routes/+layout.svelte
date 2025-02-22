<script>
    let { children } = $props();
    import AppLayout from '../layout/applayout.svelte';
    import "../app.css";
    import Applayout from '../layout/applayout.svelte';
</script>

<Applayout />
{@render children()}