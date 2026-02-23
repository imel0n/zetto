<template>
  <div class="login-container">
    <div class="login-card">
      <h1>Login</h1>
      
      <div class="input-field">
        <label for="username">Username</label>
        <input type="text" id="username" placeholder="Enter your username" />
      </div>

      <div class="input-field">
        <label for="password">Password</label>
        <input type="password" id="password" placeholder="Enter your password" />
      </div>

      <button class="login-button" @click="handleLogin">Log In</button>
      
      <p class="footer-text">Don't have an account? <span>Sign up</span></p>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    handleLogin() {
      console.log("attempting login");
      this.$router.push("/home");
    }
  }
}
</script>

<style scoped>
.login-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.login-card {
  background-color: white;
  padding: 2.5rem;
  border-radius: 12px;
  width: 100%;
  max-width: 400px;
  text-align: center;
}

h1 {
  margin-bottom: 2rem;
  font-weight: 600;
}

.input-field {
  text-align: left;
  margin-bottom: 1.5rem;
}

label {
  display: block;
  margin-bottom: 0.5rem;
  color: #666;
  font-size: 0.9rem;
}

input {
  width: 100%;
  padding: 12px;
  border: 1px solid lightgrey;
  border-radius: 6px;
  font-size: 1rem;
}

input:focus {
  outline: none;
  border: 1px solid skyblue;
}

.login-button {
  width: 100%;
  padding: 12px;
  background-color: skyblue;
  color: white;
  border: none;
  border-radius: 6px;
  font-size: 1rem;
  font-weight: bold;
  cursor: pointer;
  margin-top: 1rem;
}

.login-button:hover {
  background-color: rgb(125, 192, 219);
}

.footer-text {
  margin-top: 1.5rem;
  font-size: 0.85rem;
}

.footer-text span {
  color: skyblue;
  font-weight: 600;
}

.footer-text span:hover {
  cursor: pointer;
  color: rgb(125, 192, 219);
}
</style>