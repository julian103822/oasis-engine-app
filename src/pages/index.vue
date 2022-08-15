<script setup lang="ts">
import { startGame } from '~/utils/flyBird'
onMounted(() => {
  startGame()
})
</script>

<template>
  <canvas id="canvas" style="width: 100vw; height: 100vh; position: absolute; left: 0; top: 0;" />
</template>
