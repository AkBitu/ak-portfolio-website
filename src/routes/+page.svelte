
<script>
import { onMount } from 'svelte';
  import Header from '../lib/components/Header.svelte';
  import Footer from '../lib/components/Footer.svelte';

  let currentSlide = 0;

  const slides = [
      { title: "Hi, I’m Ak Bitu",
      subtitle: "Digital Artist & Computing Student",
      text: "I create animations, digital paintings, 3D artwork and interactive creative projects while studying Computing in Digital Art & Design at SETU.",
      image: "/banner_1.jpg"
    },
    {
      title: "Games Fleadh Project",
      subtitle: "Creative Game Development",
      text: "Developed an interactive student game project showcasing creativity and storytelling.",
      image: "/gamefleadh.jpeg"
    },
    {
      title: "Google Scholarship Recipient",
      subtitle: "Technology Learning Achievement",
      text: "Recognised for commitment to technology learning and digital skills development.",
      image: "/google.jpg"
    },
    {
      title: "Exhibiting Artist",
      subtitle: "Barrow Valley Art Group",
      text: "Participated in public exhibitions presenting traditional artwork.",
      image: "/exhibition.jpg"
    }
  ];

  function nextSlide() {
    currentSlide = (currentSlide + 1) % slides.length;
  }

  function previousSlide() {
    currentSlide = (currentSlide - 1 + slides.length) % slides.length;
  }

  onMount(() => {
    const interval = setInterval(nextSlide, 4000);
    return () => clearInterval(interval);
  });

</script>
<!--Header Navigation-->
<Header />
<!--main homepage content-->
<main class="home">
<!--banner slideshow-->
  <section class="hero">
  <button class="arrow" on:click={previousSlide}>&lt;</button>
  
  


    <div class="hero-text">
    <h1>{slides[currentSlide].title}</h1>
<p>{slides[currentSlide].subtitle}</p>
<small>{slides[currentSlide].text}</small>

      <!--<h1><span>Hi, I'm</span> Ak Bitu</h1>
      <p>Digital Artist & Student</p>
      <small> I create animation, vibrant paintings and 3D artwork. 3rd Year Computing in Digital Art & Design at SETU.

      </small>
    -->
    
      <div class="buttons">
        <button>View Portfolio</button>
        <button class="secondary">📩 Download CV</button>
      </div>
      </div>
    

<div class="banner-image">
      <img src={slides[currentSlide].image} alt={slides[currentSlide].title}>
    </div>
<button class="arrow" on:click={nextSlide}>&gt;</button> 
  
  </section>
<!--featured project cards-->
  <section class="features">
    <h2>Feature Work</h2>

    <div class="cards">

      <div class="card">
      <div class="card-images two-images">
      <img src="/animation_1.gif" alt="Animation 1 gif">
      <img src="/animation_2.jpg" alt="Animation 2 concept">
      </div>

      <div class="card-content">
        <h3>Animation</h3>
        <p>Motion and 2D Animations</p>
      </div>
      </div>

      <div class="card">
       <div class="card-images">
      <img src="/environment.png" alt="environment artwork">
       </div>
      <div class="card-content">
        <h3>Environment</h3>
        <p>Background and Environment Design</p>
      </div>
      </div>

      <div class="card">
      <div class="card-images">
      <img src="/3d.jpg" alt="3d artwork">
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
/* hero section styling */
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
 /* feature cards styling */
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
  transition:all 0.3s ease;
  cursor:pointer

 }
 .card:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 25px rgba(0,0,0,0.2);
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
    .buttons button:first-child:hover {
  background: linear-gradient(
    135deg,
    #37f7d8,
    #2dcfff
  );

  transform: translateY(-px) scale(1.08);

  box-shadow:
    0 16px 28px rgba(50, 220, 220, 0.45),
    inset 0 2px 2px rgba(255,255,255,0.9);
}
.secondary:hover {
  background: linear-gradient(
    135deg,
    #ffffff,
    #f2e8ff
  );

  transform: translateY(-3px) scale(1.08);

  box-shadow:
    0 16px 28px rgba(170, 140, 220, 0.25),
    inset 0 2px 2px rgba(255,255,255,1);
}
    .secondary {
  background: rgb(255, 255, 255);
  border:1px solid #58c7c2;
 }

  /* Responsive design */
@media (max-width: 768px) {
  nav {
    flex-direction: column;
    gap: 12px;
    padding: 15px;
  }

  .hero,
  .about-box,
  .cv-box,
  .contact-box {
    display: flex;
    flex-direction: column;
    width: 100%;
  }

  .gallery,
  .cards {
    flex-direction: column;
    align-items: center;
  }

  .hero img,
  .profile,
  .card img,
  .map {
    max-width: 100%;
  }

  h1 {
    font-size: 32px;
  }

  p {
    font-size: 14px;
  }
}
  
</style>