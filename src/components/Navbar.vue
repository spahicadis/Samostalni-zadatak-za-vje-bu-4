<script setup>
import LinkItem from '@/components/LinkItem.vue'
const activeLinkProp = defineProps(["activeLink"])
const emit = defineEmits(["promjenaActive"])
 const handleActive = (e) => {
        emit('promjenaActive', e)
    }

//Drugi emit, nosimo podatak od prvog emita
</script>



<template>
 <nav class="sticky top-0 w-full flex gap-4 flex-wrap items-center justify-around bg-[#070F2B]/25 backdrop-blur-sm py-2 px-8 rounded-lg">
  <LinkItem
  :active-link="activeLink"
  @promjenaActive="handleActive"
  />                
</nav>
</template>