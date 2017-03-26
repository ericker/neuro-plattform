<template>
  <div class="home">
    <stimulus-presenter></stimulus-presenter>
  </div>
</template>

<script>
import StimulusPresenter from './StimulusPresenter'

export default {
  name: 'home',
  components: {
    StimulusPresenter
  },
  data () {
    return {
    }
  }
}
</script>

<style scoped>
.home {
  display: flex;
  flex-grow: 1;
  flex-direction: column;
}

</style>
