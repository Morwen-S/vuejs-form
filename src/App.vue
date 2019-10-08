<template>
  <div>
    <button v-on:click="component='registration-form'">Sign up</button>
    <button v-on:click="component='login-form'">Login</button>
    <component v-bind:is="component"></component>
  </div>
</template>

<script>
import registrationForm from './components/registrationForm.vue'
import loginForm from './components/loginForm.vue'

export default {
  components: {
    'registration-form': registrationForm,
    'login-form': loginForm,
  },
  data () {
    return {
      component: 'login-form',
    }
  },
  methods: {
  },
}
</script>

<style>

.input-form {
  width: 50%;
  margin: 0 auto;
  padding: 10px;
  border: 1px solid black;
  font-size: 20px;
}
form > div{
  padding: 20px;
  background: #eee;
  margin: 10px 0;
}
label {
  display: block;
  margin-top: 10px;
}
select {
  margin: 10px 0px;
  height: 30px;
  width: 20%;
  font-size: 20px;
}
input {
  width: 100%;
  height: 20px;
}
button {
  font-size: 20px;
  height: 40px;
  margin: 20px 0;
}
span {
  margin-left: 20px;
  color: red;
}
</style>
