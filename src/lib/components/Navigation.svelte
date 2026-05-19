<script>
let path = window.location.pathname;
let menuOpen = false;
</script>

<button class="hamburger" on:click={() => menuOpen = !menuOpen}>
  <img src="/icon/menu.png" width="40px" alt="menu">
</button>

<nav class:show={menuOpen}> 
  <a href="/about" class:active={path === '/about'}>ABOUT ME</a>
  <a href="traditional" class:active={path === '/traditional'}>TRADITIONAL PORTFOLIO</a>
  
  <a href="/" class="logo">
    <img src="/logo.png" alt="logo">
  </a>

 <a href="digital" class:active={path === '/digital'}>DIGITAL PORTFOLIO</a>
  <a href="cv" class:active={path === '/cv'}>CV</a>
  <a href="contact" class:active={path === '/contact'}>CONTACT</a>
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
    background: rgba(241, 185, 238, 0.87);
    font-weight: bold;
    backdrop-filter: blur(14px);
    -webkit-backdrop-filter: blur(14px);

    border:1px solid rgba(255, 255, 255, 0.35);
    box-shadow: 0 4px 10px rgba(0,0,0,0.12), inset 0 1px 1px rgba(255,255,255,0.8);
    padding: 6px 18px;
    transition: all 0.35s ease;
    border-radius: 12px;
    color: black;
    font-size: 13px;
    font-weight: bold;
  }

  a:hover {
    transform: translateY(-3px) scale(1.04);
    background: rgba(255, 255, 255, 0.493);
    box-shadow: 0 10px 25px rgba(0,0,0,0.18),
     inset 0 -2px 3px rgba(255,255,255,0.35);
     border:1px solid rgba(255,255,255,0.55);
    color: #3a2a50;
  }
  a.active {
    background: rgba(255,255,255,0.35);
    border: 1px solid rgba(255,255,255,0.6);
    box-shadow:inset 0 2px 8px rgba(255,255,255,0.5),
    0 4px 12px rgba(0,0,0,0.15);
    color:#222;
    transform:  scale(1.08);
  }

  .logo img {
    width: 130px;
    height:auto;
    display: block;
    object-fit: contain;
    border-radius: 12px;
    transition: all 0.35s ease;
  }

  .logo {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 6px;
  border-radius: 18px;

  background: rgba(255,255,255,0.14);
  backdrop-filter: blur(18px);
  -webkit-backdrop-filter: blur(18px);

  border: 1px solid rgba(255,255,255,0.45);

  box-shadow:
    0 10px 22px rgba(0,0,0,0.15),
    inset 0 2px 2px rgba(255,255,255,0.9),
    inset 0 -2px 4px rgba(255,255,255,0.15);
    transition:all 0.35s ease;
  }
  .contact-btn{
    background:#857b84;
    color: white;
  }
/* hamburger menu*/
.hamburger {
  display: none;
  font-size: 28px;
  border: none;
  background: transparent;
  cursor: pointer;
  color: #4b2f5e;
  margin: 10px;
}

/*responsive page*/

@media (max-width: 768px) {
  .hamburger {
    display: block;
  }

  nav {
    display: none;
    flex-direction: column;
    gap: 12px;
    padding: 20px;
    align-items: center;
  }

  nav.show {
    display: flex;
  }

  .logo img {
    width: 90px;
  }

  nav a {
    width: 90%;
    text-align: center;
  }
}
</style>