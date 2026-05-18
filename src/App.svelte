<script>
  import Header from './lib/components/Header.svelte';
  import Footer from './lib/components/Footer.svelte';
</script>

<Header />

<main class="home">
  <section class="hero">
    <div class="hero-text">
      <h1><span>Hi, I'm</span> Ak Bitu</h1>
      <p>Digital Artist & Student</p>
      <small> I create animation, vibrant paintings and 3D artwork. 3rd Year Computing in Digital Art & Design at SETU.

      </small>
    
      <div class="buttons">
        <button>View Portfolio</button>
        <button class="secondary">📩 Download CV</button>
      </div>
      </div>
    

<div class="banner-image">
      <img src="/banner_1.jpg" alt="Artwork" />
    </div>
  </section>

  <section class="features">
    <h2>Feature Work</h2>

    <div class="cards">

      <div class="card">
      <div class="card-images two-images">
      <img src="/animation_1.gif" alt="Animation 1">
      <img src="/animation_2.jpg" alt="Animation 2">
      </div>

      <div class="card-content">
        <h3>Animation</h3>
        <p>Motion and 2D Animations</p>
      </div>
      </div>

      <div class="card">
       <div class="card-images">
      <img src="/environment.png" alt="environment">
       </div>
      <div class="card-content">
        <h3>Environment</h3>
        <p>Background and Environment Design</p>
      </div>
      </div>

      <div class="card">
      <div class="card-images">
      <img src="/3d.jpg" alt="3d">
       </div>
  
      <div class="card-content">
        <h3>3D Art</h3>
        <p>Blender and Maya Projects</p>
      </div>
    </div>
    </div>
  </section>
</main>

<Footer />

<style>
  :global(body) {
    margin: 0;
    font-family: Arial, sans-serif;
    background:#fae1f9;
    
  }

  .hero {
    display:flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 25px;
    background: #c5a8bf;
    border-radius: 30px;
    max-width: 900px;
    margin: 30px auto;
    gap:20px;
  }
  .hero-text {
    flex:1;
    text-align: left;

  }

  .hero-text h1 {
    font-size:42px;
    font-family: Georgia, serif;
    font-style: italic;
    color: #5a3d6b;
    margin: 0;
  }

  .hero-text h1 span {
    font-size: 30px;
    margin-right: 15px;
  }

  .hero-text p{
    font-size: 20px;
    font-weight: bold;
    color:black;
    margin: 8px 0;
  }
  .hero-text small{
    display: block;
    font-size: 14px;
    color:#444;
    margin-top: 10px;
    max-width: 380px;
  }
 
 .banner-image img {
  width:400px;
  height: 220px;
  object-fit: cover;
  border-radius:18px;
  display: block;
 }
 .features {
  padding:20px;
  text-align:center;
  margin-top: 60px;
 }
 .features h2{
  font-size: 36px;
  font-family: Georgia, serif;
    font-style: italic;
    color: #5a3d6b;
 }
 .cards {
  display: flex;
  justify-content:center;
  gap: 20px;

 }
 .card {
  background: white;
  width: 300px;
  border-radius:18px;
  overflow: hidden;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  text-align: center;
 }
 .card-images{
  display: flex;
  width: 100%;
  height: 160px;
  
 }
 .card-images img {
width: 100%;
height: 100%;
height: 180px;
object-fit: cover;

 }
 .two-images img{
  width:50%;
 }
 
 .card-content {
  background: #4aac93;
  padding: 12px;
  text-align: center;
  margin-top: 20px;
 }
 .card-content h3{
  margin: 0;
  font-size: 28px;
  color:#fde7fc;
 }
 .card-content p{
  margin-top: 8px;
  font-size: 16px;
  color:#070707;
 }
 .buttons {
  display:flex;
  gap:20px;
  margin-top:18px;
  justify-content: flex-start;
 }

  .buttons button {
    margin-right: 10px;
    border: none;
    padding: 8px 20px;
    font-size: 16px;
    cursor: pointer;
    border:none;
    border-radius: 20px;
  }

    .buttons button:first-child {
      background: #26f8ee;
      color:black
    }
    .secondary {
  background: rgb(255, 255, 255);
  border:1px solid #58c7c2;
 }

  
  
</style>