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

    <div>
      <va-button
        style="position: relative; top: 150px"
        size="large"
        color="#00BA7C"
        text-color="#FFFFFF"
        round
      >
        Log in</va-button
      >
    </div>

    <div class="devider">
      <div class="line" style="position: relative; top: 11px; left: 70px"></div>
      <div
        class="line"
        style="position: relative; top: 10px; left: 250px"
      ></div>
      <p>or</p>
    </div>

    <div>
      <va-button
        style="position: relative; top: 225px"
        size="large"
        color="#FFFFFF"
        border-color="#000000"
        text-color="#000000"
        round
      >
        Sign up</va-button
      >
    </div>
  </main>
</template>
