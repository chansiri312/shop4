<template>
  <div>
    <div class="container">
        <b-row>
     <Order />
        </b-row> 
    </div>
    
  </div>
</template>

<script>
import Order from '@/components/O1.vue'
import firebase from 'firebase/app'

export default {
  components: {
    Order,
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