<template>
  <TodoContainer />
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TodoContainer from '@/components/TodoContainer.vue'; // @ is an alias to /src

@Component({
  components: {
    TodoContainer,
  },
})
export default class TodoPage extends Vue {}
</script>
