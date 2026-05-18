
<nav>
  <a href="about">ABOUT ME</a>
  <a href="traditional">TRADITIONAL PORTFOLIO</a>

  <div class="logo">
    <img src="/logo.png" alt="logo">
  </div>

  <a href="digital">DIGITAL PORTFOLIO</a>
  <a href="cv">CV</a>
  <a href="contact" class="contact-btn">CONTACT</a>
</nav>

<style>
  nav {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 18px;
    flex-wrap: wrap;
    padding: 20px;

  }

  a {
    text-decoration: none;
    background: #f7d6f5;
    padding: 3px 14px;
    border-radius: 12px;
    color: black;
    font-size: 13px;
    font-weight: bold;
  }

  .logo img {
    width: 140px;
    height:80px;
    object-fit: cover;
    border-radius: 16px;
  }
  .logo {
    width: 140px;
    height: 80px;
    background: #9feff0;
    border:3px solid rgb(28, 43, 46);
    border-radius: 18px;
    padding: 0px;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .contact-btn{
    background:#857b84;
    color: white;
  }

</style>