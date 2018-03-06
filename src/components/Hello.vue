<template>
<div :class="{ a: true, ...b }">
  {{ data }}
</div>
</template>

<script>
export default {
  props: {
    data: Object,
  },
  mounted () {
    console.log('this.data', this.data);
  },
  data () {
    return {
      b: true,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.a {
  color: blue;
}

.b {
  font-size: 30px;
}
</style>
