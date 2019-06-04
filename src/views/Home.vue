<template>
  <div id="Home" class="container-fluid">
    <h1>Registro de Cliente</h1>
    
      <client-form></client-form>
  </div>
</template>

<script>
import ClientForm from "../components/ClientForm.vue";

export default {
  name: "Home",
  components: { ClientForm }
};
</script>

<style lang="scss" scoped>
    h1 {
        margin: 5px;
    }


</style>