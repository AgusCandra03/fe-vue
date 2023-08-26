<template>
    <div id="report">
      <Navbar />
      <Report />
    </div>
  </template>
  
  <script>
  import Navbar from '@/components/Navbar.vue'
  import Report from '@/components/Report.vue'
  
  export default {
      name: 'UserView',
      components: {
          Navbar, 
          // eslint-disable-next-line vue/no-unused-components
          Report
      }
  }
  </script>
  
  <style>
  * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
  
    #report {
      display: flex;
    }
  </style>