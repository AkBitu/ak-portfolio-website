<script>
  import Header from '../../lib/components/Header.svelte';
  import Footer from '../../lib/components/Footer.svelte';
</script>
<!-- about page header-->
<Header />
<!--about me content section-->
<section class="about-page">
  <div class="about-box">
  <!--profile image and social links-->
    <div class="left">
      <img class="profile" src="/exhibition.jpg" alt="Ak Bitu exhibition " />

      <div class="icons">
        <a href="mailto:akbitu20@gmail.com">
          <img src="/icon/email.png" alt="Email icon link">
        </a>
        <a href="https://linkedin.com/in/ak-bitu-444466253">
          <img src="/icon/linkdin.png" alt="linkedin icon link" >
        </a>
        <a href="https://www.instagram.com/bitusartcreation" >
          <img src="/icon/insta.png" alt="Intagram link">
        </a>
        <a href="https://discord.com/users/1284253232775827509">
        <img src="icon/discord.png" alt="Discord link">
      </a>
        <a href="https://github.com/AkBitu">
        <img src="/icon/github2.png" alt="Github link"> 
      </a>
      </div>

      <button class="cv">📩 Download CV </button>
    </div>
<!--about text content-->
    <div class="right">
      <h1>About Me</h1>

      <h3>Hi, I’m Ak Bitu</h3>
      <h4>Digital Artist & Visual Design Student</h4>

      <p>
        I am a self-taught digital artist and student with a passion for creating
        visual stories through art. I enjoy exploring different styles and mediums,
        including animation, digital painting, and 3D design.
      </p>

      <p>
        Art is my way of expressing ideas, emotions, and creativity. I love combining
        soft colours, clean layouts, and imaginative concepts to create meaningful
        and engaging visuals.
      </p>

      <h2>My Approach:</h2>

      <p>
        I believe design should be simple, clear, and visually appealing. I focus on
        creating work that is easy to understand and enjoyable to look at. I aim to
        design projects that connect with people and communicate ideas effectively.
      </p>
    </div>
  </div>
</section>

<Footer />

<style>
:global(body) {
  margin:0;
  padding: 0px;
}
:global(main) {
  margin:0;
  padding:0px;
  
}
/*about page layout*/
  .about-page {
    margin: 0;
    padding: 20px;
    min-height: 100vh;
    padding-top: 20px;
    background: #fae1f9;
    padding-bottom: 80px;
  }

  .about-box {
    max-width: 1050px;
    margin: 0px auto;
    padding : 35px;
    display: grid;
    grid-template-columns: 320px 1fr;
    gap: 45px;
    align-items: center;
    

    background: rgba(150, 130, 145, 0.55);
    border-radius: 10px;
  }

  .left {
    text-align: center;
  }

  .profile {
    width: 270px;
    height: 300px;
    object-fit: cover;
    border-radius: 18px;
    border: 5px solid #58a78f;
  }

  .icons {
    display: flex;
    justify-content: center;
    gap: 12px;
    margin: 18px 0;
    align-items: center;
  }
  /*social icon hover effects*/
  .icons img{
    height: 24px;
    width:24px;
    transition: 0.3s;
    cursor: pointer;
  }
 .icons img:hover {
  transform: scale(1.15);
 }
  .icons a {
    text-decoration: none;
    font-size: 18px;
    font-weight: bold;
    color: black;
  }
button {
  transition: 0.3s;
  cursor: pointer;
}
button:hover {
  background: #379f84;
  transform: scale(1.05);
}
  .cv {
    padding: 10px 18px;
    border-radius: 12px;
    border: 2px solid #58a78f;
    background: #c7efe5;
    color: #16806b;
    font-weight: bold;
    cursor: pointer;
  }

  .right h1 {
    font-family: Georgia, serif;
    font-style: italic;
    font-size: 44px;
    color: #5a2639;
    margin-bottom: 15px;
    text-align: left;
  }

  .right h3 {
    margin: 0;
    font-size: 20px;
    text-align: left;
  }

  .right h4 {
    margin: 4px 0 22px;
    font-size: 16px;
    text-align: left;
  }

  .right p {
    font-size: 16px;
    line-height: 1.5;
    color: black;
    text-align: left;
  }

  .right h2 {
    margin-top: 28px;
    font-size: 24px;
    color: #2f1830;
    text-align: left;

  }
  @media (max-width: 768px) {
    .about-page {
      padding: 20px;
    }
  .about-box {
    display: flex;
    flex-direction: column;
    height: auto;
    min-height: auto;
    overflow: visible;
    
  }

  .right {
    text-align: left;
    width: 100%;
  }

  footer {
    margin-top: 40px;
  }
  
}/* Responsive design */

</style>