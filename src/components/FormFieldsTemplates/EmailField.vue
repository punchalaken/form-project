<script setup lang="ts"></script>

<template>
  <label for="email">Email</label>
  <input type="email" id="email" placeholder="ivan.ivanov@yandex.ru" />
</template>

<style scoped>
label {
  margin-bottom: 5px;
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
