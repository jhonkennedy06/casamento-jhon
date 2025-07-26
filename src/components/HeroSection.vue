<template>
    <section id="home" class="hero is-fullheight">
        <div class="hero-body">
            <div class="container">
                <div class="box info-box">
                    <p class="is-size-4 has-text-weight-light has-text-centered has-text-grey">
                        Com a bênção de Deus e de nossos pais, nós
                    </p>
                    <h1 class="title is-1 has-text-centered mt-2 mb-4">
                        Dayanne & Jhon Kennedy
                    </h1>
                    <p class="subtitle is-4 has-text-centered has-text-grey">
                        vamos nos casar!
                    </p>
                    <hr />
                    <div class="content has-text-centered">
                        <p class="is-size-5">
                            <strong>Data:</strong> 27 de Setembro de 2025, às 15:30
                        </p>
                        <p class="is-size-5">
                            <strong>Local:</strong> Igreja Matriz São Vicente Ferrer, Formiga/MG
                        </p>
                        <a
                        href="https://maps.app.goo.gl/B9X4z1Vd7Q9XJ6vY6"
                        target="_blank"
                        class="button is-primary is-rounded mt-4"
                        >
                            <span class="icon"><i class="fas fa-map-marker-alt"></i></span>
                            <span>Ver no mapa</span>
                        </a>
                </div>
            </div>
        </div>
        </div>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({ name: 'HeroSection' });
</script>

<style scoped>
.hero-body {
    display: flex;
    align-items: center;
    justify-content: center;
}

.info-box {
    background-color: rgba(255, 255, 255, 0.95);
    max-width: 640px;
    margin: 0 auto;
    border-radius: 8px;
    padding: clamp(1.5rem, 5vw, 2.5rem);
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}

.title.is-1 {
    font-family: 'Cursive', 'Brush Script MT', sans-serif;
    font-size: clamp(3rem, 10vw, 4.5rem);
    color: var(--emerald-green) !important;
}
</style>