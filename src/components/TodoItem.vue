<template>
  <div>
    {{ todoItem.msg }}
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

export type Todo = {
  id: number,
  msg: string
}

@Component
export default class TodoItem extends Vue {
  @Prop() private todoItem!: Todo;
}
</script>
