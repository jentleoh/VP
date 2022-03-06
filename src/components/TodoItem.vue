<template>
  <div>
    <h2>TodoItem</h2>
    {{ msg }}
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class TodoItem extends Vue {
  @Prop() private msg!: string;
}
</script>
