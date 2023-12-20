<script>
import Vault from "./components/Vault.vue";
import { getData } from "./data";

export default {
  components: { Vault },
  data() {
    return { data: getData() };
  },
};
</script>

<template>
  <Vault :data="data" />
</template>
