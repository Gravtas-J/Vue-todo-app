<template>
  <div>
    {{ task.text }}
    <button @click="deleteTask">Delete</button>
  </div>
</template>

<script>
export default {
  props: {
    task: Object
  },
  methods: {
    deleteTask() {
      this.$emit('delete-task', this.task.id);
    }
  }
};
</script>