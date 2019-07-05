<template>
  <ul>
    <li v-for="(index, todo) in todos" :key="index" @click="todoDone(index)">{{index}} - {{ todo }}</li>
  </ul>
</template>
<script>
export default {
  props: {
    todos: {
      type: Array,
      required: true
    }
  },
  methods: {
    todoDone(index) {
      console.log(index);
      //$emit emots and event from the child component to the parent component
      this.emit("removeTodo", index);
    }
  }
};
</script>