<script>
  import Header from '../../lib/components/Header.svelte';
  import Footer from '../../lib/components/Footer.svelte';
</script>

<Header />

<section class="contact-page">
  <div class="contact-box">

    <div class="profile-card">
      <img src="/profile.jpg" alt="Ak Bitu" />
      <h2>Ak Bitu</h2>
      <p>Digital Artist & Visual Design</p>
      <small>Digital artist and design student passionate about animation, 3D art and creative visual storytelling.</small>

      <p class="info">📧 c00313310@setu.ie<br>📞 +353000000000</p>

      <div class="icons">
        <img src="/icon/linkdin.png"  alt="linkdin"/>
        <img src="/icon/insta.png" alt="instagram" />
        <img src="/icon/discord.png" alt="discord" />
        <img src="/icon/github2.png" alt="github "/>
      </div>

      <button>✉️ Say Hello</button>
    </div>

    <div class="middle">
      <h1>Let's Work<br><span>Together</span></h1>
      <p>
        Have a project in mind or just want to say Hello?
        Fill out the form and I'll get back to you as soon as possible.
      </p>
    
      <h3> <img src="/icon/map.png" alt="map"> Find me Here</h3>
      <iframe class="map" src="https://www.google.com/maps?q=SETU%20Carlow&output=embed">
    </iframe>
     
    </div>

    <div class="right">
      <form class="message-box">
        <h3>📩 Send a Message</h3>
        <div class="row">
          <input placeholder="Your Name" />
          <input placeholder="Your Email" />
        </div>
        <input placeholder="Subject" />
        <textarea placeholder="Message"></textarea>
        <button type="button"> 💬Send Message</button>
      </form>

      <div class="connect">
        <h3><img class="icon" src="/icon/link.png" alt="link">Connect with me</h3>
        <small>Follow me for updates, artwork</small>
        <div class="icons big">
          <img src="/icon/linkdin.png" alt="linkdin" />
          <img src="/icon/insta.png" alt="instagram" />
          <img src="/icon/discord.png" alt="discord"/>
          <img src="/icon/github2.png" alt="github" />
        </div>
      </div>
    </div>

  </div>
</section>

<Footer />

<style>
  .contact-page {
    background: #f5edf2;
    padding: 20px;
  }

  .contact-box {
    max-width: 1200px;
    margin: auto;
    background: #b8e2d2;
    display: grid;
    grid-template-columns: 250px 1fr 380px;
    gap: 30px;
    align-items: start;
    padding: 30px;
  }
  .middle {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
  }
  .middle h1 {
    font-size: 28px;
    line-height: 1;
    margin-bottom: 20px;
    text-align: left;
    padding-top: 20px;
  }
  .middle p {
    max-width: 350px;
    font-size: 16px;
    line-height: 1.4;
    padding-bottom: 60px;
    text-align: left;
  }
  .middle h3 {
    margin-top: 40px;
    font-size: 24px;
    text-align: left;
  }
  .middle img {
   width: 60px;
    height: 60px;
}
  .profile-card {
    background: #b8aeb6;
    text-align: center;
    padding: 20px;
  }

  .profile-card img {
    width: 120px;
    border-radius: 50%;
  }

  h1 {
    font-size: 38px;
    margin: 0;
  }

  h1 span {
    font-family: Georgia, serif;
    font-style: italic;
    color: #5a2d3b;
    font-size: 48px;
    
  }

  .map {
    width: 100%;
    max-width: 350px;
    height: 220px;
    object-fit: cover;
    border-radius: 12px;
    border:none;
  }

  .message-box {
    background: #f9e8ef;
    padding: 20px;
    border-radius: 16px;
  }

  input,
  textarea {
    width: 100%;
    margin: 6px 0;
    padding: 10px;
    border: 2px solid #58a78f;
    border-radius: 8px;
    box-sizing: border-box;
  }

  textarea {
    height: 100px;
  }

  .row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
  }

  button {
    background: #4aac93;
    color: white;
    border: none;
    padding: 10px 18px;
    border-radius: 10px;
    cursor: pointer;
  }

  .icons {
    display: flex;
    justify-content: center;
    gap: 12px;
    margin: 15px 0;
  }

  .icons img {
    width: 30px;
    height: 30px;
    object-fit: contain;
  }
  .icon {
    width: 60px;
    height: 60px;
  }
  
.connect h3 {
  display: flex;
  align-items: center;
  gap: 10px;
}
  .big img {
    width: 45px;
    height: 45px;
  }
  
</style>