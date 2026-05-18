<script>
import Home from './routes/+page.svelte';
import About from './routes/about/+page.svelte';

let path = window.location.pathname;
</script>

{#if path == '/about'}
<About />
{:else}
<Home />
{/if}