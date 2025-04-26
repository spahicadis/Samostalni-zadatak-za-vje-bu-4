<script setup>
    import Header from '@/components/Header.vue'
    import PagePocetna from '@/pages/PagePocetna.vue'
    import PageSlika from '@/pages/PageSlika.vue'
    import PageGrafika from '@/pages/PageGrafika.vue'
    import Footer from '@/components/Footer.vue'
    import { ref } from 'vue'
    const activeLink = ref("POČETNA");
    const handleActive = (e) => {
        activeLink.value = e;
    }
//Zadnji emit, mijenjamo activeLink!
</script>

<template>
    <div class="fixed w-full h-full flex justify-center poppins text-sm text-indigo-300
        bg-gradient-to-b from-[#1B1A55] via-[#2B428D] to-[#3B39BB]">

        <div style="background-image: url('./src/assets/images/pattern.jpg'); 
            background-size: 200px;"
            class="fixed w-full h-full bg-repeat opacity-[3%] -z-10"></div>

        <div class="bg-[#535C91]/25 border-x border-[#9290C3]/10 w-[700px] max-w-[700px] shadow-lg
            flex flex-col justify-between px-8 gap-4 overflow-auto">
         <Header
         :active-link="activeLink"
         @promjenaActive="handleActive"
         />
        <PagePocetna
        :active-link="activeLink"
        />
        <PageSlika
        :active-link="activeLink"
        />
        <PageGrafika
        :active-link="activeLink"
        />
        <Footer/>
        </div>
    </div>
</template>