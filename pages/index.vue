<template>
  <div class="container">
    <div class="item">
      <h1>{{titleText}}</h1>
    </div>

    <div class="item">
      <ConverterTextSearch 
      v-model="searchText"
      />
    </div>
    
    <div class="item"> 
      <div class="innerContainer"> 
        <ConverterRadioButtonGroup 
          :options="conversionOptions"
          v-model="selectedConversionOption"
        />
      </div>
      <div class="innerContainer">
        <ConverterButton 
          :label="convertButtonText"
          @handleClicked="convertClicked"
        />
      </div>
    </div>
    
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import * as ytdl from 'ytdl-core';
import ConverterButton from '@/components/ConverterButton.vue'
import ConverterTextSearch from '@/components/ConverterTextSearch.vue'
import ConverterRadioButtonGroup from '@/components/ConverterRadioButtonGroup.vue'

export default Vue.extend({
  name: 'IndexPage',
  components: {
    ConverterButton,
    ConverterTextSearch,
    ConverterRadioButtonGroup
  },
  methods: {
    async convertClicked() {
     // TODO
     alert("not yet implemented")
    }
  },
  data() { 
    return { 
      convertButtonText: "Convert",
      conversionOptions: ["audio", "video"], 
      selectedConversionOption: "",
      titleText: "YouTube Video Downloader",
      fileType: { VIDEO: "video", AUDIO: "audio"},
      searchText: "" 
    }
  }
})
</script> 

<style scoped>
.container {
  min-height: 100vh;
  display: flex; 
  flex-direction: column; 
  align-items: center;
  justify-content: center;
  align-content: center; 
  /* margin-right: auto;
  margin-left: auto; */
  /* border: 1px solid red; */
}

.item {
  margin: 1%;
  padding: 1%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  /* border: 1px solid green; */
}

.innerContainer {
  margin: 1%;
  padding: 1%;
  justify-content: center;
  /* border: 1px solid purple; */
}

</style>
