<template>
  <div class="login">
    <div class="left-side left">
      <div class="wrap-title">
        <h1>Your Company.</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
      </div>
    </div>
    <div class="right-side right">
      <div class="wrap-form">
        <h1>Login</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod. <a href="#">Sign up here</a></p>
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
                <input id="password" type="password" class="validate">
                <label for="password">Password</label>
              </div>
            </div>
            <p>
              <label>
                <input type="checkbox" class="filled-in"/>
                <span>Remember me</span>
              </label>
            </p>
            <a class="waves-effect waves-light btn-large btn-login">LOGIN</a>
            <div class="wrap-btn-social">
              <p>Login with social media</p>
              <a class="waves-effect waves-light btn btn-facebook"><i class="fa fa-facebook"></i> Facebook</a>
              <a class="waves-effect waves-light btn btn-google-plus"><i class="fa fa-google-plus"></i> Google +</a>
              <a class="waves-effect waves-light btn btn-twitter"><i class="fa fa-twitter"></i> Twitter</a>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .login {
    width: 900px;
    height: 600px;
    margin: 35px auto;
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

  .btn-login {
    float: right;
  }

  .wrap-btn-social {
    clear: both;
    float: left;
    margin-top: 70px;
  }

  .btn-facebook {
    background-color: #3b5998;
  }

  .btn-google-plus {
    background-color: #dd4b39;
  }

  .btn-twitter {
    background-color: #00aced;
  }
</style>
