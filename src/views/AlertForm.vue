<template>
  <div>
    <b-form-group label-cols="4" label-cols-lg="2" label="NAME" label-for="input-default">
    <b-form-input
      v-model="name"
      placeholder="Enter your Name"
    />
    </b-form-group>
        <b-form-group label-cols="4" label-cols-lg="2" label="TEL" label-for="input-default">

    <b-form-input
      v-model="tel"
      placeholder="Enter your TEL"
    />
    </b-form-group>
        <b-form-group label-cols="4" label-cols-lg="2" label="Email" label-for="input-default">

    <b-form-input
      v-model="email"
      placeholder="Enter your Email"
    />
    </b-form-group>
        <b-form-group label-cols="4" label-cols-lg="2" label="DATE" label-for="input-default">

    <b-form-input
      v-model="date"
      placeholder="Enter your DATE"
    />
    </b-form-group>
    <div class="mt-2">
      Value: {{ name }} {{ tel }} {{ email }} {{ date }}
    </div>
    <b-button variant="danger" v-b-modal.modal-1>
      완료
    </b-button>

    <b-modal
      id="modal-1"
      title="BootstrapVue"
    >
      <p class="my-4">
        {{ name }} {{ tel }} {{ email }} {{ date }}
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
