<template>
  <div class="home">
    <div class="container">
      <el-row>
        <el-col :span="24">
          <div class="grid-content bg-purple-dark">
            <h1>{{ title }}</h1>
          </div>
        </el-col>
      </el-row>
      <el-row :gutter="20">
        <el-col :span="8">
          <div class="grid-content-1 bg-purple">
            <img src="../assets/lotus.jpg">
          </div>
        </el-col>
        <el-col :span="16">
          <div class="grid-content-2 bg-purple">
            <p>{{ article1 }}</p>
          </div>
        </el-col>
      </el-row>
      <br>
      <el-row :gutter="20">
        <el-col :span="16">
          <div class="grid-content-2 bg-purple">
            <p>{{ article2 }}</p>
          </div>
        </el-col>
        <el-col :span="8">
          <div class="grid-content-1 bg-purple">
            <img src="../assets/tulips.jpg">
          </div>
        </el-col>
      </el-row>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      title: "About the Vue App",
      article1:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis velit purus, congue ut nibh in, suscipit accumsan magna. Ut enim nulla, suscipit consectetur ullamcorper non, congue et libero. Nunc efficitur tortor at tortor tincidunt, a vestibulum tellus fermentum. Maecenas laoreet justo id nibh viverra, ac posuere purus volutpat. Morbi iaculis facilisis efficitur. Morbi mollis porta massa ut dictum. Duis ultricies fringilla tellus, a vestibulum quam bibendum et. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Cras eu posuere dui. Etiam mauris sem, pharetra bibendum malesuada vitae, rutrum sed risus. Cras bibendum enim dictum tortor porta, sed accumsan ipsum vestibulum. Morbi maximus suscipit est, ut fermentum tortor placerat quis. Quisque lacinia fringilla condimentum.",
      article2:
        "Proin accumsan lectus eget tellus tincidunt rhoncus. In dolor nunc, commodo et quam quis, pulvinar lobortis nisl. Nunc pharetra lorem risus, eget rhoncus lectus bibendum eget. Proin ornare orci sed urna aliquet finibus. Sed tincidunt suscipit justo, ut consequat elit bibendum quis. Suspendisse sed magna vel justo fringilla eleifend. Phasellus ultrices euismod metus quis vestibulum. Nunc vulputate vel enim eu iaculis. Phasellus fermentum sem at mollis fermentum. Donec fermentum quam sit amet dolor laoreet, ut ultricies mi blandit. Quisque vehicula vehicula enim pulvinar scelerisque. Nullam tincidunt augue ipsum, id blandit orci molestie at. Integer non mauris ut risus consectetur efficitur hendrerit ac nulla. Integer fringilla leo in nulla maximus interdum."
    };
  }
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
}
.container {
  padding: 10%;
  padding-top: 0;
  display: block;
  margin: auto;
  max-width: 1170px;
}

.grid-content-1 img {
  width: 100%;
}

.container el-row:nth-child(2) {
  margin-bottom: 10%;
}
</style>





