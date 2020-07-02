<template>
    <div class="wrapper">
        <form class="form-signin">       
        <h2 class="form-signin-heading">Login</h2>
        <input type="email" class="form-control" name="username" placeholder="Email Address" required="true" autofocus="true" v-model="loginForm.userData.username"/>
        <input type="password" class="form-control" name="password" placeholder="Password" required="true" v-model="loginForm.userData.password"/>      
        <label class="checkbox">
            <input type="checkbox" value="remember-me" id="rememberMe" name="rememberMe" v-model="loginForm.remember"> Remember me
        </label>
        <button class="btn btn-lg btn-primary btn-block" type="submit" @click.prevent="submit">Login</button>   
        <a class="btn btn-link" @click="goToSignup">Create account</a>
        <hr>
        <h3>Other fields</h3>
        
        <h4>Array:</h4>
        <label for="cb1">
            <input type="checkbox" value="cb1" id="cb1" name="cb1" v-model="loginForm.cbox"> Cbox 1
        </label>
        <label for="cb2">
            <input type="checkbox" value="cb2" id="cb2" name="cb2" v-model="loginForm.cbox"> Cbox 2
        </label>
        
        <h4>Radio:</h4>
        <label for="rad1">
          <input type="radio" name="rad" value="one" id="rad1" v-model="loginForm.radio"> one
        </label>
        <label for="rad2">
          <input type="radio" name="rad" value="two" id="rad2" v-model="loginForm.radio"> two
        </label>
        <label for="rad3">
          <input type="radio" name="rad" value="three" id="rad3" v-model="loginForm.radio"> three
        </label>

        <h4>Select:</h4>
        <select name="daytime" id="" v-model="loginForm.daytime">
          <option v-for="item in loginForm.dayTimeOptions" :key="item">{{item}}</option>
        </select>

        </form>



        <section>
          <h4>Preview</h4>
          <p>Name: {{loginForm.userData.username}}</p>
          <p>PWD: {{loginForm.userData.password}}</p>
          <p>Remember: {{loginForm.remember}}</p>
          <hr>
          <h4>Other fields</h4>
          <p>Array:</p>
          <ul>
            <li v-for="item in loginForm.cbox" :key="item">{{item}}</li>
          </ul>
          <p>Boolean: {{loginForm.radio}}</p>
          <p>Select: {{loginForm.daytime}}</p>
        </section>
    </div>    
</template>
<script>
export default {
  name: 'Login',
  data() {
    return {
      loginForm: {
        userData: {
          username: '',
          password: ''
        },
        remember: true,
        cbox: [],
        radio: 'one',
        daytime: '',
        dayTimeOptions: ["Morning", "Afternoon", "Evening"]
      }
    }
  },
  methods: {
    goToSignup: function() {
      this.$router.push('/register');
    },
    submit: function() {
      console.log(this.loginForm)
    }
  }
}
</script>
<style scoped>

.wrapper {
  margin-top: 80px;
  display: flex;
  justify-content: center;
}

.form-signin {
  flex-grow: 1;
  max-width: 380px;
  padding: 15px 35px 45px;
  border: 1px solid rgba(0, 0, 0, 0.1);
}
.form-signin .form-signin-heading,
.form-signin .checkbox {
  margin-bottom: 30px;
}
.form-signin .checkbox {
  font-weight: normal;
}
.form-signin .form-control {
  position: relative;
  font-size: 16px;
  height: auto;
  padding: 10px;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
.form-signin .form-control:focus {
  z-index: 2;
}
.form-signin input[type="email"] {
  margin-bottom: -1px;
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}
.form-signin input[type="password"] {
  margin-bottom: 20px;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}
section {
  padding: 4rem;
}
</style>