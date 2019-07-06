<template>
  <div id="app">
    <div id="footer">
      <h4>{{ title }}</h4>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "Copyright, Flowerworld Inc."
    };
  }
};
</script>
}
</script>

<style>
#footer {
  background-color: grey;
  margin-top: 100px;
  padding: 1%;
}

.el-row h1 {
  color: black;
}

.el-row .el-col {
  direction: none;
}
</style>
