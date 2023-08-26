<template>
  <div id="navbar">
    <aside>
      <div class="logo">
        <router-link class="navbar-brand" to="/dashboard">
          <img src="../assets/logo.png" alt="">
        </router-link>
      </div>

      <hr>

      <div class="menu">
        <router-link class="buttton" to="/dashboard" v-b-tooltip.hover.right title="Dashboard">
          <i class='tooltip bx bxs-home'></i>
        </router-link>
        <router-link class="buttton" to="/user" v-b-tooltip.hover.right title="Employee's">
          <i class='tooltip bx bxs-user'></i>
        </router-link>
        <router-link class="buttton" to="/report" v-b-tooltip.hover.right title="Report's">
          <i class='tooltip bx bxs-edit'></i>
        </router-link>
        <router-link class="buttton" to="/message" v-b-tooltip.hover.right title="Message / Notification">
          <i class='tooltip bx bxs-envelope'></i>
        </router-link>
      </div>

      <div class="flex"></div>

      <div class="menu">
        <router-link class="buttton" @click.native="logout" to="" v-b-tooltip.hover.right title="Log out ?">
            <i class='tooltip bx bx-exit' ></i>
        </router-link>
      </div>
    </aside>
  </div>
</template>
  
<script>
import swal from 'sweetalert'

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'NavbarMenu',
  methods: {
    logout(){
      swal({
        title: "Are you sure you want to logout ?",
        text: "Please confirm if you are want to logout.",
        icon: "info",
        buttons: true,
      })
      .then((willLogout) => {
        if (willLogout) {
          window.location.href = "/"; 
        }
      });
    },
    ToggleMenu(){
      alert('google');
    }
  }
}
</script>

<style>
aside {
  display: flex;
  flex-direction: column;
  width: calc(2rem + 32px);
  min-height: 100vh;
  background-color: blue;
  color:white;
  overflow: hidden;
  padding: 1rem;
  transition: 0.2s ease-out;
  /* position: fixed; */
  float: left;
  z-index: 1;
}

.logo img {
  width: 2rem;
  margin-bottom: 1rem;
}

.menu-toggle {
  font-size: 30px;
  margin-bottom: 1rem;
}

.menu i {
  font-size: 30px;
  color: white;
  opacity: 1;
  margin-bottom: 1rem;
}

.menu i:hover {
  opacity: 0.6;
}

.flex {
  flex: 1 1 0;
}


</style>