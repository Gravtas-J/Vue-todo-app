<template>
  <form @submit.prevent="addTask">
    <input v-model="newTask" placeholder="Add a new task" />
  </form>
</template>

<script>
export default {
  data() {
    return {
      newTask: ''
    };
  },
  methods: {
    addTask() {
      this.$emit('add-task', this.newTask);
      this.newTask = '';
    }
  }
};
</script>