<template>
  <header>
    <h1>{{ title }}</h1>
    <Button :color="showAddTask ? 'red' : 'green'" :text="showAddTask ? 'Close' : 'Add Task'"
            @btn-click="$emit('toggle-add-task')"/>
  </header>
</template>

<script>
import Button from "@/components/Button.vue";

export default {
  name: 'Header',
  props: {
    title: {
      type: String,
      default: "Task tracker",
    },
    showAddTask: Boolean
  },
  components: {
    Button
  }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-content: center;
  margin-bottom: 20px;
}
</style>