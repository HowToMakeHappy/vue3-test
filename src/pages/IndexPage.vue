<template>
  <button @click="increment">
    Count is {{state.count}}, Double is {{double}}
  </button>
</template>

<script>
import { computed, defineComponent, reactive } from 'vue'

export default defineComponent({
  setup () {
    const state = reactive({
      count: 0
    })

    const double = computed(() => state.count * 2)
    const increment = () => state.count++

    return {
      state,
      double,
      increment
    }
  },
  name: 'IndexPage'
})
</script>
