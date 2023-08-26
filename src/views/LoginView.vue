<template>
  <div id="login">
    <div class="container">
      <div class="card mb-3 shadow rounded">
        <div class="row g-0">
          <div class="col-md-6">
            <div class="card-body">
              <h5 class="card-title">Login to Your Account</h5>
              <p class="card-text"><small class="text-body-secondary">Enter your username and password to access your account</small></p>

              <form action="">
                <div class="form-floating mb-3">
                  <input type="email" class="form-control" id="floatingInput" placeholder="name@example.com">
                  <label for="floatingInput">Email address</label>
                </div>
                <div class="form-floating">
                  <input type="password" class="form-control" id="floatingPassword" placeholder="Password">
                  <label for="floatingPassword">Password</label>
                </div>
                <div class="row validation">
                  <div class="col">
                    <input class="form-check-input" type="checkbox" id="gridCheck1">
                    <label class="form-check-label" for="gridCheck1">
                      Remember Me
                    </label>
                  </div>
                  <div class="col">
                    <router-link class="other-link link-underline-light" to="">Forgot Password ?</router-link>
                  </div>
                </div>
                
                <router-link class="btn btn-primary form-control" to="/dashboard">SIGN IN</router-link>
              </form>

              <p class="card-text"><small class="text-body-secondary">Or Sign In with</small></p>

              <div class="icon-col">
                <a href=""><img alt="Vue logo" src="../assets/1.png" width="80px" /></a>
                <a href=""><img alt="Vue logo" src="../assets/2.png" width="80px" /></a>
                <a href=""><img alt="Vue logo" src="../assets/3.png" width="80px" /></a>
              </div>
            </div>
          </div>
          
          <div class="col-md-6">
            <div class="side">
              <div class="side-text">
                <h5>Don't Have an Account Yet ?</h5>
                <p class="card-text"><small>Let's Create Your Account With Your Access For More Experiences !</small></p>
                <button type="button" class="btn btn-outline-primary"><router-link class="nav-link" to="/register">SIGN UP</router-link></button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'

export default {
  name: 'LoginView',
  components: {
    // eslint-disable-next-line vue/no-unused-components
    Navbar
  }
}
</script>

<style>

#login .container {
  margin-top: 5vh;
}

#login .card {
  text-align: center;
}

.card-body {
  margin: 5vh 5vw;
}

#login form {
  margin-top: 10vh;
  margin-bottom: 5vh;
}

#login .validation {
  margin: 14px -60px;
}

#login .validation label {
  margin-left: 4px;
}

#login .icon-account {
  display: inline-block;
  justify-content: center;
  align-items: center;
}

#login .side {
  background-color: blue;
  height: 100%;
  border-radius: 0px 0px 0px 50%;
}

#login .side-text {
  padding: 25vh 0px;
}

#login .side h5 {
  color: white;
  opacity: 0.8;
}

#login .side p {
  color: white;
}

#login .side .nav-link {
  color: white;
}

</style>