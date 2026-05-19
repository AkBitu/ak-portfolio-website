<script>
import Home from './routes/+page.svelte';
import About from './routes/about/+page.svelte';
import Traditional from './routes/traditional/+page.svelte';
import Digital from './routes/digital/+page.svelte';

let path = window.location.pathname;
</script>

{#if path == '/about'}
<About />
{:else if path == '/traditional'}
<Traditional />
{:else if path == '/digital'}
  <Digital />
{:else}
<Home />
{/if}