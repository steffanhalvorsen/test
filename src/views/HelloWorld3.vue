<template>
  <div class="hello">
    <h1 @click="show = !show">Hi 3</h1>
    <div v-if="show">ey</div>
  </div>
</template>

<script>
export default {
  props: ['msg'],
  data() {
    return {
      show: true
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
