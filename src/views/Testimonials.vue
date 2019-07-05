<template>
  <div>
    <h1>{{ title }}</h1>

    <el-row>
      <el-col v-for="(testimonial, index) of testimonials" :key="index" :span="12">
        <div class="current_comment">
          <h4>{{ testimonial.name }} - {{ testimonial.position }}</h4>
          <p>{{ testimonial.comment }}</p>
        </div>
      </el-col>
    </el-row>

    <el-form
      :model="ruleForm"
      :rules="rules"
      v-show="!dialogVisible"
      ref="ruleForm"
      label-width="120px"
      class="demo-ruleForm"
    >
      <div class="top">
        <el-form-item label="Name" prop="name">
          <el-input v-model="ruleForm.name"></el-input>
        </el-form-item>
        <el-form-item label="Job Title" prop="position">
          <el-input v-model="ruleForm.position"></el-input>
        </el-form-item>
      </div>
      <el-form-item label="Comments" prop="comment">
        <el-input type="textarea" v-model="ruleForm.comment"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="submitForm('ruleForm')">Submit</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>
<script>
import Todo from "@/components/Todo.vue";
import TodoForm from "@/components/TodoForm.vue";
import axios from "axios";
export default {
  data() {
    return {
      title: "Testimonials",
      ruleForm: {
        name: "",
        position: "",
        comment: ""
      },
      rules: {
        name: [
          {
            required: true,
            message: "Please input first name",
            trigger: "blur"
          },
          {
            min: 3,
            max: 50,
            message: "Length should be 3 to 50",
            trigger: "blur"
          }
        ],
        position: [
          {
            required: true,
            message: "Please input last name",
            trigger: "blur"
          },
          {
            min: 3,
            max: 50,
            message: "Length should be 3 to 50",
            trigger: "blur"
          }
        ],
        comment: [
          {
            required: true,
            message: "Please input Claim Request Content form",
            trigger: "blur"
          },
          {
            min: 3,
            max: 120,
            message: "Length should be 3 to 120",
            trigger: "blur"
          }
        ]
      },
      testimonials: []
    };
  },
  components: {
    Todo,
    TodoForm
  },
  methods: {
    appDeleteTodo(index) {
      this.todoList.splice(index, 1);
      axios.put(
        "https://midterm-b7693.firebaseio.com/data.json",
        this.todoList
      );
    },

    submitForm(formName) {
      this.$refs[formName].validate(valid => {
        if (valid) {
          this.testimonials.push(this.ruleForm);
          console.log(this.testimonials);
          axios
            .put(
              "https://midterm-b7693.firebaseio.com/data.json",
              this.testimonials
            )
            .then(response => {
              console.log(response);
              console.log("Your data was saved status: " + response.status);
            })
            .catch(error => {
              console.log(error);
            });
        } else {
          console.log("error submit!!");
          return false;
        }
      });
    }
  },

  created() {
    axios
      .get("https://midterm-b7693.firebaseio.com/data.json")
      .then(response => {
        console.log(response.data);
        if (response.data) {
          this.testimonials = response.data;
        }
      })
      .catch(error => {
        console.log(" there are and error in getting data: " + error.response);
      });
  }
};
</script>
<style>
.current_comment {
  background-color: #999;
  width: 50%;
  margin: 0 auto;
}
form {
  margin: 0 auto;
  width: 800px;
  padding: 1em;
  border: 1px solid #ccc;
  border-radius: 1em;
}

label {
  display: inline-block;
  width: 90px;
  text-align: right;
}

input,
textarea {
  font: 1em sans-serif;
  width: 300px;
  box-sizing: border-box;
  border: 1px solid #999;
}

input:focus,
textarea:focus {
  border-color: #000;
}

textarea {
  vertical-align: top;
  height: 5em;
}

.button {
  padding-left: 90px;
}

button {
  margin-left: 0.5em;
}
.top {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-between;
}

el-col {
}
</style>

