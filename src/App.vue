<!-- App.vue -->

<script setup lang="ts">
import { ref } from 'vue'
import MyComponent from './components/MyComponent.vue'

const id = ref({ id: 'myId' })
</script>

<template>
  <div :="id" />

  <MyComponent>
    <template #default="{ props }">
      <div :="props" />
    </template>
  </MyComponent>

  <MyComponent #="{ props }">
    <div :="props" />
  </MyComponent>
</template>
