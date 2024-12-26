<template>
  <div class="login-container">
    <img src="/assets/images/logo.png" alt="logo" style="margin-bottom: 20px;">
    <h2>Welcome Back</h2>
    <p>Please enter your details to sign in</p>
    <form>
      <label for="email">Email Address</label>
      <div class="input-container">
        <input 
          id="email" 
          type="email" 
          placeholder="✉ Email address" 
          required 
        />
      </div>

      <label for="password">Password</label>
      <div class="input-container">
        <input 
          id="password"
          type="password" 
          placeholder="Password" 
          required 
        />
      </div>

      <div class="remember-container">
        <div class="remember-left">
          <input type="checkbox" id="rememberMe" />
          <label for="rememberMe">Remember Me</label>
        </div>
        <a href="#">Forgot password?</a>
      </div>

      <button type="submit">Sign In</button>

      <p class="or-continue">---------------Or continue with---------------</p>

      <div class="socialmedia">
        <div class="apple">
          <button class="social-button apple">
          <img src="/assets/images/apple-logo.png" alt="Apple">Apple
        </button>
        </div>
        <div>
          <button class="social-button google">
          <img src="/assets/images/google.png" alt="Google">Google
        </button>
        </div>
      </div>
      <div class="signup">
        <p>Don't have a Google Account? <a href="http://login">Sign Up</a></p>
      </div>
    </form>

  </div>
</template>

<style src="~/assets/css/login.css"></style>
