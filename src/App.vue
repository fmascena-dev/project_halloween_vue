<script setup lang="ts">
import Costumes from './components/Costumes.vue';
import Events from './components/Events.vue';
import Footer from './components/Footer.vue';
import FormAttendance from './components/FormAttendance.vue';
import Header from './components/Header.vue';

</script>

<template>
  <Header />
  <Events />
  <Costumes />
  <FormAttendance />
  <Footer />
</template>

<style scoped>
@import './style.css';
</style>
