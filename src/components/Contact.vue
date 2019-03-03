<template>
  <div class="contact">
    <label class="field" for="first-name">
      <div class="title">First Name</div>
      <input class="input" id="first-name" />
    </label>
    <label class="field" for="last-name">
      <div class="title">Last Name</div>
      <input class="input" id="last-name" />
    </label>
    <label class="field" for="email">
      <div class="title">Email</div>
      <input class="input" id="email" />
    </label>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  props: {
    contact: Object,
  },
}
</script>

<style lang="stylus" scoped>
label
  display: flex
  padding: 5px
  .title
    width: 160px
    text-align: left
    display: flex
    align-items: center
  .input
    padding: 10px 5px
</style>
