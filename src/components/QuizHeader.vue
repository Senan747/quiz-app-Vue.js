<script setup>
import {defineProps} from "vue"


const {questionStatus, barPercentage} = defineProps(["questionStatus", "barPercentage"])

</script>
<template>
    <header>
            <h4>Question {{ questionStatus }}</h4>
            <div class="bar">
                <div class="completion" :style="{width: barPercentage}"></div>
            </div>
    </header> 
</template>

<style scoped>
  h4{
    font-size: 40px;
  }
  .bar {
    border: 2px solid bisque;
    width: 300px;
    height: 40px;

  }
  .completion {
    height: 100%;
    width: 0%;
    background-color: bisque;
  }
</style>