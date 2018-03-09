<template>
  <!-- <div id="app"> -->
    <el-container id="app">
      <!-- <el-aside > -->
        <el-row class="tac">
          <el-col :span="24" v-for="(route, index) in routes" :key="index">
            <el-menu
              default-active="1"
              class="el-menu-vertical-demo"
              :router="true"
              >
              <el-menu-item index="index" :route="route" @click="handleOpen">
                <i class="el-icon-menu"></i>
                <span>{{route.name}}</span>
              </el-menu-item>
            </el-menu>

          </el-col>
        </el-row>

      <!-- </el-aside> -->
      <el-main>
        <!-- <el-button @click="startHacking">Start</el-button> -->
        <router-view></router-view>
      </el-main>
    </el-container>
    <!-- <img src="./assets/logo.png"> -->
  <!-- </div> -->
</template>

<script>
export default {
  name: 'app'
}
</script>
<script>
export default {
  created() {
      this.$router.options.routes.forEach(route => {
          this.routes.push({
              name: route.name,
              path: route.path
          })
      })
  },
  data () {
      return {
          routes: []
      }
  },
  methods: {
  //   startHacking () {
  //     this.$notify({
  //       title: 'It works!',
  //       type: 'success',
  //       message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
  //       duration: 5000
  //     })
  //   }
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}
</style>
