<template>
  <div :class="classes">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'card',
  props: {
    columns: {
      type: Number,
      default: 6
    },
    shadow: {
      type: Number,
      default: 4
    }
  },
  data () {
    return {
      defaultClasses: ['card', 'mdl-cell']
    }
  },
  computed: {
    classes () {
      return this.defaultClasses.concat(['mdl-cell--' + this.columns + '-col', 'mdl-shadow--' + this.shadow + 'dp'])
    }
  }
}
</script>