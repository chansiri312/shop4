<template>
  <div align="center">
    <b-button variant="primary" @click="login">Login </b-button>
  
  </div>
</template>
<script>
import firebase from 'firebase/app'
import { auth } from '@/plugins/firebaseConfig.js'

export default {
  methods: {
    login() {
      const provider = new firebase.auth.GoogleAuthProvider()
      auth
        .signInWithPopup(provider)
        .then((result) => {
         
          const credential = result.credential
       
          const token = credential.accessToken
          console.log('token=' + token)
         
          const user = result.user
          console.log('user=' + user)
          this.$router.replace('/home')
          // ...
        })
        .catch((error) => {
          // Handle Errors here.
          const errorCode = error.code
          console.log('error=' + errorCode)
        
          //   // ...
        })
    },
    logout() {
      firebase
        .auth()
        .signOut()
        .then(() => {
          // Sign-out successful.
          console.log('sign-out successful')
        })
        .catch((error) => {
          // An error happened.
          console.log(error)
        })
    },
  },
}
</script>
