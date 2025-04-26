<script setup>
  const activeLinkProp = defineProps(["activeLink"])
  
  const links = [
        { name: "POČETNA", active: true},
        { name: "SLIKA", active: true},
        { name: "ZVUK", active: false},
        { name: "GRAFIKA", active: true},
        { name: "MODEL", active: false},
        { name: "VIDEO", active: false}
    ];
//Prvi emit krece iz template za promjenu aktivnog
</script>

<template>
<div v-for="link in links" class="text-sm z-10 relative transition" @click="$emit('promjenaActive', link.name)"
                        :class="[link.name == activeLink ? 'underline text-purple-100' : 'cursor-pointer text-indigo-300 text-sm hover:text-indigo-200 hover:scale-105', 
                            link.active ? '' : 'text-indigo-500/50 text-sm pointer-events-none font line-through']">
                    {{ link.name }} 
                    <b v-if="link.name == activeLink" class="text-purple-400 -z-[5] absolute -left-0.5 blur-sm">
                        {{ link.name }}
                    </b>
                </div>
</template>