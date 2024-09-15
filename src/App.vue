<script setup>

import {ref} from "vue"

    const seconds = ref(0)
    const timerReset = ref(null)
    const secs = ref(0)

    const startTimer = () => {
      seconds.value = secs.value
      if (seconds.value > 0) {
       timerReset = setInterval(() => {
          seconds.value--
          if (seconds.value == -1) {
            seconds.value = 0
            clearInterval(timerReset);
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
        <input v-model.number="secs" type="number" min = "0" max="60" :key="x" > 
        <button @click="startTimer()" type="button">Start Timer </button>
        </div>

        <div class ="Display">
            <span>{{seconds}} seconds left </span>

        </div>
		
		<div style =" justify-content: bottom; color: black; margin-top: 25px">
			Caitlyn McKenzie
		</div>

    </div>
</template>
