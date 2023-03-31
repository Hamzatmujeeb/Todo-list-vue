<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
   <h2 class="title">
        Create Todo List
      </h2>
</template>

<style scoped>
.title {
  text-align: center;
  margin-bottom: 1rem;
  color: salmon;
  font-size: 1rem;
}
</style>
