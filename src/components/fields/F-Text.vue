<template>
  <label class="field" :class="{ 'is-invalid': !isValid }">
    <div class="title">{{ label }}</div>
    <input class="input" :value="value" @input="onInput($event)" />
  </label>
</template>

<script>
export default {
  name: 'F-Text',
  props: {
    label: String,
    value: String,
    validations: Array,
    isValid: Boolean,
  },
  methods: {
    onInput($event) {
      this.$emit('input', $event.target.value)
      this.$emit(
        'update:isValid',
        this.validations.every(v => v($event.target.value))
      )
    },
  },
}
</script>

<style lang="stylus" scoped>
label
  display: block
  padding: 10px
.is-invalid
  background: rgba(255, 0, 0, 0.5)
</style>
