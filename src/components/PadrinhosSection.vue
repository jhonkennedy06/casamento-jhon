<template>
    <section id="padrinhos" class="section">
        <div class="container">
        <div class="box content-box">
            <h2 class="title is-2 has-text-centered">Nossos Padrinhos</h2>
            <p class="subtitle is-5 has-text-centered">
            Ao nosso lado, teremos pessoas que são mais do que amigos e familiares: são a representação do amor e do apoio que nos trouxeram até aqui. A vocês, nossa eterna gratidão.
            </p>
            <div class="columns is-centered is-multiline mt-5">
            <div class="column is-one-quarter-desktop is-half-tablet has-text-centered">
                <figure class="image is-128x128 is-inline-block">
                <img class="is-rounded" src="https://bulma.io/assets/images/placeholders/128x128.png">
                </figure>
                <p class="title is-5 mt-2">Nome do Padrinho</p>
                <p class="subtitle is-6">Nome da Madrinha</p>
            </div>
            </div>
        </div>
        </div>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({ name: 'PadrinhosSection' });
</script>

<style scoped>
.content-box {
    padding: 2.5rem;
    background-color: rgba(255, 255, 255, 0.95);
    border-radius: 8px;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}
</style>