<template>
  <div>
    <template v-if="fields">
      <component
        v-for="field in fields"
        :is="field.name"
        :label="field.label"
        v-model="field.value"
        :validations="field.validations"
        :isValid.sync="field.isValid"
      ></component>
    </template>
  </div>
</template>

<script>
// import Contact from '@/components/Contact.vue'
// import ContactFirstName from '@/components/fields/ContactFirstName.vue'
export default {
  // components: {
  //   ContactFirstName,
  // },
  props: {
    config: Object,
  },
  data() {
    return {
      fields: [
        {
          name: 'ContactFirstName',
          value: 'Dominic',
          validations: [value => value.length > 0],
          isValid: true,
        },
        {
          name: 'ContactLastName',
          value: 'English',
          validations: [],
          isValid: true,
        },
        {
          name: 'F-Text',
          label: 'Cool Field',
          value: 'testaroo',
          validations: [],
          isValid: true,
        },
      ],
    }
  },
  computed: {
    // fields() {
    //   if (!this.config || !Array.isArray(this.config.fields)) return
    //   return this.config.fields
    // },
  },
  // watch: {
  //   test: {
  //     immediate: true,
  //     handler() {
  //       import test from `@/components/${test}.vue`
  //     }
  //   }
  // }
}
</script>
