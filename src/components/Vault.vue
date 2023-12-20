<script>
import { Vault } from "@dhx/trial-vault";
import "@dhx/trial-vault/codebase/vault.min.css";

export default {
  props: ["data"],
  data() {
    return {
      vault: null,
    };
  },

  mounted() {
    this.vault = new Vault(this.$refs.cont, {});
    this.vault.data.parse(this.data);
  },
  unmounted() {
    this.vault.destructor();
    this.$refs.cont.innerHTML = "";
  },
};
</script>

<template>
  <div ref="cont" style="width: 440px; height: 400px; margin: 50px auto"></div>
</template>
