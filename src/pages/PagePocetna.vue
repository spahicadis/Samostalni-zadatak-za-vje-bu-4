<script setup>
import Pocetna from '@/components/Pocetna.vue'
const prop = defineProps(["activeLink"])
</script>


<template>

  <Pocetna
  :active-link="activeLink"
  />

</template>