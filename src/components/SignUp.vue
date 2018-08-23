<template>
  <div class="signup">
    <div class="left-side left">
      <div class="wrap-title">
        <h1>Your Company.</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
      </div>
    </div>
    <div class="right-side right">
      <div class="wrap-form">
        <h1>Signup</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod. <a href="#" v-on:click="redirectToSignin">Sign in here</a></p>
        <div class="row">
          <form class="col s12">
            <div class="row">
              <div class="input-field col s12">
                <input id="email" type="email" class="validate">
                <label for="email">Email</label>
              </div>
            </div>
            <div class="row">
              <div class="input-field col s12">
                <input id="password" type="password" class="validate" v-model="password">
                <label for="password">Password</label>
              </div>
            </div>
            <div class="row">
              <div class="input-field col s12">
                <input id="password-validate" type="password" class="validate" v-bind:class="{ invalid: isPasswordNotSame }" v-on:input="watchPassword" v-model="passwordValidate">
                <label for="password-validate">Re type password</label>
              </div>
            </div>
            <a class="waves-effect waves-light btn-large btn-signup">SIGNUP</a>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SignUp',
  data: function() {
    return {
        password: '',
        passwordValidate: '',
        isPasswordNotSame: false
    }
  },
  methods: {
    redirectToSignin: function() {
      this.$router.push('/');
    },
    watchPassword: function() {
      if(this.passwordValidate != this.password) {
        this.isPasswordNotSame = true;
      } else {
        this.isPasswordNotSame = false;
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .signup {
    width: 900px;
    height: 600px;
    margin: 20px auto;
    border-radius: 10px;
    -moz-border-radius: 10px;
    -webkit-border-radius: 10px;
    box-shadow: 0 3px 16px -5px #070707;
    z-index: 10;
  }

  .left-side {
    background-image: url(../assets/bg.jpg);
    background-position: center;
    height: 100%;
    width: 50%;
    border-radius: 5px 0 0 5px;
    -moz-border-radius: 5px 0 0 5px;
    -webkit-border-radius: 5px 0 0 5px;
    position: relative;
  }

  .right-side {
    height: 100%;
    width: 50%;
    background-color: white;
    border-radius: 0 5px 5px 0;
    -moz-border-radius: 0 5px 5px 0;
    -webkit-border-radius: 0 5px 5px 0;
  }

  .wrap-title {
    position: absolute;
    top: 150px;
    left: 25px;
  }

  .left-side h1 {
    color: white;
    font-size: 50px;
  }

  .left-side p {
    color: white;
  }

  p {
    margin-top: -20px;
  }

  .wrap-form {
    margin: 40px 20px;
  }

  .right-side p {
    color: grey;
  }

  .btn-signup {
    float: right;
  }
</style>
