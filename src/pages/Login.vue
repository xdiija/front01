<template>
  <q-page class="flex flex-center bg-primary">
    <q-card style="width: 300px; height: auto; display: flex; flex-direction: column; align-items: center">
      <img src="../assets/Logo.jpg" ratio='1' width='200px'>

      <q-card-section class="q-pt-none">
        <div class="text-h5">Login</div>
      </q-card-section>

      <q-card-section class="q-pt-none full-width">
        <q-input filled v-model="login.email" label="Nick" />
        <q-input class="q-mt-sm" v-model="login.password" filled label="Password" :type="login.isPwd ? 'password' : 'text'">
        <template v-slot:append>
          <q-icon
            :name="login.isPwd ? 'visibility_off' : 'visibility'"
            class="cursor-pointer"
            @click="login.isPwd = !login.isPwd"
          />
        </template>
      </q-input>
      </q-card-section>
      <q-card-actions class="full-width">
         <q-btn class="q-mx-sm" color="primary" label="Submit" @click="$router.push({ name: 'home' })" style="width: 100%" />
      </q-card-actions>
      <q-card-actions class="full-width">
         <q-btn flat class="q-mx-sm" color="primary" label="Forgot Password?" @click="$router.push({ name: 'forgotPw'})" style="width: 100%" />
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-img src="https://cdn.quasar.dev/img/parallax2.jpg">
        <div class="absolute-bottom text-subtitle2 text-center">
          Title
        </div>
      </q-img>
    </q-card>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      login: {
        email: '',
        password: '',
        isPwd: true
      }
    }
  },
  methods: {
  }
}
</script>
