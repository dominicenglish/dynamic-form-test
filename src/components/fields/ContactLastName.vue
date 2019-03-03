<template>
  <label class="field" for="contact-last-name">
    <div class="title">Last Name</div>
    <input
      class="input"
      id="contact-last-name"
      :value="value"
      @input="$emit('input', $event.target.value)"
    />
  </label>
</template>

<script>
export default {
  name: 'ContactLastName',
  props: {
    value: String,
  },
}
</script>
