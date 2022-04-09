<template>
  <nav>
    <router-link to="/">Home</router-link>
    <div class="navmenu">
      <router-link to="/about">About</router-link>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  width: 100vw;
  top: 0;
  font-size: 1.7rem;
  background-color: rgb(8, 158, 204);
}

a {
  text-decoration: none;
  color: white;
  margin-right: 5%;
}

.navmenu {
  display: flex;
  width: 30%;
  justify-content: end;
  margin-right: 5%;
}
</style>
