<script>
  import Header from '../../lib/components/Header.svelte';
  import Footer from '../../lib/components/Footer.svelte';

</script>

<Header />

<section class="cv-page">
 <div class="cv-box">
   <div class="profile-card">
     <img src="/profile.jpg" alt="Ak Bitu profile pic">
      <h2> <b> Ak Bitu </b></h2>
      <p><b> Digital Artist & Visual Design </b></p>
      <small>
        Digital artist and design student passionate about animation, 3D art and creative visual storytelling.
      </small>
      <p class="contact">C00313310@setu.ie<br />SETU Carlow Campus</p>
      <button>📩 Download CV </button>
    </div>

     <div class="cv-content">
      <h1><b>Curriculum Vitae</b></h1>

      <div class="cv-grid">
        <div class="education">
          <h3><img class="icon" src="/icon/education.png" alt="Education icon"> 
            Education </h3>
          <p><b>2023 - Present</b><br />BSc Computing in Interactive Digital Art & Design</p>
          <p><b>2021 - 2022</b><br />Certificate Applied Digital Marketing</p>
        
        <div class="skills">
          <h3><img class="icon" src="/icon/skills.png" alt="skills symbol">Skills</h3>
          <ul>
            <li>Animation & Spine</li>
            <li>Concept Art</li>
            <li>3D Art: Blender, Maya</li>
            <li>Illustrator & UI Design</li>
            <li>Sketching & Painting</li>
          </ul>
        </div>
        </div>

        <div class="experience">
          <h3><img class="icon" src="/icon/work2.png" alt="work experience icon"> Experience</h3>
          <p><b>Game Project</b><br />Best Game Award Winner, Games Fleadh 2026</p>
          <p><b>Art Exhibition Participant</b><br />Barrow Valley Artist Group</p>
          <p><b>Freelance Logo Designer</b><br />Client work</p>

          <h3><img class="icon" src="/icon/interest.png" alt="heart icon">Interests</h3>
          <div class="interests">
          <h3><img class="icon" src="/icon/draw.png" alt="Sketching icon"></h3>
          <h3><img class="icon" src="/icon/animator.png" alt="animation icon"></h3>
          <h3><img class="icon" src="/icon/3D.png" alt="threeD icon"></h3>
          <h3><img class="icon" src="/icon/color.png" alt="painting icon"></h3>
            
          </div>
        </div>
      </div>
      
      <div class="summary">
      <h3><img class="icon" src="/icon/aa.png" alt="comment icon"></h3>
        Creative digital artist and design student with skills in animation, 3D design, and visual storytelling.
        Strong interest in game art, 2D/3D design and freelance logo design.
      </div>
    </div>
  </div>
</section>

<Footer />

<style>
  .cv-page {
    background: #f5edf2;
    padding: 20px;
  }

  .cv-box {
    max-width: 1200px;
    margin: auto;
    background: #b8aeb6;
    padding: 40px;
    display: grid;
    grid-template-columns: 260px 1fr;
    gap: 45px;
  }

  .profile-card {
    background: #f8edf1;
    padding: 40px;
    text-align: center;
  }

  .profile-card img {

    width: 130px;
    border-radius: 50%;
  }

  .profile-card h2 {
    padding: 20px;
    font-family: Georgia, serif;
    font-style: italic;
    font-size: 34px;
    color: #5a2d3b;
  }

  .profile-card button {
    margin-top: 20px;
    padding: 10px 18px;
    border-radius: 12px;
    border: 2px solid #58a78f;
    background: #c7efe5;
    color: #16806b;
    font-weight: bold;
  }

  .cv-content {
    background: #f8edf1;
    padding: 30px;
  }

  .cv-content h1 {
    font-family: Georgia, serif;
    font-style: italic;
    font-size: 44px;
    color: #5a2d3b;
    text-align: center;
  }

  .cv-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 50px;
    align-items: start;
  }

  h3 {
    display: flex;
    align-items: center;
    color: #26856f;
    font-size: 24px;
  }
  h3 img {
  vertical-align: middle;
  margin-right: 8px;
  width: 40px;
}

  p, li, small {
    font-size: 14px;
    line-height: 1.5;
  }  
    .skills ul {
        padding: 0 40px;
    }
    
  
  .education ,
  .experience,
  .skills ul {
    text-align: left;
  }
  

  .summary {
    margin-top: 25px;
    background: #b8aeb6;
    padding: 20px;
    border-radius: 12px;
    font-size: 14px;
    min-height: 100px;

    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
  }
  .education p,
  .experience p {
    text-align: left;
    margin-left: 20px;
  }
  .interests {
    display: flex;
    gap: 15px;
    align-items: center;
    margin-top: 15px;
  }
  .summary img {
    width: 30px;
    height: 30px;
    margin-right: 10px;
  }
  button {
  transition: 0.3s;
  cursor: pointer;
}
button:hover {
  background: #379f84;
  transform: scale(1.05);
}

   /* Responsive design */
@media (max-width: 768px) {
  .cv-box {
    grid-template-columns: 1fr;
    padding: 20px;
  }

  .cv-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }

  .profile-card {
    width: 100%;
  }
  


  .cv-content h1 {
    font-size: 34px;
  }
}
</style>

  