<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
    <div class="about">
      <h1 cla>{{ msg }}</h1>
    </div>
  </template>
  
