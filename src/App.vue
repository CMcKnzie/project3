<script setup>
</script>

<template>
  <div class="content">
        
        <div>
        <h1 class="main-title">Timer</h1>
        </div>

        <div class="formItems">
        <input id="time" type="number" min = "0" max="60"> 
        <button onclick="startTime()" type="button">Start Timer </button>
        </div>

        <div class ="Display">
            <div id="timerDisplay">
            </div>

        </div>
		
		<div style =" justify-content: bottom; color: black; margin-top: 25px">
			Caitlyn McKenzie
		</div>

    </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
