<script>
</script>

<style>
   
  .about-container {
      position: relative;
      background-color: rgb(5, 78, 5);
      width: 100%;
      height: 470px;
      font-family: 'VT323', monospace;
  }

  .tech-logo {
    width: 60px;
    height: 60px;
  }

  .tech-item {
    display: flex;
    margin: 4rem 15rem;
    padding: 1rem;
    justify-content: center;
    font-size: 1.5rem;
    gap: 10px;
  }

  #scan, #bezel {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  #scan {
    opacity: 20%;
  }

  .noselect {
    user-select: none;
  }

  #content {
    padding: 10px;
    color: rgba(179, 248, 19, 0.938) ;
    width: 400px;
    margin: 0 auto;
    font-size: 1.4rem;
    text-align: center;
    text-shadow: 1px 1px 2px rgb(228, 230, 126), 0 0 1em rgb(238, 241, 22), 0 0 0.2em rgb(241, 245, 23);
    padding-top: 40px;
  }

</style>


<main class="about-container">
  <!-- svelte-ignore a11y_missing_attribute -->
  <img src="/scanlines.png" id="scan" class="noselect" />
    <!-- svelte-ignore a11y_missing_attribute -->
  <img src="/bezel.png"  id="bezel" class="noselect" />
  <div id="content" class="noselect">
    <h1>WELCOME</h1>
    <img src="/public/cmprops.dll_14_16.ico" id="compu" class="tech-logo" />
    <p>FullStack Developer && Blockhain Estusiasta</p>
  </div>
</main>

<div class="developer">
  <div class="tech-item">
    <p>Developed with </p>
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/svelte/svelte-original.svg" alt="CSS3" class="tech-logo" />
  </div>
</div>

