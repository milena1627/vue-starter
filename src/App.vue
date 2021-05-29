<template>
  <div >
    <h1>Witaj w systemie do zapisow na zajecia</h1>  
    <div 
  <div v-if="authenticated" >
    <h3> Zalogowany jako {{email}}</h3>
    <a @click="logOut()">Wyloguj</a>
    </div>

    <div v-else>
      Zaloguj sie:
    <input type="email" v-model="email">   
    <button @click="logIn()"> Zaloguj sie</button>
  </div>
  </div>

</template>

<script>

export default {

  data() {
  return {
    authenticated: false,
    email: ''

  };
},
methods: {
  logIn() {
    this.authenticated=true;
  },

  logOut() {

    this.authenticated = false;
    this.email = '';
  }
}
 
};

</script>

<style>

</style>
