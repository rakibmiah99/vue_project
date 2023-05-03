<script>
  import {RouterLink} from "vue-router";
  import cogoToast from "cogo-toast";
  export default {
    data(){
      return {
          username: '',
          password: ''
      }
    },

    methods: {
      handleForm() {
        cogoToast.success("hello")
        console.log({
          username: this.username,
          password: this.password
        })
      }
    }
  }
</script>
<template>
    <div class="auth-area d-flex justify-content-center align-items-center vh-100">
        <form @submit.prevent="handleForm()" class="auth-form">
            <div class="form-group d-flex flex-column">
              <label class="label">User Name</label>
              <input type="text" v-model="username" name="username" class="form-control">
            </div>
            <div class="form-group mt-3 d-flex flex-column">
              <label class="label">Password</label>
              <input v-model="password" type="text" name="password" class="form-control">
            </div>

            <div class="form-group mt-3 d-flex flex-column">
              <button class="btn btn-primary w-100">Login</button>
            </div>
        </form>
    </div>
</template>


<style>
  .auth-form{
    height: 400px;
    width: 400px;
  }
  .label{
    margin-bottom: 7px;
  }
</style>
