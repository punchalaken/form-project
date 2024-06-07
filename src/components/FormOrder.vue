<script setup>
import FirstNameField from './FormFieldsTemplates/FirstNameField.vue'
import SecondNameField from './FormFieldsTemplates/SecondNameField.vue'
import TelephoneField from './FormFieldsTemplates/TelephoneField.vue'
import EmailField from './FormFieldsTemplates/EmailField.vue'
import TimeField from './FormFieldsTemplates/TimeField.vue'
import PromotionField from './FormFieldsTemplates/PromotionField.vue'
import CommentField from './FormFieldsTemplates/CommentField.vue'
import SubmitButton from './FormFieldsTemplates/SubmitButton.vue'
import ResetButton from './FormFieldsTemplates/ResetButton.vue'
import { ref } from 'vue'

const promoObject = {
  '': 'Без акции',
  '1+1': '2 по цене 1',
  '3=4': '3 по цене 4',
  '1=9': '1 по цене 9',
  clothes: 'Я за одеждой',
  drink: 'Пьяный полдник',
  vegan: 'Веганы'
}


</script>

<template>
  <main class="main">
    <div class="conteiner">
      <form name="order" class="order">

        <FirstNameField/>

        <SecondNameField />

        <TelephoneField />

        <EmailField />

        <TimeField />

        <PromotionField :optionObject="promoObject" />

        <CommentField />

        <SubmitButton />

        <ResetButton />
      </form>
    </div>
  </main>
</template>

<style scoped>
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

.main {
  display: flex;
  justify-content: center;
  font-family: 'Inter';
  font-weight: 400;
  font-size: 22px;
  color: #6134ab;
}

.conteiner {
  box-sizing: border-box;
  max-width: 360px;
  min-width: 360px;
  padding: 20px 30px;
  border: 2px solid #40a44a;
}

.order {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  align-items: center;
}
</style>
