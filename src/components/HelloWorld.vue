<template>
  <div class="hello">
    <div v-for="i in 5" :key="i" class="py-3">content {{ i }}</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
};
</script>

<style scoped lang="scss">
.hello {}
</style>
