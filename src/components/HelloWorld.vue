<template>
  <form id="basic-signup-form" @submit.prevent="submitHandler">
    <div class="form-input">
      <label for="username">
        Username
      </label>
      <input
        id="username"
        type="text"
        name="username"
        pattern="[a-z]{4,8}"
        required
      />
      <p class="help-text">
        Usernames must be lowercase and between 4-8 characters in length.
      </p>
    </div>

    <div class="form-input">
      <label for="email">
        Email
      </label>
      <input id="email" type="email" name="email" required />
    </div>

    <input type="submit" value="Register!" />
  </form>
</template>

<script>
export default {
  methods: {
    submitHandler() {
      alert('Thank you for signing up!');
    },
  },
};
</script>

<style>
body {
  min-height: 100vh;
  padding: 2em;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(to bottom right, cyan, magenta);
}

form {
  display: flex;
  flex-direction: column;
  background-color: #fff;
  border: 1px solid #999;
  width: 90%;
  max-width: 320px;
  padding: 3em 2em;
  border-radius: 0.3em;
  box-shadow: 0.25em 0.15em 12em 0 rgba(#000, 0.25);

  * {
    box-sizing: border-box;
  }

  h2 {
    margin-top: 0;
    color: #555;
  }
}

.form-input {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  margin-bottom: 1em;

  input,
  textarea {
    width: 100%;
    margin-bottom: 0;
    border: 1px solid #caca;
    padding: 0.5em;
    border-radius: 0.25em;
  }

  label {
    font-weight: bold;
    font-size: 0.85em;
    margin-bottom: 0.5em;
  }

  .help-text {
    margin-top: 0.5em;
    margin-bottom: 0;
    color: #999;
    font-size: 0.75em;
  }
}

input[type='submit'] {
  appearance: none;
  border: 1px solid deeppink;
  background-color: magenta;
  padding: 1em 1.5em;
  font-weight: bold;
  color: #fff;
  text-transform: uppercase;
  border-radius: 0.5em;
  margin: 1em auto 0 auto;
}
</style>
