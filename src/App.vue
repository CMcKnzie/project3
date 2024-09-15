<script setup>

import {ref} from "vue"

    const seconds = ref(0)
    const _timerId = null

    const startTimer = () => {
      seconds.value = timer.value
      if (seconds.value > 0) {
        _timerId = setInterval(() => {
          seconds.value--
          if (seconds.value <= 0) {
            clearInterval(_timerId)
          }
        }, 1000)
      }
    
    return {
      seconds,
    }
  }
</script>

<template>
  <div class="content">
        
        <div>
        <h1 class="main-title">Timer</h1>
        </div>

        <div class="formItems">
        <input type="number" min = "0" max="60" :key="x" v-model = "timer"> 
        <button @click="startTimer(x)" type="button">Start Timer </button>
        </div>

        <div class ="Display">
            <span>{{ seconds }} left </span>

        </div>
		
		<div style =" justify-content: bottom; color: black; margin-top: 25px">
			Caitlyn McKenzie
		</div>

    </div>
</template>
