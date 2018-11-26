<template>
  <div class="sample">
    <h1>{{ title }}</h1>
    <p>{{ name }}</p>
    <p>{{ num }}</p>
    <p :class="['hide',{seven : num >= 7}]">sample</p>
    <button
      type="button"
      name="button"
      @click="plus">plus
    </button>
  </div>
</template>

<script>
  export default {
    props: {
      title: {
        type: String,
        default: 'Default title'
      }
    },
    data() {
      return {
        name: 'taichi',
        num: 0
      }
    },
    mounted() {
      console.log('console')
    },
    methods: {
      plus() {
        this.num++
      }
    }
  }
</script>

<style lang="scss" scoped>
  .sample {
    color: red;
  }

  .hide {
    display: none;
  }

  .hide.seven {
    display: block;
  }
</style>
