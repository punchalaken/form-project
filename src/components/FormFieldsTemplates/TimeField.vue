<script setup lang="ts"></script>

<template>
  <fieldset class="order-time">
    <legend>Выберите время</legend>

    <div>
      <input type="radio" name="order-time" value="now" id="now" required checked />
      <label for="now">Как можно быстрее</label>
    </div>

    <div>
      <input type="radio" name="order-time" value="at-time" id="at-time" class="at-time" />
      <label for="at-time">Ко времени</label>

      <div class="time">
        <label for="time-choose">Дата:</label>
        <input type="datetime-local" id="time-choose" />
      </div>
    </div>
  </fieldset>
</template>

<style lang="scss" scoped>
legend {
  text-align: center;
}

.order-time {
  margin-bottom: 20px;
  padding: 10px;
  box-sizing: border-box;
  text-align: center;
  min-width: 200px;
  border: 2px solid #40a44a;
  text-align: start;
  height: 100px;
  transition: all 0.2s;

  &:has(.at-time:checked) {
    height: 170px;
    transition: all 0.2s;
  }
}

.time {
  display: flex;
  flex-direction: column;
  align-items: center;
  opacity: 0;
  transition: all 0.3s;

  label {
    margin-block: 5px;
  }

  input {
    min-width: 200px;
    max-width: 200px;
    text-align: center;
  }

  .at-time:checked ~ & {
    opacity: 1;
    transition: all 0.3s;
  }
}
</style>
