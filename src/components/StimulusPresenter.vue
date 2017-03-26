<template>
  <div class="stimulus-presenter">
    <text-stimulus :textContent="stimulusConfig.text" :textColor="stimulusConfig.color" :textSize="stimulusConfig.size"></text-stimulus>
    <!--<button @click="updateContent('maoe', 'red', 2)" class="mdl-button mdl-js-button mdl-button--icon mdl-button--colored">
      <i class="material-icons">insert_drive_file</i>
    </button>-->
  </div>
</template>

<script>
import TextStimulus from './TextStimulus'
import Vue from 'vue'

export default {
  name: 'stimulus-presenter',
  components: {
    TextStimulus
  },
  data () {
    return {
      stimulusConfig: {
        text: 'teste',
        color: '#000',
        size: 4
      }
    }
  },
  methods: {
    updateContent (text, color, size) {
      this.stimulusConfig.text = text
      this.stimulusConfig.color = color
      this.stimulusConfig.size = size
    },
  }
}
</script>

<style scoped>

.stimulus-presenter {
  display: flex;
  flex-direction: column;
}

</style>
