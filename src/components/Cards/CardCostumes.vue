<template>
    <div class="flex gap-6 flex-wrap mt-5 w-[95%] items-center justify-center">
      <Card
        v-for="item in cardFantasy"
        :key="item.title"
        class="flex flex-col border border-gray-800 bg-[#111111] p-2 items-center justify-center rounded-xl w-[169px]"
      >
        <CardHeader>
          <img :src="item.icon" :alt="item.title" width="45px" />
        </CardHeader>
        <CardTitle class="text-2xl font-bold text-center">{{ item.title }} </CardTitle>
        <CardFooter class="text-gray-600 text-sm text-center mt-1"> {{ item.footer }} </CardFooter>
      </Card>
    </div>
</template>

<script setup lang="ts">
import type { CardItemCostumes } from '../models/Halloween.interface';
import Card from '../ui/card/Card.vue';
import CardFooter from '../ui/card/CardFooter.vue';
import CardHeader from '../ui/card/CardHeader.vue';
import CardTitle from '../ui/card/CardTitle.vue';

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

<style>
h3 {
  color: #f06e42;
  font-size: 24px;
  font-weight: 700;
}
</style>