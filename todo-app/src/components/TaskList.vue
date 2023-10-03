<template>
  <div>
    <task-item v-for="task in tasks" :key="task.id" :task="task" />
  </div>
</template>

<script>
import TaskItem from './TaskItem.vue';

export default {
  props: {
    tasks: Array
  },
  components: {
    TaskItem
  }
};
</script>