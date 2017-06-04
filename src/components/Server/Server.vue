<template>
  <div>
    <li
      class="list-group-item"
      style="cursor: pointer"
      @click="showServerDetail">
      Server #{{ server.id }} - Status: {{ server.status }}
    </li>
  </div>
</template>

<script>
import { eventBus } from './../../main';
export default {
  props: {
    server: {
      type: Object,
      required: true
    }
  },
  methods: {
    showServerDetail() {
      eventBus.$emit('serverSelected', this.server);
    }
  }
}
</script>

<style lang="css">
</style>
