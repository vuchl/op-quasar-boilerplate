<template>
<div id="login-full-page">
  <div class="card bg-white" id="login-card">
    <div class="card-title bg-primary text-white">
      Kalkulationsprogramm
    </div>
    <div class="card-content card-force-top-padding">
      <div class="floating-label">
        <input required class="full-width" v-model="user.name"/>
        <label>Kennung</label>
      </div>
      <div class="floating-label">
        <input type="password" required class="full-width" v-model="user.password"/>
        <label>Passwort</label>
      </div>
      <label id="rememberme-container">
        <q-checkbox v-model="user.rememberme"></q-checkbox>
        Remember Me?
      </label>
      <button class="primary full-width" @click.prevent.stop="submit">Login</button>
      <div id="version-tag">
        <small>Version v0.0.x</small>
      </div>
    </div>
</div>
</template>

<script type="text/javascript">
export default {
  name: 'LoginPage',
  data () {
    return {
      user: {
        name: '',
        password: '',
        rememberme: false
      }
    }
  },
  methods: {
    submit () {
      console.log('submit the login')
    }
  }
}
</script>

<style scoped>

#login-full-page {
  height: 100vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: url('/statics/bg.jpg') no-repeat center center fixed; 
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}
#login-card {
  width: 400px;
}
#rememberme-container {
  margin-top: 50px;
}
button {
  margin-top: 15px;
  margin-bottom: 15px;
}
</style>