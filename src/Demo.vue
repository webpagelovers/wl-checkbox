<template>
  <wl-checkbox></wl-checkbox>
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
      change(checkedItems) {
        console.log(checkedItems)
      },
      check(checkedItems) {
        //console.log(checkedItems)
      }
    }
  }
</script>

<style scoped>

</style>
