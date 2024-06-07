<script setup lang="ts">
import { ref, type Ref } from 'vue';

const text: Ref<string> = ref('')
const disable: Ref<boolean> = ref(true)

function checkBlur(): void {
  if (!text.value) {
    disable.value = false
  }
}

function reset() {
  disable.value = true
}
</script>

<template>
  
  <label for="first-name">Имя</label>

  <div 
    class = "error"
    :class="{disable: disable}">
      Обязательное поле
  </div>

  <input 
    type="text" 
    id="first-name" 
    placeholder="Иван" 
    v-model="text" 
    @blur="checkBlur" 
    @focus="reset"/>

</template>

<style scoped>
label {
  margin-bottom: 5px;
}

.error{
  font-size: 10px;
  color: red;
}

.disable{
  display: None;
}

input {
  margin-bottom: 20px;
  padding: 10px;
  box-sizing: border-box;
  text-align: center;
  min-width: 200px;
  border: 2px solid #40a44a;
}

input:focus {
  border-color: #40a44a;
  outline: none;
  box-shadow: 0 0 5px #40a44a;
}
</style>
