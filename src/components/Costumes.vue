<template>
  <section class="bg-[#402659] mt-5 flex flex-col items-center justify-center gap-6 h-[780px]">
    <div class="flex flex-col items-center gap-6">
      <h2 class="text-6xl m-5">Inspirações de Fantasias</h2>
      <p class="text-xl">
        Solte sua criatividade e venha caracterizado! Aqui estão algumas ideias para você arrasar na
        festa.
      </p>
    </div>

    <CardCostumes />

    <div
      class="bg-[#211E1C80] w-[90%] h-[206px] mt-9 border border-[#F06E4233] rounded-lg flex flex-col items-center justify-center gap-3"
    >
      <h3>🏆 Concurso de Fantasias!</h3>
      <p class="text-[#BEB4A7] m-2 text-lg">Melhor fantasia ganha um prêmio especial! Prepare-se para competir.</p>
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
import Button from './ui/button/Button.vue'
import CardCostumes from './Cards/CardCostumes.vue'
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
