<template>
  <div class="home">
    <HelloWorld />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/H1.vue'
import firebase from 'firebase/app'
export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  beforeCreate() {
    firebase.auth().onAuthStateChanged((user) => {
      if (user != null) {
        // User is signed in.
        // ให้แสดงชื่อ email รูป
      } else {
        // No user is signed in.
        // กลับไปหน้า login
        this.$router.replace('/')
      }
    })
  },
}
</script>
