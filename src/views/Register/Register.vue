<template>
  <v-container class="d-flex flex-column align-center">
    <RegisterForm />
    <router-link to="/Login" tag="button"
      ><i>Already have an account?</i></router-link
    >
  </v-container>
</template>
<script>
import RegisterForm from '@/components/RegisterForm/RegisterForm.vue';
export default {
  name: 'Register',
  components: {
    RegisterForm,
  },
};
</script>
