<template>
  <div id="app">
    <h1>タスク一覧</h1>
    <ul>
      <li v-for="task in tasks" :key="task.id">
        <input type="checkbox" :checked="task.done">
        {{ task.name }}
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  computed: {
    tasks () {
      return this.$store.state.tasks; // ストアのステートtasksを返し、テンプレート内で使用できるようにしている。
    },
  },
}
</script>
