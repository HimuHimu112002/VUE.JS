<script>
  import CardComponents from '../components/CardComponents.vue';
  export default {
  components: {
    CardComponents
  },
  data() {
    return {
      title: 'Hello from the parent!',
      discription: "Hello bangladesh card body"
    };
  },
};
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    <TestView/>
    <CardComponents :title="title" :discription="discription"/>
    <CardComponents :title="title" :discription="discription"/>

  </div>
</template>
