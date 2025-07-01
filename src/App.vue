<script setup>
import {onBeforeMount, onMounted, onBeforeUpdate, onUpdated, onBeforeUnmount, onUnmounted, ref} from 'vue'

const counter = ref(0)

onBeforeMount(() => console.log('1️ antes de montar'))
onMounted(() => console.log('2️ componente montado'))
onBeforeUpdate(() => console.log('3️ antes de actualizar'))
onUpdated(() => console.log('4️ componente actualizado'))
onBeforeUnmount(() => console.log('5️ antes de destruir'))
onUnmounted(() => console.log('6️ componente destruido'))

function increase() {
  counter.value++
}
</script>

<template>
  <div>
    <p>Contador: {{ counter }}</p>
    <button @click="increase">Aumentar</button>
  </div>
</template>
