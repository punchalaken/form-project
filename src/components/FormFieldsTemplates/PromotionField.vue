<script setup lang="ts">
interface SomeObject {
  [key: string]: string
}

const props = defineProps<{
  optionObject: SomeObject
}>()
</script>

<template>
  <label for="promotion">Выберите акцию</label>
  <select name="promotion" id="promotion">
    <option v-for="(value, key) in props.optionObject" :key="key" :value="key">
      {{ value }}
    </option>
  </select>
</template>

<style scoped>
label {
  margin-bottom: 5px;
}

select {
  margin-bottom: 20px;
  padding: 10px;
  box-sizing: border-box;
  text-align: center;
  min-width: 200px;
  border: 2px solid #40a44a;
}

select:focus {
  border-color: #40a44a;
  outline: none;
  box-shadow: 0 0 5px #40a44a;
}
</style>
