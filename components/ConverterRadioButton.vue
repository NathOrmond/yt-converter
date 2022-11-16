<template>
    <div>
    <label :for="option">
        <input 
            type="radio"   
            name="radio-input" 
            :value="option" 
            :id="option" 
            @change="$parent.$emit('input', option)" 
        />
            {{ option }}
    </label>
    </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
    props: {
        option: {
            required: true,
            type: String
        }
    },
    methods: {
    },
})
</script>


<style>
label {
  cursor: pointer;
}
</style>
