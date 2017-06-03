<template>
    <div class="container">
        <my-header></my-header>
        <hr>
          <div class="row">
            <server-list></server-list>
            <server-details></server-details>
          </div>
        <hr>
        <my-footer></my-footer>
    </div>
</template>

<script>
  import Header from './components/Shared/Header.vue';
  import ServerList from './components/Server/ServerList.vue'
  import ServerDetails from './components/Server/ServerDetails.vue';
  import Footer from './components/Shared/Footer.vue';
  export default {
    components: {
      'my-header': Header,
      'server-list': ServerList,
      'server-details': ServerDetails,
      'my-footer': Footer
    }
  }
</script>

<style>

</style>
