<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<template>
  <div class="q-pa-md">
    <div class="row">
      <div class="col col-md-8">.col .col-md-8</div>
      <div class="col-6 col-md-4">.col-6 .col-md-4</div>
    </div>
    <div class="row">
      <div class="col-6 col-md-4">.col-6 .col-md-4</div>
      <div class="col-6 col-md-4">.col-6 .col-md-4</div>
      <div class="col-6 col-md-4">.col-6 .col-md-4</div>
    </div>
    <div class="row">
      <div class="col-6">.col-6</div>
      <div class="col-6">.col-6</div>
    </div>
  </div>
</template>

<style lang="sass">
.row > div
    padding: 10px 15px
    background: rgb(86, 61, 124)
    border: 1px solid rgb(86, 61, 124)

.row + .row
    margin-top: 1rem
</style>
