<template>
  <div class="checkbox">
    <div
      :class="['check',isChecked  ? 'checked' : '', disabled ? 'disabled' : '',this.className]"
      @click="toggleCheck">
    </div>
    <div class="checkbox-label" @click="toggleCheck">{{label}}</div>
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
      checked: {
        type: Boolean,
        default: false
      },
      disabled: {
        type: Boolean,
        default: false
      },
      label: {
        type: String,
        default: ''
      }
    },
    data() {
      return {
        isChecked: false
      }
    },
    methods: {
      toggleCheck() {
        if (this.disabled) {
          return false
        }
        this.isChecked = !this.isChecked
        this.$emit('change', this.isChecked)
      },
    },
    watch: {
      checked: {
        handler(newVal, oldVal) {
          this.isChecked = newVal
        },
        immediate: true
      }
    }
  }
</script>


<style scoped>
  .checkbox {
    display: inline-block;
  }

  .check {
    float: left;
    width: 16px;
    height: 16px;
    border: 1px solid #ddd;
    border-radius: 2px;
  }

  .check:hover {
    border-color: #4395ff;
  }

  .check.checked {
    border-color: #4395ff;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .check.checked:before {
    content: '';
    display: block;
    width: 4px;
    height: 8px;
    border-color: #4395ff;
    border-style: solid;
    border-width: 0 2px 2px 0;
    transform: rotate(45deg) translate(-10%, -10%);
  }

  .check.half {
    border-color: #4395ff;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .check.half:before {
    content: '';
    display: block;
    width: 8px;
    height: 2px;
    border: none;
    background-color: #4395ff;
    transform: rotate(0deg) translate(0, 0);
  }

  .check.checked.disabled {
    background-color: #ddd;
    border-color: #ccc;
  }

  .check.checked.disabled:before {
    border-color: #fff;
  }

  .checkbox-label {
    float: left;
    height: 16px;
    line-height: 16px;
    margin-left: 5px;
    cursor: pointer;
  }
</style>
