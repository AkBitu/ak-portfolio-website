<script>
import Home from './routes/+page.svelte';
import About from './routes/about/+page.svelte';
import Traditional from './routes/traditional/+page.svelte';

let path = window.location.pathname;
</script>

{#if path == '/about'}
<About />
{:else if path == '/traditional'}
<Traditional />
{:else}
<Home />
{/if}