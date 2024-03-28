<script >

export default {
  data() {
    return {
      email: '',
      isValid: false,
      emailColor: '',
      validColor: 'green',
      invalidColor: 'red',

    }
  },

  methods: {

    checkEmail() {
      let inputEmail = prompt('Enter your email:');
      if (inputEmail !== null) {
        this.email = inputEmail.trim();
        this.isValid = this.validateEmail(this.email)
        this.emailColor = this.isValid ? 'green' : 'red';
      }
    },

    validateEmail(email) {
      const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      return emailPattern.test(email);
    },
    reset() {
      this.email = '';
      this.isValid = false;
      this.emailColor = '';
    },

  },
}


</script>

<template>
  <header>
    <div> <button class="email" @click="checkEmail">Input Email</button> </div>
    <h1 :style="{ border: isValid ? '2px solid green' : '2px solid red' }">{{ email }}</h1>
    <h4 v-if="email" :style="{ color: validColor }">{{ isValid ? 'The email is valid' : '' }} </h4>
    <h4 v-if="email" :style="{ color: invalidColor }">{{ isValid ? '' : 'The email is invalid' }}</h4>
    <button @click="reset">Reset</button>


  </header>

  <main>
    <TheWelcome />



  </main>
</template>

<style>
.email {
  margin-bottom: 5px;

  width: 150px;

}
</style>
