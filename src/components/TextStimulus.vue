<template>
  <div class="text-stimulus">
    <card class="container"
                :columns="columns"
                :shadow="shadow"
                :style="{ color: textColor, fontSize: textSize + 'em' }">
      <span class="text">
        {{ textContent }}
      </span>
    </card>
  </div>
</template>

<script>
import Card from './Card'

export default {
  name: 'text-stimulus',
  components: {
    Card
  },
  props: {
    columns: {
      type: Number,
      default: 12
    },
    shadow: {
      type: Number,
      default: 4
    },
    textContent: {
      type: String,
      default: ''
    },
    textColor: {
      type: String,
      default: '#000'
    },
    textSize: {
      type: Number,
      default: 2
    }
  },
  data () {
    return {
    }
  }
}
</script>

<style scoped>

.text-stimulus .container {
  display: flex;
  padding: 1em;
}

.text-stimulus .text {
}

</style>
