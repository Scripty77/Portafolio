<script>
</script>

<style>
    .contact-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 20px;
        color: #fff;
        border-radius: 10px;
        box-shadow: 0 0 20px rgba(0, 255, 255, 0.5);
        gap: 1rem;
    }

    h1 {
        font-family: 'Courier New', Courier, monospace;
        font-size: 2.5rem;
        margin-bottom: 20px;
        text-shadow: 0 0 10px #00ffff, 0 0 20px #00ffff, 0 0 30px #00ffff;
    }

    p {
        font-family: 'Courier New', Courier, monospace;
        font-size: 1.2rem;
        margin-bottom: 20px;
    }

    .contact-link {
        display: flex;
        align-items: center;
        margin: 10px;
        font-size: 1.5rem;
        text-decoration: none;
        color: #00ffff; /* Color para los enlaces */
        font-family: 'Courier New', Courier, monospace;
        text-shadow: 0 0 5px #00ffff, 0 0 10px #00ffff;
        transition: color 0.3s ease, text-shadow 0.3s ease;
    }

    .contact-link:hover {
        color: #ff00ff;
        text-shadow: 0 0 10px #ff00ff, 0 0 20px #ff00ff;
    }

    .contact-link.github {
        color: #ff00ff; /* Color para GitHub */
        text-shadow: 0 0 5px #ff00ff, 0 0 10px #ff00ff;
    }

    .contact-link.github:hover {
        color: #00ffff;
        text-shadow: 0 0 10px #00ffff, 0 0 20px #00ffff;
    }

    .contact-link img {
        margin-right: 10px;
        width: 40px;
        height: 40px;
    }
</style>

<div class="contact-container">
    <h2>Connect with me on:</h2>
    <a class="contact-link" href="https://www.linkedin.com/in/jean-carlos-contreras-485485279/" target="_blank">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" alt="LinkedIn">
        LinkedIn
    </a>
    <a class="contact-link github" href="https://github.com/Scripty77" target="_blank">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/githubcodespaces/githubcodespaces-original.svg" alt="GitHub">
        GitHub
    </a>
</div>
