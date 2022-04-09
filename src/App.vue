<template>
  <div class="container">
    <div class="navbar">
      <NavBar />
    </div>
    <div class="mobile__navbar">
      <NavBarMobile />
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from "@/components/Nav-bar.vue";
import NavBarMobile from "@/components/Nav-bar-mobile.vue";
export default {
  components: {
    NavBar,
    NavBarMobile,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.mobile__navbar {
  display: none;
}
.navbar {
  display: flex;
}

@media (max-width: 640px) {
  .mobile__navbar {
    display: flex;
  }
  .navbar {
    display: none;
  }
}
</style>
