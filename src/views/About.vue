<template>
  <div>
    <b-form-input
      v-model="text"
      placeholder="Enter your name"
    />
    <div class="mt-2">
      Value: {{ text }}
    </div>

    <b-button v-b-modal.modal-1>
      보기
    </b-button>

    <b-modal
      id="modal-1"
      title="BootstrapVue"
    >
      <p class="my-4">
        {{ text }}
      </p>
    </b-modal>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
export default class About extends Vue {
  text = ''
}
</script>
