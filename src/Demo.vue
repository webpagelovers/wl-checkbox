<template>
  <wl-checkbox label="saaa" @change="change"></wl-checkbox>
</template>

<script>
  import WlCheckbox from "@/components/Checkbox";

  export default {
    name: "Demo",
    components: {
      WlCheckbox
    },
    data() {
      return {}
    },
    methods: {
      change(checked) {
        //console.log(checked)
      }
    }
  }
</script>

<style scoped>

</style>
