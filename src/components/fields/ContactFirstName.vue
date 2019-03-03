<template>
  <label
    class="field"
    for="contact-first-name"
    :class="{ 'is-invalid': !isValid }"
  >
    <div class="title">First Name</div>
    <input
      class="input"
      id="contact-first-name"
      :value="value"
      @input="onInput($event)"
    />
  </label>
</template>

<script>
export default {
  name: 'ContactFirstName',
  props: {
    value: String,
    validations: Array,
    isValid: Boolean,
  },
  methods: {
    onInput($event) {
      this.$emit('input', $event.target.value)
      this.$emit('update:isValid', this.validations[0]($event.target.value))
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
