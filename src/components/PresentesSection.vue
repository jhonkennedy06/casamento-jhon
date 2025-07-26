<template>
    <section id="presentes" class="section">
        <div class="container">
        <div class="box content-box">
            <h2 class="title is-2 has-text-centered">Lista de Presentes</h2>
            <p class="subtitle is-5 has-text-centered">
                Sua presença é o nosso maior presente, mas se desejar nos presentear com algo para o nosso novo lar, ficaremos imensamente felizes.
            </p>

            <div class="columns is-centered mt-4">
                <div class="column is-two-thirds">
                    <div class="content ">
                    <p><strong><h4>Quer nos presentear mas ficou na dúvida se já temos o item? Veja na lista abaixo o que já temos:</h4></strong></p>
                    <ul>
                        <li><span class="icon has-text-success"><i class="fas fa-check-circle"></i></span> Liquidificador</li>
                        <li><span class="icon has-text-success"><i class="fas fa-check-circle"></i></span> Máquina de Lavar</li>
                        <li><span class="icon has-text-success"><i class="fas fa-check-circle"></i></span> Micro-ondas</li>
                        <li><span class="icon has-text-success"><i class="fas fa-check-circle"></i></span> Airfryer</li>
                    </ul>
                    </div>
                </div>
            </div>

            <div class="has-text-centered mt-5">
                <a href="https://www.finalfeliz.de/dayanne-jhon-kennedy"  target="_blank" class="button is-primary is-large is-rounded">
                    <span class="icon"><i class="fas fa-gift"></i></span>
                    <span>Acessar Lista Online</span>
                </a>
            </div>
        </div>
    </div>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({ name: 'PresentesSection' });
</script>

<style scoped>
.content-box {
    padding: 2.5rem;
    background-color: rgba(255, 255, 255, 0.95);
    border-radius: 8px;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}
.content ul {
    list-style: none;
    margin-left: 0;
}
.content li {
    font-size: 1.25rem;
    padding: 0.5rem 0;
}
.content li .icon {
    margin-right: 10px;
}
</style>