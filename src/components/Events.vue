<template>
    <section class="flex flex-col items-center gap-6 py-10 px-3 ">
        <h2 class="text-6xl m-5">Detalhes do Evento</h2>

        <CardEvents />
        
    </section>
</template>

<script lang="ts" setup>
import CardEvents from './Cards/CardEvents.vue';

</script>

<style scoped>
h2 {
    font-family: var(--font-title);
    background-image: linear-gradient(355deg, rgba(115, 46, 184, 1) 30%, rgba(240, 110, 66, 1) 80%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    color: transparent;
  }
</style>