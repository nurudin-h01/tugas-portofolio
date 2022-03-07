<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light " style="background-color: #645193ff;">
      <div class="container-fluid">
        <button class="navbar-toggler" type="button" >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0 mx-auto">
        <div class="d-flex">
          <div id="nav" class="d-flex flex-end">
          <li class="nav-item me-3">
            <router-link class="nav-link " to="/">Home</router-link>
          </li>
          <li class="nav-item me-3">
            <router-link class="nav-link" to="/contact">Contact</router-link>
          </li>
          <li class="nav-item me-3">
            <router-link class="nav-link" to="/detail">Detail Project</router-link>
          </li>
        </div>
        </div>
        </ul>
    </div>
  </div>
</nav>
    <router-view/>
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
  padding: 10px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: white;
    }
  }
}
</style>
