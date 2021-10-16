<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about" exact-active-class="ttt">About</router-link> |
      <router-link to="/book">BookList</router-link> |
      <router-link to="/user/profile">User</router-link>
    </div>
    <div class="border-b">
      <router-view />
    </div>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }

    &.router-link-active.ttt {
      color: #0000ff;
    }
  }
}

.border-b {
  border: 1px blue solid;
}
</style>
