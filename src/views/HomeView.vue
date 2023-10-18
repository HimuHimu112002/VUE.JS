<script>
import HeroSection from '../components/HeroSection.vue';
import MenuBar from '../components/MenuBar.vue';
import NameBuilder from '../components/NameBuilder.vue';
export default {
  components: {
    MenuBar,
    HeroSection,
    NameBuilder
},
};
</script>

<template>
  <main>
    <MenuBar/>
    <HeroSection></HeroSection>
    <NameBuilder></NameBuilder>
    <HomePage></HomePage>
  </main>
</template>