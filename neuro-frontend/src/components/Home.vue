<template lang="pug">
  div(v-mdl="").custom-item-list
    slot(name="item", v-for="item in value", :value="item")
</template>
<script>
  import Card from './Card'
  export default {
    name: 'Home',
    props: {
      value: {
        type: Array,
        default () {
          return []
        }
      }
    },
    components: {
      Card
    }
  }
</script>

<style lang="scss" scoped>
.custom-item-list {
  display: flex;
  flex-direction: column;
}
</style>
