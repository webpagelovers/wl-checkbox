<template>
  <div :class="[this.className]">
    aaaaa
  </div>
</template>

<script>

  export default {
    name: "Checkbox",
    props: {
      className: {
        type: String,
        default: ''
      },
    },
    data() {
      return {}
    },
    methods: {
      check(item) {
      },
    }
  }
</script>


<style scoped>

</style>
