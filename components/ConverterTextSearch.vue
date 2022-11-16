<template>
    <input 
        type="text" 
        placeholder="value" 
        v-model="inputVal"
    />
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    value: String
  },
  setup(props) {
    props.value 
  },
  computed: {
    inputVal: {
      get() {
        return this.value;
      },
      set(val) {
        this.$emit('input', val);
      }
    }
  }
})
</script>


<style></style>
