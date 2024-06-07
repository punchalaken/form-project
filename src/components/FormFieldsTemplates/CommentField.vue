<script setup lang="ts"></script>

<template>
  <label for="comment">Комментарий</label>
  <textarea
    name="comment"
    id="comment"
    rows="7"
    placeholder="Привезите заказ побыстрее, я голодный!"
  ></textarea>
</template>

<style scoped>
label {
  margin-bottom: 5px;
}

textarea {
  margin-bottom: 20px;
  padding: 10px;
  box-sizing: border-box;
  text-align: center;
  border: 2px solid #40a44a;
  min-width: 300px;
  max-width: 300px;
  resize: none;
}

textarea:focus {
  border-color: #40a44a;
  outline: none;
  box-shadow: 0 0 5px #40a44a;
}
</style>
