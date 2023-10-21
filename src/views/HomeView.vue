<script>
import HeroSection from '../components/HeroSection.vue';
import MenuBar from '../components/MenuBar.vue';
export default {
  components: {
    MenuBar,
    HeroSection,
},
};
</script>

<template>
  <main>
    <MenuBar/>
    <HeroSection></HeroSection>
    <HomePage></HomePage>
  </main>
</template>