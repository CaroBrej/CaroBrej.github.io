<template>
  <nav>
    <router-link to="/">Home</router-link>
    <div class="navmenu">
      <img
        class="menuimg"
        @click="menushow"
        alt="menu button"
        src="../assets/navbarmenu.png"
      />
    </div>
    <div class="scroll__menu" :style="vis">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      opened: false,
      vis: { visibility: "hidden" },
    };
  },
  methods: {
    menushow() {
      if (this.opened == true) {
        this.opened = false;
        this.vis = { visibility: "hidden" };
      } else {
        this.opened = true;
        this.vis = { visibility: "visible" };
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  width: 100vw;
  max-height: 5vh;
  top: 0;
  font-size: 1.7rem;
  background-color: rgb(8, 158, 204);
}

a {
  text-decoration: none;
  color: white;
  margin-right: 5%;
  width: 100%;
}

.navmenu {
  display: flex;
  width: 30%;
  justify-content: end;
  margin-right: 5%;
}

.menuimg {
  height: 90%;
  align-self: center;
}

.scroll__menu {
  height: 100vh;
  width: 70%;
  padding: 20px;
  display: flex;
  position: fixed;
  text-align: center;
  flex-direction: column;
  background-color: rgb(0, 120, 156);
  row-gap: 10px;
  z-index: 10;
}
</style>
