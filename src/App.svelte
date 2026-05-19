<script>
import Home from './routes/+page.svelte';
import About from './routes/about/+page.svelte';
import Traditional from './routes/traditional/+page.svelte';
import Digital from './routes/digital/+page.svelte';
import Cv from './routes/cv/+page.svelte';
import Contact from './routes/contact/+page.svelte';

let path = window.location.pathname;
</script>

{#if path == '/about'}
<About />
{:else if path == '/traditional'}
<Traditional />
{:else if path == '/digital'}
  <Digital />
{:else if path == '/cv'}
  <Cv />
{:else if path == '/contact'}
  <Contact />
{:else}
<Home />
{/if}