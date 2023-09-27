<script setup>
const props = defineProps(["resultado"]);
</script>

<template>
  <section class="result p-5 mb-4 mt-4 bg-light rounded-3 text-center">
    <h2>Resultado</h2>
    <h3>{{ props.resultado }}</h3>
  </section>
</template>
