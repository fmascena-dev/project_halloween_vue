<template>
  <section class="bg-[#402659] mt-5 flex flex-col items-center justify-center gap-6 h-[780px]">
    <div class="flex flex-col items-center gap-6">
      <h2 class="text-6xl m-5">Inspirações de Fantasias</h2>
      <p class="text-xl">
        Solte sua criatividade e venha caracterizado! Aqui estão algumas ideias para você arrasar na
        festa.
      </p>
    </div>

    <div class="flex gap-6 flex-wrap mt-5 w-[95%] items-center justify-center">
      <Card
        v-for="item in cardFantasy"
        :key="item.title"
        class="flex flex-col border border-gray-800 bg-[#111111] p-3 items-center justify-center rounded-xl w-[169px] h-[170px]"
      >
        <CardHeader>
          <img :src="item.icon" :alt="item.title" width="40px" />
        </CardHeader>
        <CardTitle class="text-2xl font-bold text-center">{{ item.title }} </CardTitle>
        <CardFooter class="text-gray-600 text-sm text-center mt-1"> {{ item.footer }} </CardFooter>
      </Card>
    </div>

    <div
      class="bg-[#211E1C80] w-[95%] h-[206px] mt-9 border border-[#F06E4233] rounded-lg flex flex-col items-center justify-center gap-3"
    >
      <h3>🏆 Concurso de Fantasias!</h3>
      <p class="text-[#BEB4A7] m-2">Melhor fantasia ganha um prêmio especial! Prepare-se para competir.</p>
      <Button
        variant="default"
        class="flex gap-2 border-none hover:cursor-pointer items-center justify-center p-5"
      >
        <img src="/camera.svg" alt="camera" width="20px" />
        <p>ENVIAR FANTASIA</p>
      </Button>
    </div>
  </section>
</template>

<script setup lang="ts">
import type { CardItemCostumes } from './models/Halloween.interface'
import Card from './ui/card/Card.vue'
import CardFooter from './ui/card/CardFooter.vue'
import CardHeader from './ui/card/CardHeader.vue'
import CardTitle from './ui/card/CardTitle.vue'
import Button from './ui/button/Button.vue'

const cardFantasy: CardItemCostumes[] = [
  {
    icon: '/dracula.png',
    title: 'Vampiro',
    footer: 'Clássico e elegante',
  },
  {
    icon: '/witch.png',
    title: 'Bruxa',
    footer: 'Misteriosa e poderosa',
  },
  {
    icon: '/ghost.png',
    title: 'Fantasma',
    footer: 'Assustador e simples',
  },
  {
    icon: '/zumbi.png',
    title: 'Zumbi',
    footer: 'Morto-vivo faminto',
  },
  {
    icon: '/clown.png',
    title: 'Palhaço',
    footer: 'Terrível e divertido',
  },
  {
    icon: '/werewolf.png',
    title: 'Lobisomem',
    footer: 'Selvagem e feroz',
  },
]
</script>

<style scoped>
h2 {
  font-family: var(--font-title);
  background-image: linear-gradient(355deg, rgba(115, 46, 184, 1) 40%, rgba(240, 110, 66, 1) 80%);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  color: transparent;
}

h3 {
  color: #f06e42;
  font-size: 24px;
  font-weight: 700;
}
</style>
