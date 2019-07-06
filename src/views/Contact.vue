<template>
  <div class="contact">
    <div class="container">
      <el-row>
        <el-col :span="24">
          <div class="grid-content bg-purple-dark">
            <h1>{{ title }}</h1>
          </div>
        </el-col>
      </el-row>
      <el-row :gutter="20">
        <el-col :span="12">
          <div class="grid-content-1 bg-purple">
            <h2>{{ ad }}</h2>
            <p>{{ address }}</p>
            <p>{{ phone }}</p>
          </div>
        </el-col>
        <el-col :span="12">
          <div class="grid-content-2 bg-purple">
            <p></p>
            <h2>{{ hours }}</h2>
            <ul>
              <li v-for="obj of operation">{{ obj.key }} : {{ obj.value }}</li>
            </ul>
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
      title: "Contact",
      address: "465 Richmond Road, ON K2Z 1A1",
      phone: "613-7274723",
      hours: "Hours of Operation",
      ad: "Address",
      operation: [
        {
          key: "Monday",
          value: "8:00-4:00pm"
        },

        {
          key: "Tuesday",
          value: "8:00-4:00pm"
        },
        {
          key: "Wednesday",
          value: "8:00-4:00pm"
        },
        {
          key: "Thursday",
          value: "8:00-4:00pm"
        },
        {
          key: "Friday",
          value: "8:00-4:00pm"
        },
        {
          key: "Saturday",
          value: "8:00-4:00pm"
        },
        {
          key: "Sunday",
          value: "Colosed"
        }
      ]
    };
  }
};
</script>

<style>
li {
  text-align: left;
  list-style: none;
}

p {
  text-align: left;
}
.grid-content h1 {
  margin-bottom: 1%;
}
</style>



