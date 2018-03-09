<template>
  <el-row>
    <el-col :span="8"><div class="grid-content bg-purple"></div><br/></el-col>
    <el-col :span="8">
      <div class="grid-content bg-purple-light">
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <span>Login</span>
            <!-- <el-button style="float: right; padding: 3px 0" type="text">Operation button</el-button> -->
          </div>
          <div>
              <div style="margin-top: 15px;">
                <el-input
                  placeholder="User"
                  v-model="user">
                  <!-- icon icon-user from at-ui-style -->
                  <i slot="prefix" class="el-input__icon icon icon-user"></i>
                </el-input>
              </div>
              <div style="margin-top: 15px;">
                <!-- <el-input placeholder="Password" type="password" v-model="password" auto-complete="off"></el-input> -->
                <el-input
                  placeholder="Password"
                  type="password"
                  v-model="password"
                  auto-complete="off">
                  <!-- icon icon-user from at-ui-style -->
                  <i slot="prefix" class="el-input__icon icon icon-lock"></i>
                </el-input>
              </div>
              <div style="margin-top: 15px;">
                <el-button type="primary" style="float: right">Login</el-button>
              </div>
              <br/>
                <!-- <el-button slot="prepend" icon="el-icon-search"></el-button> -->


          </div>
        </el-card>

      </div>
    </el-col>
    <el-col :span="8"><div class="grid-content bg-purple"></div></el-col>
  </el-row>
</template>

<script>
export default {
  name: 'Login',
  data () {
    return {
      user: '',
      password: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<!-- <style>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #35495E;
}
</style>
-->
