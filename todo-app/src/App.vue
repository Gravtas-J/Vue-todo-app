<template>
  <div>
    <task-input @add-task="addTask" />
    <task-list :tasks="tasks" @delete-task="deleteTask" />
  </div>
</template>

<script>
import TaskInput from './components/TaskInput.vue';
import TaskList from './components/TaskList.vue';

export default {
  components: {
    TaskInput,
    TaskList
  },
  data() {
    return {
      tasks: []
    };
  },
  methods: {
    addTask(taskText) {
      const newTask = { id: Date.now(), text: taskText };
      this.tasks.push(newTask);
    },
    deleteTask(taskId) {
      this.tasks = this.tasks.filter(task => task.id !== taskId);
    }
  }
};
</script>