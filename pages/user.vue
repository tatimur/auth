<template>
  <v-app>
    <userForm />
  </v-app>
</template>

<script>
  import userForm from '@/components/userForm'
  export default {
    middleware: ['user-auth'],
    components: {userForm},
    layout: 'userData'
  }

</script>
