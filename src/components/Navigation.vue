<template>
  <div id="app">
    <div id="nav">
      <div class="navcontainer">
        <el-row>
          <el-col :span="8">
            <div class="grid-content bg-purple-light">
              <h1>Flowerworld</h1>
            </div>
          </el-col>
          <el-col :span="4">
            <div class="grid-content bg-purple">
              <router-link to="/">
                <h3>Home</h3>
              </router-link>
            </div>
          </el-col>
          <el-col :span="4">
            <div class="grid-content bg-purple-light">
              <router-link to="/about">
                <h3>About</h3>
              </router-link>
            </div>
          </el-col>
          <el-col :span="4">
            <div class="grid-content bg-purple">
              <router-link to="/contact">
                <h3>Contact</h3>
              </router-link>
            </div>
          </el-col>
          <el-col :span="4">
            <div class="grid-content bg-purple-light">
              <router-link to="/testimonials">
                <h3>Testimonials</h3>
              </router-link>
            </div>
          </el-col>
        </el-row>
      </div>
    </div>
  </div>
</template>

<style>
.navcontainer {
  max-width: 1170px;
  margin: auto;
}
#nav {
  background-color: grey;
  box-sizing: border-box;
  padding: 0px;
}

.el-row h1 {
  color: black;
  margin-top: 2%;
}

div.grid-content h3 {
  color: white;
  border-left: 1px solid black;
  border-right: 1px solid black;
  padding: 10%;
}
div.grid-content h3:last {
  border-right: 1px solid black;
}
div.grid-content a:link {
  text-decoration: none;
  color: black;
}
div.grid-content a:active h3 {
  color: black;
  border-bottom: 1px solid black;
}
</style>
