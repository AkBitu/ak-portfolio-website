<script>
  import Header from '../../lib/components/Header.svelte';
  import Footer from '../../lib/components/Footer.svelte';

  const works = [
    {
      title: "Drawings",
      image: "/ak-portfolio-website/drawing.jpg"
    },
    {
      title: "Paintings",
      image: "/ak-portfolio-website/paintings.jpg"
    },
    {
      title: "Exhibitions",
      image: "/ak-portfolio-website/exhibition.jpg"
    }
  ];
</script>
<!--Portfolio page header-->
<Header />
<!--portfolio gallery section-->
<section class="traditional-page">
  <div class="portfolio-box">
    <h1>Traditional Portfolio</h1>

    <div class="gallery">
    <!--project cards-->
      {#each works as work}
        <div class="card">
          <img src={work.image} alt={work.title} />
          <div class="card-content">
          <h3>{work.title}</h3>
        </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<Footer />

<style>
  .traditional-page {
    min-height: 100vh;
    background: #f5edf2;
    padding: 20px 20px;
  }

  .portfolio-box {
    background: rgba(180, 165, 175, 0.8);
    padding: 80px;
    border-radius: 10px;
    max-width: 1200px;
    margin: auto;
    text-align: center;
    min-height: 450px;
  }

  h1 {
    font-size: 48px;
    font-family: Georgia, serif;
    font-style: italic;
    color: #5a2d3b;
    margin-bottom: 50px;
  }

  .gallery {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
  }
/* portfolio card styling */
  .card {
    background: white;
    width: 280px;
    height: 280px;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0,0,0,0.15);
    transition: transform 0.3s;
  }
/* card hover efect */
  .card:hover {
    transform: scale(1.05);
  }
   .card-content {
    background: #4aac93;
    padding: 16px;
    text-align: center;
    margin-top: 0;
    
    
   }
  .card img {
    width: 100%;
    height: 180px;
    object-fit: cover;
  }

  .card h3 {
    padding: 20px;
    font-size: 24px;
    margin: 0;
    color: #f1f0f1;
  }
</style>