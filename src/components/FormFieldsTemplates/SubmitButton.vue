<script setup lang="ts"></script>

<template>
  <button type="submit" title="ok" class="ok-button button">
    <span class="visually-hidden">Подтвердение заказа</span>
    <span class="button-arrow ok">Подтвердить</span>
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
  background-color: #40a44a;
  margin-bottom: 20px;
  min-width: 270px;
  max-width: 270px;

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

  .ok {
    left: 5px;

    &::after {
      content: '\2714';
    }
  }
}

@media (hover) {
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
