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

    .card {
        padding: 1.5rem;
        border-radius: 10px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        transition: transform 0.3s ease, box-shadow 0.3s ease;
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        width: 100%;
        max-width: 300px;
        margin: 10px;
    }

    .card:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 16px rgba(240, 238, 238, 0.3);
    }

    .card h2 {
        font-size: 1.5rem;
        font-weight: bold;
        color: #00ffff70;
        margin-bottom: 1rem;
        text-shadow: 0 0 5px #0f4444, 0 0 10px #00ffff, 0 0 15px #00ffff;
    }

    .card p {
        font-size: 1rem;
        color: #d6d3d3;
        margin-bottom: 1rem;
    }

    .tech-item {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 0.5rem;
        margin-bottom: 1rem;
    }

    .tech-logo {
        width: 40px;
        height: 40px;
        animation: glow-logo 1.5s ease-in-out infinite alternate;
    }

    .card a {
        display: inline-block;
        padding: 0.5rem 1rem;
        background-color: #00ffff;
        color: #ebd61c;
        text-decoration: none;
        border-radius: 5px;
        font-weight: bold;
        transition: background-color 0.3s ease;
    }

    .card a:hover {
        background-color: #ff00ff7c;
        color: #fff;
    }

</style>

<div class="organizer">
    <div class="card">
        <h2>{title}</h2>
        <div class="tech-item">
            {#each imageUrls as imageUrl}
                <img src={imageUrl} class="tech-logo" />
            {/each}
        </div>
        <p>{description}</p>
        <a href={link} target="_blank">View Project</a>
    </div>
</div>