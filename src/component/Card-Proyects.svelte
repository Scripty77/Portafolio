<script>
    export let title = "Project Title";
    export let description = "Project Description";
    export let imageUrls = ["/default-image.svg"]; // Array of image URLs
    export let link = "#"; // Default link
</script>
  
<style>
    .organizer {
        display: flex;
        flex-wrap: wrap; /* Permite que las tarjetas se ajusten a la siguiente línea si es necesario */
        justify-content: flex-start; /* Alinea las tarjetas a la izquierda */
        padding: 10px;
    }

    .about-container {
        background-color: rgba(5, 14, 4, 0.466);
        padding: 1rem;
        box-shadow: 0 0 10px rgba(180, 219, 5, 0.904);
        width: 30%;
        margin: 10px; /* Añade un margen para separar las tarjetas */
        animation: neon 1.5s ease-in-out infinite alternate;
    }

    .tech-logo {
        width: 40px;
        height: 40px;
        animation: glow-logo 1.5s ease-in-out infinite alternate;
    }

    .about-container a {
        text-decoration: none;
        color: inherit;
    }
</style>

<div class="organizer">
    <div class="about-container">
        <a href={link} target="_blank">
            <h2>{title}</h2>
            <div class="tech-item">
                {#each imageUrls as imageUrl}
                    <img src={imageUrl} class="tech-logo" />
                {/each}
            </div>
            <p>{description}</p>
        </a>
    </div>
</div>