<template>
  <div class="home">
     <el-row>
   <el-row>
  <el-col :span="24"><div class="grid-content bg-purple-dark"> <h1>{{ title }}</h1></div></el-col>
</el-row>
</el-row>
    <div class="container">
     
      <el-row :gutter="20">
        <el-col :span="12">
          <div class="grid-content-1 bg-purple"><img src="../assets/flowers.jpg"></div>
        </el-col>
        <el-col :span="12">
          <div class="grid-content-2 bg-purple"><p>{{ article }}
            </p></div>
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>


export default {
    data() {
        return {
            title:"Welcome to My Vue App",
            article: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis velit purus, congue ut nibh in, suscipit accumsan magna. Ut enim nulla, suscipit consectetur ullamcorper non, congue et libero. Nunc efficitur tortor at tortor tincidunt, a vestibulum tellus fermentum. Maecenas laoreet justo id nibh viverra, ac posuere purus volutpat. Morbi iaculis facilisis efficitur. Morbi mollis porta massa ut dictum. Duis ultricies fringilla tellus, a vestibulum quam bibendum et. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Cras eu posuere dui. Etiam mauris sem, pharetra bibendum malesuada vitae, rutrum sed risus. Cras bibendum enim dictum tortor porta, sed accumsan ipsum vestibulum. Morbi maximus suscipit est, ut fermentum tortor placerat quis. Quisque lacinia fringilla condimentum.",
        };
}
};

</script>

<style>

* {
    margin: 0;
    padding: 0;
}
.container{
  padding:10%;
  padding-top:0;
  display: block;
  margin:auto;
  max-width:1170px;
}

.grid-content-1 img{
width:100%;
}








