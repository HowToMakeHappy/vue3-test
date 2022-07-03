<template>
  <button @click="increment">
    Count is {{count}}, Double is {{double}}
  </button>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  data () {
    return {
      count: 0
    }
  },
  computed: {
    double () {
      return this.count * 2
    }
  },
  methods: {
    increment () {
      this.count++
    }
  },
  name: 'IndexPage'
})
</script>
