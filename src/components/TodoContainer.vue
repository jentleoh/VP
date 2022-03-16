<template>
  <div>
    <h1>TodoContainer</h1>
    <TodoItem />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TodoItem from '@/components/TodoItem.vue';

@Component({
  components: {
    TodoItem,
  },
})
export default class TodoContainer extends Vue {
}
</script>
