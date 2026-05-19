<script>
  import Header from '../../lib/components/Header.svelte';
  import Footer from '../../lib/components/Footer.svelte';

  const works = [
    { title: "Animation",
      text: "Motion & 2D Animations", 
      image: "/animation_1.gif" 
    },
    { title: "Environment", 
      text: "Background and Environment", 
      image: "/environment.png" 
    },
    { title: "3D Art",
      text: "Blender & Maya 3D", 
      image: "/3d.jpg" 
    },
    { title: "Games Fleadh",
     text: "SITLab 0023 Project",
      image: "/gamefleadh.jpeg" 
    }
  ];
</script>

<Header />

<section class="digital-page">
  <div class="portfolio-box">
    <h1>Digital Portfolio</h1>

    <div class="gallery">
      {#each works as work}
        <div class="card">
          <img src={work.image} alt={work.title} />

          <div class="card-content">
            <h3>{work.title}</h3>
            <p>{work.text}</p>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<Footer />

<style>
  .digital-page {
    background: #f5edf2;
    padding: 20px;
  }

  .portfolio-box {
    background: #b8aeb6;
    padding: 45px;
    border-radius: 10px;
    max-width: 1200px;
    margin: auto;
    text-align: center;
  }

  h1 {
    font-size: 48px;
    font-family: Georgia, serif;
    font-style: italic;
    color: #5a2d3b;
    margin: 0 0 35px;
  }

  .gallery {
    display: flex;
    justify-content: center;
    gap: 35px;
    flex-wrap: wrap;
  }

  .card {
    background: white;
    width: 260px;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 12px rgba(0,0,0,0.18);
    transition: 0.3s ease;
  }

  .card:hover {
    transform: translateY(-8px) scale(1.04);
  }

  .card img {
    width: 100%;
    height: 170px;
    object-fit: cover;
  }

  .card-content {
    background: #4aac93;
    padding: 14px;
  }

  .card-content h3 {
    margin: 0;
    font-size: 22px;
    color: white;
  }

  .card-content p {
    margin: 6px 0 0;
    font-size: 14px;
    color: black;
  }
</style>