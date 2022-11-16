<template>
    <div class="buttonContainer">
        <button 
            class="button"
            @click="clicked"
        >
        <span>
            {{label}}
        </span>
        </button>
    </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
    name: 'ConverterButton',
    components: {
    },
    props: {
        label: {
			type: String, 
			default: undefined,
			required: true
		}
    }, 
    methods: {
        clicked(){ 
            this.$emit('handleClicked');
        }
    },
    data() {
        return {
        };
    }
})
</script>


<style>
.buttonContainer {
  width: auto;
  margin: 20px auto;
  padding: 15px 20px;
  /* border: 1px solid black; */
  border-radius: 8px;
  display: flex;
  justify-content: space-between;
}
</style>
