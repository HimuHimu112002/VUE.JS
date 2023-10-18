<script>
  import CardComponents from '../components/CardComponents.vue';
  export default {
  components: {
    CardComponents
  },
  data() {
    return {
      title: 'Bangladesh',
      discription: "Hello bangladesh card body",

      title2: 'India',
      discription2: "Hello bangladesh card body",
    };
  },
};
</script>

<template>
  <div class="about">
    <CardComponents :title="title" :discription="discription"/>
    <CardComponents :title="title2" :discription="discription2"/>
  </div>
</template>
