<template>
  <section class="flex gap-5">
    <Card
      class="flex flex-col gap-3 border border-gray-800 bg-[#111111] p-3 items-center justify-center rounded-xl w-[259px] h-[194px]"
    >
      <CardHeader>
        <img src="/calendar.svg" alt="calendar icon" />
      </CardHeader>
      <CardDescription>
        <p class="text-gray-600 text-lg">Data</p>
      </CardDescription>
      <CardTitle class="text-2xl font-bold"> 31 de Outubro </CardTitle>
      <CardFooter class="text-gray-600 text-sm"> Quinta-feira </CardFooter>
    </Card>

    <Card
      class="flex flex-col gap-3 border border-gray-800 bg-[#111111] p-3 items-center justify-center rounded-xl w-[259px] h-[194px]"
    >
      <CardHeader>
        <img src="/clock.svg" alt="clock icon" />
      </CardHeader>
      <CardDescription>
        <p class="text-gray-600 text-lg">Horário</p>
      </CardDescription>
      <CardTitle class="text-2xl font-bold"> 20:00 - 02:00 </CardTitle>
      <CardFooter class="text-gray-600 text-sm"> 6h de terror </CardFooter>
    </Card>

    <Card
      class="flex flex-col gap-3 border border-gray-800 bg-[#111111] p-3 items-center justify-center rounded-xl w-[259px] h-[194px]"
    >
      <CardHeader>
        <img src="/map.svg" alt="map icon" />
      </CardHeader>
      <CardDescription>
        <p class="text-gray-600 text-lg">Local</p>
      </CardDescription>
      <CardTitle class="text-2xl font-bold"> Cassa Assombrada </CardTitle>
      <CardFooter class="text-gray-600 text-sm"> Rua do Medo, 666 </CardFooter>
    </Card>

    <Card
      class="flex flex-col gap-3 border border-gray-800 bg-[#111111] p-3 items-center justify-center rounded-xl w-[259px] h-[194px]"
    >
      <CardHeader>
        <img src="/peoples.svg" alt="peoples icon" />
      </CardHeader>
      <CardDescription>
        <p class="text-gray-600 text-lg">Dress Code</p>
      </CardDescription>
      <CardTitle class="text-2xl font-bold"> Fantasias </CardTitle>
      <CardFooter class="text-gray-600 text-sm"> Obrigatório! </CardFooter>
    </Card>
  </section>
</template>

<script setup lang="ts">
import Card from '../ui/card/Card.vue'
import CardDescription from '../ui/card/CardDescription.vue'
import CardFooter from '../ui/card/CardFooter.vue'
import CardHeader from '../ui/card/CardHeader.vue'
import CardTitle from '../ui/card/CardTitle.vue'
</script>

<style></style>
