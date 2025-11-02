<template>
    <header>
        <h1 class="text-[150px]">HALLOWEEN</h1>
        <p class="text-5xl font-bold">PARTY 2025</p>
        <p class="text-gray-400 text-4xl uppercase font-bold">Prepare-se para a noite mais assombrada do ano!</p>

        <div class="uppercase flex gap-4">
            <Button variant="default" class="flex gap-2 border-none hover:cursor-pointer items-center p-5">
                <img src="/mask.png" alt="Confirmar presença" width="20px">
                Confirmar Presença
            </Button>
            <Button variant="default" class="flex gap-2 border-none hover:cursor-pointer items-center justify-center p-5">
                <img src="/ghost.png" alt="Adicionar ao calendário" width="20px">
                Ver detalhes
            </Button>
        </div>

        <img src="/pumpkin.png" alt="abobora" class="absolute top-1/6 left-30 w-14" />
        <img src="/batman.png" alt="morcego" class="absolute top-1/6 right-30 w-14" />
        <img src="/ghost.png" alt="fantasma" class="absolute bottom-1 left-1/12 w-14" />
        <img src="/clown.png" alt="palhaço" class="absolute bottom-1 right-25 w-32" />
    </header>
</template>

<script setup lang="ts">
import Button from './ui/button/Button.vue';


</script>

<style lang="scss">
@use '@/styles/_header.scss';
</style>