<template>
  <div id="app">
    <Kanban :data="data" :create_task_submit="create_task_submit" />
  </div>
</template>

<script>
import Kanban from "./components/Kanban";

export default {
  name: "App",
  components: {
    Kanban,
  },
  data() {
    return {
      data: [
        {
          name: "Todo",
          color: "#F9ACC0",
          tasks: [{
            task_name: "test"
          }],
        },
        {
          name: "Doing",
          color: "#86A5C4",
         tasks: [{
            task_name: "test"
          }],
        },
        {
          name: "Done",
          color: "#C4B3C3",
          tasks: [{
            task_name: "test"
          }],
        },
      ],
    };
  },
  methods: {
    create_task_submit(column_index, item) {
      this.data[column_index].tasks.push(item);
    },
  },
};
</script>

<style>
#app {
  height: 100vh;
}
</style>
