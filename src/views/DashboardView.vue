<template>
    <div id="dashboard">
        <Navbar />
        <Home />
    </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Home from '@/components/Home.vue'

export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Dashboard',
    components: {
        Navbar,
        // eslint-disable-next-line vue/no-unused-components
        Home
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  #dashboard {
    display: flex;
  }

</style>