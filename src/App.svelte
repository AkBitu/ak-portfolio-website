<script>
  import Header from './lib/components/Header.svelte';
  import Footer from './lib/components/Footer.svelte';
</script>

<Header />

<main class="home">
  <section class="hero">
    <div class="hero-text">
      <h1>Hi, I'm Ak Bitu</h1>
      <p>Digital Artist and Computing in Interactive Digital Art and Design</p>

      <div class="buttons">
        <button>View Portfolio</button>
        <button class="secondary">Download CV</button>
      </div>
    </div>

<div class="hero-image">
      <img src="https://via.placeholder.com/400x250" alt="Artwork" />
    </div>
  </section>

  <section class="features">
    <h2>Feature Work</h2>

    <div class="cards">
      <div class="card">
        <h3>Animation</h3>
        <p>Motion and 2D Animations</p>
      </div>

      <div class="card">
        <h3>Environment</h3>
        <p>Background and Environment Design</p>
      </div>

      <div class="card">
        <h3>3D Art</h3>
        <p>Blender and Maya Projects</p>
      </div>
    </div>
  </section>
</main>

<Footer />

<style>
  :global(body) {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #fae1e7;
  }

  .hero {
    display:flex;
    justify-content: space-between;

    align-items: center;
    padding: 60px;
  }
  .hero-text {
    max-width:500px;
  }

  h1 {
    font-size:48px;
  }
 .secondary {
  background: white;
  border:1px solid #58c7c2;
 }
 .hero-image img {
  width:400px;
  border-radius:10px;
 }
 .features {
  padding:40px;
  text-align:center;
 }
 .cards {
  display: flex;
  justify-content:center;
  gap: 20px;

 }
 .card {
  background:#aaecd2;
  padding:20px;
  width: 220px;
  border-radius:10px;
 }
 .buttons {
  margin-top:20px;
 }

  button {

    background: #58c7c2;
    margin-right: 10px;
    border: none;
    padding: 12px 20px;
    font-size: 16px;
    cursor: pointer;
    border:none;
    border-radius: 20px;
  }
</style>