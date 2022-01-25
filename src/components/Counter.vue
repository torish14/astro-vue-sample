<template>
	<div class="counter">
		<button @click="decrement()">-</button>
		<pre>{{ count }}</pre>
		<button @click="increment()">+</button>
	</div>
	<div class="counter-message">
		<slot />
	</div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const count = ref(0)
const increment = () => count.value++
const decrement = () => count.value--
</script>
