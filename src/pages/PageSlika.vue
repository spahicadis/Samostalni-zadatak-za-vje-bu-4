<script setup>
import Slika from '@/components/Slika.vue'
const prop = defineProps(["activeLink"])
</script>


<template>

  <Slika
  :active-link="activeLink"
  />

</template>