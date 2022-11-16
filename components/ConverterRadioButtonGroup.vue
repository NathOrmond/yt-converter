<template>
  <div class="radio-button-group">
    <ConverterRadioButton 
      v-for="option in options" 
      :option="option" 
      :key="option" 
    />
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import ConverterRadioButton from './ConverterRadioButton.vue';

export default defineComponent({
  components: {
    ConverterRadioButton
  },
  props: {
    options: {
     required: true,
     type: Array
    }
  },
  methods: {
  }
})
</script>


<style>
.radio-button-group {
  width: auto;
  margin: 20px auto;
  padding: 15px 20px;
  /* border: 1px solid black; */
  border-radius: 8px;
  display: flex;
  justify-content: space-between;
}

label {
  cursor: pointer;
}
</style>
