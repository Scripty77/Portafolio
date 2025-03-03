<script>
// @ts-nocheck
import About from './component/About.svelte';
import Contact from "./component/Contact.svelte";
import Proyect from "./component/Proyect.svelte";
import Home from "./component/Home.svelte";

let currentComponent = Home; // Componente inicial

function handleNavigation(component) {
  currentComponent = component;
}
</script>

<main>
  <header class="header">
    <div class="header__left">
      <img class="nes-atari" src="/game.png" alt="atari" />
      <span class="site-title glitch">WELCOME A CYBERIA</span>
    </div>
    <div class="header__right neon">Cafe & Club</div>
  </header>
  <!-- Navigation Sidebar -->
  <div class="sidebar">
    <div class="sidebar__title">NAVIGATION.EXE</div>

    <nav class="sidebar__nav">
      <!-- svelte-ignore a11y_missing_attribute -->
      <a class:sidebar__link--active={currentComponent === Home} on:click={() => handleNavigation(Home)} on:keydown={(e) => e.key === 'Enter' && handleNavigation(Home)}>
      <img class="pc" src="/computer.png" alt="pc" />
        <span>HOME</span>
      </a>
      <!-- svelte-ignore a11y_missing_attribute -->
      <a class:sidebar__link--active={currentComponent === About} on:click={() => handleNavigation(About)} on:keydown={(e) => e.key === 'Enter' && handleNavigation(About)}>
        <img class="user" src="/computer-window.png" alt="user" />
        <span>ABOUT</span>
      </a>

      <!-- svelte-ignore a11y_missing_attribute -->
      <a class="sidebar__link" role="button" tabindex="0" on:click={() => handleNavigation('Proyect')} on:keydown={(e) => e.key === 'Enter' && handleNavigation('Proyect')}>
        <img class="disc" src="/floppy-disc.png" alt="disc" />
        <span>PROJECTS</span>
      </a>

      <!-- svelte-ignore a11y_missing_attribute -->
      <a class="sidebar__link">
        <img class="phone" src="/flip-phone.png" alt="phone" />
        <span>CONTACT</span>
      </a>
    </nav>
  </div>

  <!-- Main Content -->
   
  <div class="main-content">
    <div class="display-title">DISPLAY.SYS</div>
    {#if currentComponent}
    <svelte:component this={currentComponent} />
    {/if}
  </div>
</main>

<style>
  /*estilos css*/
  /* header */
  .header {
    position: absolute;
    top: 13%;
    left: 120px;
    width: 77%;
    border: 4px solid rgba(255, 0, 255, 0.452);
    padding: 30px;
    display: flex;
    justify-content: space-between;
    background-color: rgba(5, 14, 4, 0.466);
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    z-index: 10;
    animation: neon 1.5s ease-in-out infinite alternate;
  }

  .header__left,
  .header__right {
    display: flex;
    align-items: center;
  }

  .header__left {
    gap: 10px;
  }

  .nes-atari {
    width: 40px;
    height: auto;
  }

  .site-title {
    font-size: 2rem;
    font-weight: bold;
  }

  .header__right {
    font-size: 1.25rem;
    font-weight: bold;
  }

  .glitch {
    position: relative;
    color: white;
    font-family: sans-serif;
    font-weight: 800;
    font-size: 2rem;
  }

  .glitch::before,
  .glitch::after {
    content: "WELCOME A CYBERIA";
    position: absolute;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.507);
    overflow: hidden;
    top: 0;
  }

  .glitch::before {
    left: 3px;
    text-shadow: -2px 0 red;
    animation: glitch-animation-1 2s linear infinite reverse-alternate;
  }

  .glitch::after {
    left: -3px;
    text-shadow: -2px 0 blue;
    animation: glitch-animation-2 2s linear infinite reverse-alternate;
  }

  @keyframes glitch-animation-1 {
    0%,
    100% {
      clip: rect(0, 9999px, 9999px, 0);
    }
    10%,
    30%,
    50%,
    70%,
    90% {
      clip: rect(random(150) + px, 350px, random(150) + px, 30px);
    }
  }

  @keyframes glitch-animation-2 {
    0%,
    100% {
      clip: rect(0, 9999px, 9999px, 0);
    }
    10%,
    30%,
    50%,
    70%,
    90% {
      clip: rect(random(150) + px, 350px, random(150) + px, 30px);
    }
  }

  .nes-atari {
    width: 40px;
    height: 40px;
  }

  /*sidebar*/
  .sidebar {
    left: 120px;
  }

  .header__left,
  .header__right {
    display: flex;
    align-items: center;
  }

  .site-title {
    color: #ff00ff;
    font-size: 1.25rem;
    font-weight: bold;
    letter-spacing: 10px;
  }

  .header__right {
    color: #00ffff;
    font-size: 0.875rem;
  }

  .sidebar {
    position: absolute;
    top: 25%;
    width: 100%;
    height: 40rem;
    max-width: 300px;
    border: 4px solid rgba(255, 0, 255, 0.432);
    background-color: rgba(5, 14, 4, 0.507);
    padding: 16px;
    animation: neon 1.5s ease-in-out infinite alternate;
  }

  .sidebar__title {
    color: #00ffff;
    margin-bottom: 16px;
  }

  .sidebar__nav {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  .sidebar__link {
    display: flex;
    align-items: center;
    gap: 20px;
    padding: 12px;
    border-radius: 8px;
    color: #b0b0b0;
    transition:
      background-color 0.3s,
      color 0.3s;
  }

  .pc {
    width: 24px;
    height: 24px;
  }

  .user {
    width: 24px;
    height: 24px;
  }

  .disc {
    width: 24px;
    height: 24px;
  }

  .phone {
    width: 24px;
    height: 27px;
  }

  .sidebar__link:hover,
  .sidebar__link--active {
    background-color: rgba(58, 10, 58, 0.5);
    color: #ff00ff;
  }

  /*main content*/
  .main-content {
    position: absolute;
    border: 4px solid rgba(255, 0, 255, 0.363);
    background-color: rgba(5, 14, 4, 0.466);
    padding: 10px;
    width: 58%;
    top: 25%;
    left: 480px;
    font-size: 1rem;
    height: 41rem;
    animation: neon 5.5s ease-in-out infinite alternate;
  }

  .display-title {
    color: #00ffff; /* Color cyan */
    margin-bottom: 16px; /* Espacio inferior */
  }

  @keyframes pulse {
    0%,
    100% {
      opacity: 1;
    }
    50% {
      opacity: 0.5;
    }
  }

  @keyframes neon {
    10% {
      text-shadow:
        0 0 5px #a00202,
        0 0 10px #c20c0c,
        0 0 20px #ff00ff,
        0 0 30px #ff00ff,
        0 0 40px #ff00ff,
        0 0 50px #ff00ff,
        0 0 60px #ff00ff;
    }
    100% {
      text-shadow:
        0 0 10px #fff,
        0 0 10px #ff00ff,
        0 0 10px #ff00ff,
        0 0 10px #ff00ff,
        0 0 10px #ff00ff,
        0 0 10px #ff00ff,
        0 0 10px #ff00ff;
    }
  }

  nav a {
        margin-right: 10px;
        cursor: pointer;
  }
</style>
