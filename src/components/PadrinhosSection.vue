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
          >
            <figure class="image is-inline-block padrinho-figure">
              <img
                class="is-rounded padrinho-img"
                :src="require(`@/assets/padrinhos/${padrinho?.img}`)"
                :alt="padrinho?.nome"
              />
            </figure>
            <p class="title is-6 mt-2">{{ padrinho?.nome }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

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
    const nomes = [
      'Elenice',
      'Cristiano',
      'Paulina', 
      'Carlo',
      'Helena', 
      'Tiãozinho',
      'Terezinha', 
      'Diego', 
      'Jheneffer',
      'Dieneson',
      'Edivan', 
      'Waniely',
      'Ariane', 
      'César', 
      'Luiz', 
      'Glenda',
      'Érika', 
      'Talisson', 
      'Jennifer', 
      'Giovanne',
      'Thales', 
      'Alexandre', 
      'Thalise',
      'Quinzinho', 
      'Júnior', 
      'Ariele', 
      'Jhonathan',
    ];

    const padrinhos = nomes.map(nome => ({
      nome,
      img: normalizeName(nome),
    }));

    return { padrinhos };
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

@media (max-width: 768px) {
  .padrinho-img {
    width: 50px;
    height: 50px;
  }

  .padrinho-figure {
    width: 50px;
    height: 50px;
    margin: 0 auto;
  }
}

</style>
