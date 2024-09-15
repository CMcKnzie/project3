<script setup>

import {ref} from "vue"

const varTime = ref('')
const timer = ref('')
const countDownSecs = ref('')

const startTime =()=>{ 
  varTime = setInterval(start, 1000);
  timerDisplay.value = timer.value;
  countDownSecs = timer.value;

  timerDisplay.value.push({
  content: timer.value,
})

} 

const start=() =>{
  countDownSecs--;
  timerDisplay.value = countDownSecs;
  timerDisplay.value
  if (countDownSecs == -1){
    stop();
   timerDisplay.value = "0";
  }
}

const stop = ()=>{
  clearInterval(varTime)
}



</script>

<template>
  <div class="content">
        
        <div>
        <h1 class="main-title">Timer</h1>
        </div>

        <div class="formItems">
        <input type="number" min = "0" max="60" :key="x" v-model = "timer"> 
        <button @click="startTime()" type="button">Start Timer </button>
        </div>

        <div class ="Display">
            <div ref="timerDisplay">
            </div>

        </div>
		
		<div style =" justify-content: bottom; color: black; margin-top: 25px">
			Caitlyn McKenzie
		</div>

    </div>
</template>
