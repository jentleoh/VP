<template>
  <div>
    <h1>TodoContainer</h1>
    <b-form-input v-model="inputMsg" />
    <b-button @click="addTodoList">
      추가하기
    </b-button>

    <TodoItem
      v-for="todoItem in todoList"
      :key="todoItem.id"
      :todo-item="todoItem"
    />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TodoItem, { Todo } from '@/components/TodoItem.vue';

@Component({
  components: {
    TodoItem,
  },
})
export default class TodoContainer extends Vue {
  private todoList:Array<Todo> = []

  private idGenerator = 0;

  private inputMsg = '';

  addTodoList(): void {
    if (this.inputMsg !== '') {
      const newId = this.idGenerator + 1;

      this.todoList.push({ id: newId, msg: this.inputMsg });
      this.idGenerator = newId;
      this.inputMsg = '';
    }
  }
}
</script>
