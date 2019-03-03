<template>
  <div class="contact">
    <Contact contact="contact" />
  </div>
</template>

<script>
// @ is an alias to /src
import Contact from '@/components/Contact.vue'

export default {
  name: 'home',
  components: {
    Contact,
  },
  data() {
    return {
      contact: {
        firstName: 'Dominic',
        lastName: 'English',
        email: 'dominic.b.english@gmail.com',
      },
    }
  },
}
</script>
