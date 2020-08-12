<template>
  <v-app>
    <h1 class="login__title">Войти в личный кабинет</h1>
    <v-form
      class="login__form"
      ref="form"
      @submit.prevent="onSubmit"
    >
      <v-text-field
        label="E-mail"
        required
      ></v-text-field>

      <v-text-field
        type="password"
        label="Пароль"
        required
      ></v-text-field>

      <v-btn type="submit" color="primary">
        Войти
      </v-btn>
    </v-form>
  </v-app>
</template>

<script>
  export default {
    methods: {
      onSubmit() {
        this.$store.dispatch('login')
        this.$router.push('/user')
      }
    }
  }
</script>

<style>
  * {
    text-align: center;
    color: #808080;
  }

  .login__title {
    margin-top: 50px;
  }

  .login__form {
    margin: 0 auto;
    width: 600px;
  }
</style>
