<template>
    <section id="historia" class="section">
        <div class="container">
        <div class="box content-box">
            <h2 class="title is-2 has-text-centered">Nossa História</h2>
            <div class="columns is-vcentered mt-4">
            <div class="column is-half">
                <div class="content is-medium">
                <p>Nossos caminhos se cruzaram pela primeira vez em 2015, na simplicidade e na fé do grupo de jovens da S.S.V.P. O tempo nos levou por direções diferentes, mas o destino já havia traçado seus planos. Anos depois, em 2017, uma conversa despretensiosa sobre um status nas redes sociais se transformou em um convite: um cinema, apenas como amigos.</p>
                <p>Na noite de 15 de setembro, o inesperado aconteceu. Um problema com o vidro do carro se tornou o cenário perfeito para o nosso primeiro beijo, um momento que selou o início de tudo. Entre beijos roubados e uma pipoca disputada de brincadeira durante o filme (do qual mal lembramos a história!), sentimos que algo especial nascia ali.</p>
                <p>Enfrentamos juntos os altos e baixos da vida. A distância surgiu como um desafio, testando nossa força e nosso amor, que se mantiveram firmes a cada reencontro. E então, no dia 7 de setembro de 2024, veio o pedido que mudaria nossas vidas para sempre.</p>
                <p>Com a certeza no coração e os sonhos alinhados, decidimos que era a hora. A hora de unir nossas vidas em um só caminho. Agora, convidamos vocês para celebrar conosco o início do nosso 'felizes para sempre'.</p>
            </div>
            </div>
                <div class="column is-half">
                    <figure class="image is-3by4">
                    <img
                        class="image-cover"
                        src="@/assets/nossahistoria.png"
                        alt="Foto do casal Dayanne e Jhon"
                    >
                    </figure>
                </div>
            </div>
        </div>
        </div>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({ name: 'HistoriaSection' });
</script>

<style scoped>
.content-box {
    padding: 2.5rem;
    background-color: rgba(255, 255, 255, 0.95);
    border-radius: 8px;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}

.content p {
  color: var(--text-color);
}
</style>