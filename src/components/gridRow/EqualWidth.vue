<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  //   setup() {},
});
</script>

<template>
  <div class="q-pa-md">
    <div class="row">
      <div class="col">.col</div>
      <div class="col">.col</div>
    </div>
    <div class="row">
      <div class="col">.col</div>
      <div class="col">.col</div>
      <div class="col">.col</div>
    </div>
  </div>
</template>

<style lang="sass" scoped>
.row > div
    padding: 10px 15px
    background: rgba(86, 61, 124,.15)
    border: 1px solid rgba(86, 61, 124,.2)

.row + .row
    margin-top: 1rem
</style>
