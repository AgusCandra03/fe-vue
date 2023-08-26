<template>
  <div id="register">
    <div class="container">
      <div class="card mb-3 shadow rounded">
        <div class="row g-0">
          <div class="col-md-6">
            <div class="side">
              <div class="side-text">
                <h5>Have an Account ?</h5>
                <p class="card-text"><small>Let's Move to Login Page For Start Your Experiences ! </small></p>
                <button type="button" class="btn btn-outline-primary"><router-link class="nav-link" to="/">SIGN IN</router-link></button>
              </div>
            </div>
          </div>

          <div class="col-md-6">
            <div class="card-body">
              <h5 class="card-title">Create an Account</h5>
              <p class="card-text"><small class="text-body-secondary">Enter your data to create new account</small></p>

              <form>
                <div class="row">
                  <div class="col">
                    <div class="col form-floating mb-3">
                    <input type="text" class="form-control" id="floatingfirst" placeholder="First Name">
                    <label for="floatingfirst">First Name</label>
                  </div>
                  </div>
                  <div class="col">
                    <div class="col form-floating mb-3">
                    <input type="text" class="form-control" id="floatinglast" placeholder="Last Name">
                    <label for="floatinglast">Last Name</label>
                  </div>
                  </div>
                </div>
                <div class="form-floating mb-3">
                  <input type="email" class="form-control" id="floatingInput" placeholder="name@example.com">
                  <label for="floatingInput">Email</label>
                </div>
                <div class="form-floating">
                  <input type="password" class="form-control" id="floatingPassword" placeholder="Password">
                  <label for="floatingPassword">Password</label>
                </div>
                <div class="terms">
                  <input class="form-check-input" type="checkbox" id="gridCheck1">
                  <label class="form-check-label" for="gridCheck1">
                    I accepted the <a href="">Terms and Conditions </a>
                  </label>
                </div>
                
                <!-- <router-link class="btn btn-primary form-control" to="/">SIGN UP</router-link> -->
                <button type="button" class="btn btn-primary form-control" @click="signupAlert()">SIGN UP</button>
              </form>

              <p class="card-text"><small class="text-body-secondary">Or Sign Up Using</small></p>

              <div class="icon-col">
                <a href=""><img alt="Vue logo" src="../assets/1.png" width="80px" /></a>
                <a href=""><img alt="Vue logo" src="../assets/2.png" width="80px" /></a>
                <a href=""><img alt="Vue logo" src="../assets/3.png" width="80px" /></a>
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
import swal from 'sweetalert'

export default {
  name: 'RegisterView',
  components: {
    // eslint-disable-next-line vue/no-unused-components
    Navbar
  },
  methods: {
    signupAlert(){
      swal({
        title: "Success !",
        text: "You can access your account after sign in.",
        icon: "success",
        button: false
      });
    }
  }

}
</script>

<style>
#register .container {
  margin-top: 3vh;
}

#register .card {
  text-align: center;
}

#register .card-body {
  margin: 5vh 5vw;
}

#register form {
  margin-top: 5vh;
  margin-bottom: 5vh;
}

#register .terms {
  margin: 14px 0px;
  text-align: start;
}

#register .terms label {
  margin-left: 4px;
}

#register .icon-account {
  display: inline-block;
  justify-content: center;
  align-items: center;
}

#register .side {
  background-color: blue;
  height: 100%;
  border-radius: 0px 0px 50% 0px;
  box-sizing: border-box;
}

#register .side-text {
  padding: 25vh 0px;
}

#register .side h5 {
  color: white;
  opacity: 0.8;
}

#register .side p {
  color: white;
}

#register .side .nav-link {
  color: white;
}
</style>