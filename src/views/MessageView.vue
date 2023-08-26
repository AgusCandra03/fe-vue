<template>
    <div id="message">
      <Navbar />
      <Message />
    </div>
  </template>
  
  <script>
  import Navbar from '@/components/Navbar.vue'
  import Message from '@/components/Message.vue'
  
  export default {
      name: 'UserView',
      components: {
          Navbar, 
          Message
      }
  }
  </script>
  
  <style>
  * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
  
    #message {
      display: flex;
    }
  </style>