<template>
  <div class="wrapper">
    <side-bar>
      <mobile-menu slot="content"></mobile-menu>
      <sidebar-link to="/admin/overview">
        <i class="nc-icon nc-grid-45"></i>
        <p>Dashboard</p>
      </sidebar-link>
      <!--sidebar-link to="/gter">
        <i class="nc-icon nc-circle-09"></i>
        <p>WEB APP</p>
      </sidebar-link-->
      <li class="router-link-exact-active nav-item">
        <a href="https://simile.como.polimi.it/SimileWebAdministrator2/" class="nav-link" target="_blank">
          <i class="nc-icon nc-mobile"></i>
          <p>WEB APP SIMILE</p>
        </a>
      </li>
      <li class="router-link-exact-active nav-item">
        <a href="https://simile.como.polimi.it/SimileWebAdministrator2/" class="nav-link" target="_blank">
          <!--i class="fa fa-map"></i-->
          <i class="nc-icon nc-map-big"></i>
          <p>WEBGIS DATI SAT</p>
        </a>
      </li>
      <!--sidebar-link to="/admin/user">
        <i class="nc-icon nc-circle-09"></i>
        <p>User Profile</p>
      </sidebar-link-->
      <sidebar-link to="/admin/lago-maggiore">
        <i class="nc-icon nc-tag-content"></i>
        <p>Lago Maggiore</p>
      </sidebar-link>
      <sidebar-link to="/admin/lago-lugano">
        <i class="nc-icon nc-tag-content"></i>
        <p>Lago di Lugano</p>
      </sidebar-link>
      <sidebar-link to="/admin/lago-como">
        <i class="nc-icon nc-tag-content"></i>
        <p>Lago di Como</p>
      </sidebar-link>
      <!--sidebar-link to="/admin/maps">
        <i class="nc-icon nc-pin-3"></i>
        <p>Maps</p>
      </sidebar-link-->
      <!--sidebar-link to="/admin/notifications">
        <i class="nc-icon nc-bell-55"></i>
        <p>Notifications</p>
      </sidebar-link-->

      <!--template slot="bottom-links">
        <sidebar-link class="active"
                      to="/admin/upgrade">
          <i class="nc-icon nc-alien-33"></i>
          <p>Upgrade to PRO</p>
        </sidebar-link>
      </template-->
    </side-bar>
    <div class="main-panel">
      <top-navbar></top-navbar>

      <dashboard-content @click="toggleSidebar">

      </dashboard-content>

      <content-footer></content-footer>
    </div>
  </div>
</template>
<style lang="scss">

</style>
<script>
  import TopNavbar from './TopNavbar.vue'
  import ContentFooter from './ContentFooter.vue'
  import DashboardContent from './Content.vue'
  import MobileMenu from './MobileMenu.vue'
  export default {
    components: {
      TopNavbar,
      ContentFooter,
      DashboardContent,
      MobileMenu
    },
    methods: {
      toggleSidebar () {
        if (this.$sidebar.showSidebar) {
          this.$sidebar.displaySidebar(false)
        }
      }
    }
  }

</script>
