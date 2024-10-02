<template>
  <form @submit.prevent="handleSubmit">
    <input type="text" placeholder="I need to..." v-model="newTask" />
    <button>Add</button>
  </form>
</template>

<script>
import { useTaskStore } from '@/stores/TaskStore';
import { ref } from 'vue';

  export default {
    setup(){
 const taskStore = useTaskStore()
    const newTask = ref('')
    const handleSubmit = () => {
      if (newTask.value.length > 0) {
        taskStore.addTask({
          title: newTask.value,
          isFav: false,
          id: Math.floor(Math.random() * 1000000)
        })
        newTask.value = ""
      }
    }
    return {handleSubmit, newTask}
    }

  }
</script>

<!-- Uncaught TypeError: taskStore.addTask is not a function というエラーが出た。 -->
<!-- 原因は定数taskStoreの値の最後に関数を表す()が抜けていた -->
