<template>
  <div class="contact">
    <DynamicForm :config="config" />
    <!-- <contact-first-name /> -->
  </div>
</template>

<script>
// import Vue from 'vue'
// @ is an alias to /src
import DynamicForm from '@/components/DynamicForm.vue'

// import ContactFirstName from '@/components/fields/ContactFirstName.vue'

export default {
  name: 'DynamicFormPage',
  components: {
    DynamicForm,
  },
  data() {
    return {
      config: {
        fields: [
          {
            name: 'ContactFirstName',
            value: 'Dominic',
            validations: [],
          },
          {
            name: 'ContactLastName',
            value: 'English',
            validations: [],
          },
        ],
      },
    }
  },
}
</script>
