<script setup lang="ts"></script>

<template>
  <button type="reset" title="Reset menu" class="reset-button button">
    <span class="visually-hidden">Сброс заказа</span>
    <span class="button-arrow reset">Отмена</span>
  </button>
</template>

<style lang="scss" scoped>
.visually-hidden {
  position: absolute !important;
  width: 1px !important;
  height: 1px !important;
  margin: -1px !important;
  border: 0 !important;
  padding: 0 !important;
  white-space: nowrap !important;
  clip-path: inset(100%) !important;
  clip: rect(0 0 0 0) !important;
  overflow: hidden !important;
}

button {
  border: none;
  border-radius: 5px;
  box-sizing: border-box;
  padding: 10px;
  text-align: center;
  font-size: 30px;
  color: #ffffff;
  background-color: #f4511e;
  min-width: 200px;
  max-width: 200px;

  .button-arrow {
    position: relative;
    left: 10px;
    transition: all 0.5s;

    &::after {
      opacity: 0;
      margin-left: 5px;
      font-size: 20px;
      transition: all 0.5s;
    }
  }

  .reset::after {
    content: '\2718';
  }
}

@media (hover: hover) {
  .button:hover .button-arrow::after {
    transition: all 0.5s;
    opacity: 1;
  }

  .button:hover .button-arrow {
    left: 0;
    transition: all 0.5s;
  }
}
</style>
