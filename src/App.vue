<script>
export default {
  name: 'Types',

  data: () => ({
    isPasswordVisible: false,
    isPasswordWrong: false,
    isUsernameWrong: false,
    username: '',
    password: '',
    errorMessage: 'Error!',
  }),
};
</script>

<template>
  <main class="MainLogin">
    <header>
      <h1 class="companyName">TFE | Taxi For Everyone</h1>
    </header>

    <div class="username">
      <va-input
        v-model="username"
        class="mb-6"
        label="Enter Username"
        placeholder="Username..."
      />
    </div>

    <div class="password">
      <va-input
        v-model="password"
        :type="isPasswordVisible ? 'text' : 'password'"
        label="Enter Password"
        placeholder="Password..."
        class="mr-6 mb-6"
      >
        <template #appendInner>
          <va-icon
            :name="isPasswordVisible ? 'off' : 'on'"
            size="small"
            color="808080"
            @click="isPasswordVisible = !isPasswordVisible"
          />
        </template>
      </va-input>
    </div>
  </main>
</template>

<style></style>
