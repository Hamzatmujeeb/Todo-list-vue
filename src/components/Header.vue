<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
   <header class="wrapper">
      <h1 class="title">
        Todo List v1
      </h1>
    </header>
</template>

<style scoped>
.title {
  text-align: center;
  margin-bottom: 1rem;
  color: salmon;
  font-size: 2.5rem;
}
</style>
