<template>
  <NuxtForm @submit="register">
    <template #default>
      <NuxtField label="Имя" type="text" name="name" />
      <NuxtField label="Email" type="email" name="email" />
      <NuxtField label="Пароль" type="password" name="password" />
      <NuxtField
        label="Подтверждение пароля"
        type="password"
        name="passwordConfirmation" />
      <NuxtSubmit label="Зарегистрироваться" />
    </template>
  </NuxtForm>
</template>

<script>
export default {
  methods: {
    async register() {
      const { email, password, passwordConfirmation } = this.$refs.form.value;

      if (password !== passwordConfirmation) {
        console.error("Пароли не совпадают");
        return;
      }

      try {
        await this.$supabase.auth.signUp({ email, password });
        // Навигация на страницу после регистрации
        this.$router.push("/");
      } catch (error) {
        console.error(error);
      }
    },
  },
};
</script>
