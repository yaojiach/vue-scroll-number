<template>
  <ul class="flex">
    <ScrollNumber
      v-for="(num, idx) of numArr"
      :key="idx"
      as="li"
      :i="num"
      :delay="idx + 1"
    />
  </ul>
</template>

<script>
import ScrollNumber from './ScrollNumber.vue'

export default {
  components: { ScrollNumber },
  data: () => ({ num: 886 }),
  computed: {
    numArr() {
      const str = String(this.num)

      return [parseInt(str[0]), parseInt(str[1]), parseInt(str[2])]
    }
  }
}
</script>

<style scoped>
.flex {
  display: flex;
}
ul {
  padding: 0;
  margin: 0;
  list-style: none;
}
</style>

