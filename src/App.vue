<template>
  <div id="app">
    <div>
      <el-menu :default-active="'Home'" mode="horizontal" router>
        <el-menu-item
          :index="route.name"
          :route="route"
          v-for="(route, index) in $router.options.routes"
          :key="index">{{ route.name }}</el-menu-item>
      </el-menu>
    </div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
