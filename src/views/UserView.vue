<template>
  <div id="user">
    <Navbar />
    <User />
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import User from '@/components/User.vue'

export default {
    name: 'UserView',
    components: {
        Navbar, 
        User
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  #user {
    display: flex;
  }
</style>