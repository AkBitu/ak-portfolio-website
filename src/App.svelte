<script>
  import Header from './lib/components/Header.svelte';
  import Footer from './lib/components/Footer.svelte';
</script>

<Header />

<main>
  <section class="hero">
    <h2>Welcome to My Portfolio</h2>
    <p>I am Ak Bitu, a digital artist and computing interective digital art and design student.</p>
    <button>View My Projects</button>
  </section>
</main>

<Footer />

<style>
  :global(body) {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #f5f5f5;
  }

  .hero {
    text-align: center;
    padding: 100px 20px;
  }

  h2 {
    font-size: 42px;
    margin-bottom: 20px;
  }

  p {
    font-size: 20px;
    margin-bottom: 30px;
  }

  button {
    background: #222;
    color: white;
    border: none;
    padding: 15px 30px;
    font-size: 16px;
    cursor: pointer;
    border-radius: 8px;
  }
</style>