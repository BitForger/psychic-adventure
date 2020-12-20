<template>
  <code>
    {{this.result}}
  </code>
</template>

<script lang="ts">
import Vue from 'vue'
import { Component, Prop } from 'vue-property-decorator';

@Component({
  name: 'Chat',
  async mounted () {
  },
  computed: {
  },
  data: {
  }
})
export default class Chat extends Vue {
  private result: any;

  constructor () {
    super();
    this.axios.get('http://localhost:3000/keys/keypair').then(value => {
      this.result = JSON.stringify(value.data, null, 4);
    })
  }
}
</script>

<style scoped>

</style>
