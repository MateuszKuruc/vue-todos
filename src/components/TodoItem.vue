<script setup>
import { defineProps } from "vue";
import { Icon } from "@iconify/vue";

const props = defineProps({
  todo: {
    type: Object,
    required: true,
  },
});
</script>

<template lang="">
  <li>
    <input type="checkbox" :checked="todo.isCompleted" />
    <div class="todo">
      <input type="text" :value="todo.todo" />
      <span>
        {{ todo.todo }}
      </span>
    </div>
    <div class="todo-actions">
        <Icon icon="ph:check-circle" color="#41b080" width="22" />
    </div>
  </li>
</template>

<style lang="scss" scoped></style>
