<template>
  <div class="col-xs-12 col-sm-6">
      <p v-if="!server">Server Details are currently not updated</p>
      <p v-else>Status for Server #{{ server.id }} - {{ server.status }}</p>
      <hr>
      <button @click="resetStatus">Reset server status to Normal</button>
  </div>
</template>

<script>
import { eventBus } from './../../main';
export default {
  data() {
    return {
      server: null
    }
  },
  methods: {
    resetStatus() {
      this.server.status = 'Normal';
    }
  },
  created() {
    eventBus.$on('serverSelected', (server) => {
      this.server = server;
    });
  }
}
</script>

<style lang="css">
</style>
