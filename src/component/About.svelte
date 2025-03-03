<script>
  

</script>  
  <style>
    .about-container {
      background-color: rgba(5, 14, 4, 0.466);
      padding: 2rem;
      box-shadow: 0 0 10px rgba(0, 255, 255, 0.5);
      width: 70%;
      margin: 0 auto;
      animation: neon 1.5s ease-in-out infinite alternate;
    }
  
    .about-title {
      font-size: 2.5rem;
      font-weight: bold;
      color: #ff00ff; 
      text-align: center;
      letter-spacing: 2px;
      margin-bottom: 1rem;
      text-shadow: 0 0 5px #ff00ff, 0 0 10px #ff00ff, 0 0 20px #ff00ff;
      animation: neon-text 1.5s ease-in-out infinite alternate;
    }
  
    .about-content {
      color: #ffee05; /* Cyan neon */
      font-size: 1.25rem;
      line-height: 1.6;
      text-align: center;
      text-shadow: 0 0 5px #00ffff, 0 0 10px #00ffff, 0 0 15px #00ffff;
    }
  
    @keyframes neon {
      0% {
        box-shadow: 0 0 5px #ff00ff, 0 0 10px #ff00ff, 0 0 20px #ff00ff;
      }
      100% {
        box-shadow: 0 0 15px #00ffff, 0 0 25px #00ffff, 0 0 35px #00ffff;
      }
    }
  
    @keyframes neon-text {
      0% {
        text-shadow: 0 0 5px #ff00ff, 0 0 10px #ff00ff, 0 0 20px #ff00ff;
      }
      100% {
        text-shadow: 0 0 15px #ff00ff, 0 0 25px #ff00ff, 0 0 35px #ff00ff;
      }
    }

    .technologies-container {
    background-color: rgba(5, 14, 4, 0.466);
    padding: 2rem;
    box-shadow: 0 0 10px rgba(0, 255, 255, 0.5);
    width: 90%;
    margin: 2rem auto; 
    animation: neon 1.5s ease-in-out infinite alternate;
  }

  .technologies-title {
    font-size: 2.5rem;
    font-weight: bold;
    color: #ff00ff; /* Magenta neon */
    text-align: center;
    letter-spacing: 2px;
    margin-bottom: 1rem;
    text-shadow: 0 0 5px #ff00ff, 0 0 10px #ff00ff, 0 0 20px #ff00ff;
    animation: neon-text 1.5s ease-in-out infinite alternate;
  }

  .technologies-content {
    color: #00ffff; 
    line-height: 1.6;
    text-align: center;
    text-shadow: 0 0 5px #00ffff, 0 0 10px #00ffff, 0 0 15px #00ffff;
  }

  .tech-item {
    display: inline-block;
    margin: 0.5rem 1rem;
    padding: 0.5rem;
    border-radius: 5px;
    color: #00ffff;
    text-shadow: 0 0 5px #00ffff, 0 0 10px #00ffff, 0 0 15px #00ffff;
  }

  .tech-logo {
    width: 30px;
    height: 30px;
    animation: glow-logo 1.5s ease-in-out infinite alternate;
  }

</style>
  
<main class="about-container">
    <div class="about-title">ABOUT ME</div>
    <div class="about-content">
      <p>My name is Jean, I am passionate about technology, I like to play with it, I like to read books and mathematics, I am currently a student of systems engineering. </p>
    </div>
</main>

<main class="technologies-container">
    <div class="technologies-section">
        <div class="technologies-title">TECHNOLOGIES</div>
        <div class="technologies-content">
          <div class="technologies-grid">
            <div class="tech-item">
              <img src="/html-5-svgrepo-com.svg" id="html-img" alt="HTML5"class="tech-logo" />
            </div>
            <div class="tech-item">
              <img src="/css-3-svgrepo-com.svg" alt="CSS3" class="tech-logo" />
            </div>
            <div class="tech-item">
              <img src="/javascript-svgrepo-com.svg" alt="JavaScript" class="tech-logo" />
            </div>
            <div class="tech-item">
              <img src="/docker-svgrepo-com.svg" alt="Docker" class="tech-logo" />
            </div>
            <div class="tech-item">
              <img src="/node-svgrepo-com.svg" alt="Node.js" class="tech-logo" />
            </div>
            <div class="tech-item">
              <img src="/git-svgrepo-com.svg" alt="Git" class="tech-logo" />
            </div>
            <div class="tech-item">
                <img src="/java-svgrepo-com.svg" alt="Java" class="tech-logo" />
            </div>
            <div class="tech-item">
                <img src="/linux-svgrepo-com.svg" alt="Linux" class="tech-logo" />
            </div>
            <div class="tech-item">
                <img src="/typescript-svgrepo-com.svg" alt="Typescript" class="tech-logo" />
            </div>
            <div class="tech-item">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nestjs/nestjs-original.svg" alt="Nest.js" class="tech-logo" />
            </div>
            <div class="tech-item">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original-wordmark.svg" alt="Postgresql" class="tech-logo" />
            </div>
          </div>
        </div>
      </div>
</main>
  