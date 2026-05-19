<script>
  import Header from '../../lib/components/Header.svelte';
  import Footer from '../../lib/components/Footer.svelte';

  let sent = false;
  let name ='';
  let email ='';
  let subject ='';
  let message ='';
  let error = false;

  function sendMessage() {
    if (name && email && subject && message) {
    sent =true;
    } else {
        alert("please fill in all fields.");
    }
    
    error=false;
  }
</script>
<!--contact page header-->
<Header />
<!--contact page main content-->
<section class="contact-page">
  <div class="contact-box">

    <!--profile contact card-->
    <div class="profile-card">
      <img src="/ak-portfolio-website/profile.jpg" alt="Ak Bitu profile pic" />
      <h2>Ak Bitu</h2>
      <p>Digital Artist & Visual Design</p>
      <small>Digital artist and design student passionate about animation, 3D art and creative visual storytelling.</small>

      <p class="info">📧 c00313310@setu.ie<br>📞 +353000000000</p>

      <div class="icons">
        <img src="/ak-portfolio-website/icon/linkdin.png"  alt="linkdin link"/>
        <img src="/ak-portfolio-website/icon/insta.png" alt="instagram link" />
        <img src="/ak-portfolio-website/icon/discord.png" alt="discord link" />
        <img src="/ak-portfolio-website/icon/github2.png" alt="github link "/>
      </div>

      <button>✉️ Say Hello</button>
    </div>

    <div class="middle">
      <h1>Let's Work<br><span>Together</span></h1>
      <p>
        Have a project in mind or just want to say Hello?
        Fill out the form and I'll get back to you as soon as possible.
      </p>
    
      <h3> <img src="/ak-portfolio-website/icon/map.png" alt="map icon"> Find me Here</h3>
      <iframe class="map" src="https://www.google.com/maps?q=SETU%20Carlow&output=embed">
    </iframe>
     
    </div>

    <div class="right">
    <!--contact form-->
      <form class="message-box">
        <h3>📩 Send a Message</h3>
        <level> Your Name</level>
        <div class="row">
          <input bind:value={name} required placeholder="Your Name" />
          <input bind:value={email} type="email" required placeholder="Your Email" />
        </div>
        <level> Subject</level>
        <input bind:value={subject} required placeholder="Subject" />

        <level>Message</level>
        <textarea bind:value={message} required placeholder="Message"></textarea>
        <button type="button" on:click={sendMessage}> 💬Send Message</button>
        <!--success feedback message-->
        {#if sent}
        <p class="success">Thanks! Your message has been sent.</p>
        {/if}
      </form>

      <div class="connect">
        <h3><img class="icon" src="/ak-portfolio-website/icon/link.png" alt="link">Connect with me</h3>
        <small>Follow me for updates, artwork</small>
        <div class="icons big">
          <img src="/ak-portfolio-website/icon/linkdin.png" alt="linkdin link" />
          <img src="/ak-portfolio-website/icon/insta.png" alt="instagram link" />
          <img src="/ak-portfolio-website/icon/discord.png" alt="discord link"/>
          <img src="/ak-portfolio-website/icon/github2.png" alt="github link" />
        </div>
      </div>
    </div>

  </div>
</section>

<Footer />

<style>
/* contact page layout*/
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
/* form styling*/
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
/* button hover effects*/
  button {
    background: #4aac93;
    color: white;
    border: none;
    padding: 10px 18px;
    border-radius: 10px;
    cursor: pointer;
    transform: 0.3s;
  }
  button:hover {
    transition: 0.3s;
    transform: scale(1.05);
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
    transition: 0.3s;
    cursor: pointer;
  }
  .icons img:hover {
    transform: scale(1.15);
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
  level {
    display: block;
    text-align: left;
    margin-bottom: 6px;
    font-weight: bold;
  }
  .message-box{
    text-align: left;
  }
  .success {
    color:green;
    margin-top: 10px;
    font-weight: bold;
  }
  /* Keyboard accessibility focus style */
button:focus,
a:focus,
input:focus,
textarea:focus {
  outline: 3px solid #4aac93;
  outline-offset:  3px;
}


   /* Responsive design */
  @media (max-width: 768px) {
  .contact-box {
    grid-template-columns: 1fr;
    padding: 20px;
  }

  .row {
    grid-template-columns: 1fr;
  }

  .middle h1 {
    font-size: 38px;
  }

  .map {
    max-width: 100%;
  }
}
</style>