<template>
  <q-page padding class="row bg-grey-1 justify-left">
    <div class="col-10">
      <todo-list></todo-list>
    </div>
  </q-page>
</template>

<script>
import TodoList from "components/todoList";
export default {
  name: "task",
  components: {
    TodoList,
  },
};
</script>
