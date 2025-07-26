<template>
  <section id="padrinhos" class="section">
    <div class="container">
      <div class="box content-box">
        <h2 class="title is-2 has-text-centered">Nossos Padrinhos</h2>
        <p class="subtitle is-5 has-text-centered">
          Ao nosso lado, teremos pessoas que são mais do que amigos e familiares: são a representação do amor e do apoio que nos trouxeram até aqui. A vocês, nossa eterna gratidão.
        </p>

        <div class="columns is-multiline is-centered is-mobile mt-5">
          <div
            v-for="(padrinho, index) in padrinhos"
            :key="index"
            class="column is-one-sixth-desktop is-one-quarter-tablet is-half-mobile has-text-centered"
            @click="openModal(padrinho)"
            style="cursor: pointer;"
          >
            <figure class="image is-inline-block padrinho-figure">
              <img
                class="is-rounded padrinho-img"
                :src="require(`@/assets/padrinhos/${padrinho.img}`)"
                :alt="padrinho.nome"
              />
            </figure>
            <p class="title is-6 mt-2">{{ padrinho.nome }}</p>
          </div>
        </div>
      </div>
    </div>

    <div class="modal" :class="{ 'is-active': isModalActive }">
      <div class="modal-background" @click="closeModal"></div>
      <div class="modal-content" v-if="selectedPadrinho">
        <div class="box modal-box has-text-centered">
          <figure class="image">
            <img :src="require(`@/assets/padrinhos/${selectedPadrinho.img}`)" :alt="selectedPadrinho.nome" class="modal-image">
          </figure>
          <h3 class="title is-4 mt-4">{{ selectedPadrinho.nome }}</h3>

          <button class="button is-primary is-rounded mt-4" @click="closeModal">
            Fechar
          </button>
        </div>
      </div>
      <button class="modal-close is-large" aria-label="close" @click="closeModal"></button>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

interface Padrinho {
  nome: string;
  img: string;
}

function normalizeName(name: string): string {
  return name
    .normalize('NFD')
    .replace(/[\u0300-\u036f]/g, '')
    .replace(/\s+/g, '')
    .toLowerCase() + '.png';
}

export default defineComponent({
  name: 'PadrinhosSection',
  data() {
    const nomes: string[] = [
      'Elenice', 'Cristiano', 'Paulina', 'Carlo', 'Helena', 'Tiãozinho',
      'Terezinha', 'Diego', 'Jheneffer', 'Dieneson', 'Edivan', 'Waniely',
      'Ariane', 'César', 'Luiz', 'Glenda', 'Érika', 'Thalisson',
      'Jennifer', 'Giovanne', 'Thales', 'Alexandre', 'Thalise',
      'Quinzinho', 'Júnior', 'Ariele', 'Jhonathan',
    ];
    const padrinhos: Padrinho[] = nomes.map(nome => ({
      nome,
      img: normalizeName(nome),
    }));
    return {
      padrinhos,
      isModalActive: false,
      selectedPadrinho: null as Padrinho | null,
    };
  },
  methods: {
    openModal(padrinho: Padrinho) {
      this.selectedPadrinho = padrinho;
      this.isModalActive = true;
    },
    closeModal() {
      this.isModalActive = false;
    },
  },
});
</script>

<style scoped>
.content-box {
  padding: 2.5rem;
  background-color: rgba(255, 255, 255, 0.95);
  border-radius: 8px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}

.padrinho-img {
  width: 80px;
  height: 80px;
  object-fit: cover;
}

.padrinho-figure {
  width: 80px;
  height: 80px;
  margin: 0 auto;
}

.modal-box {
  background-color: white;
  border-radius: 8px;
  padding: 1.5rem;
  display: inline-block;
}

.modal-image {
  max-width: 400px;
  max-height: 70vh;
  width: auto;
  height: auto;
  border-radius: 6px;
}

.modal-content {
  max-width: 90vw;
}

@media screen and (max-width: 768px) {
  .modal-content {
    padding: 20px;
    width: 100%;
  }

  .modal-box {
    padding: 1.25rem;
  }

  .modal-image {
    max-width: 100%;
  }

  .title.is-4 {
    font-size: 1.5rem;
  }
}
</style>