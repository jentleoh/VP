<template>
  <div>
    <div>
      <b-form-input
        v-model="text"
        label="Enter your name"
        placeholder="Enter your name"
      />
      <b-modal
        id="modal-1"
        title="BootstrapVue"
      />
    </div>

    <div>
      <b-form-input
        v-model="text"
        placeholder="Enter your tel"
      />

      <b-modal
        id="modal-1"
        title="BootstrapVue"
      />
    </div>

    <div>
      <b-form-input
        v-model="text"
        placeholder="Enter your email"
      />
      <b-modal
        id="modal-1"
        title="BootstrapVue"
      />
    </div>
    <div>
      <b-form-input
        v-model="text"
        placeholder="Enter your date"
      />
      <b-button v-b-modal.modal-1>
        완료
      </b-button>

      <b-modal
        id="modal-1"
        title="BootstrapVue"
      />
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
export default class AlertForm extends Vue {
  text = ''
}
</script>
