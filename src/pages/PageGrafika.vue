<script setup>
import Grafika from '@/components/Grafika.vue'
const prop = defineProps(["activeLink"])
</script>


<template>

  <Grafika
  :active-link="activeLink"
  />

</template>