<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<template>
  <div class="q-pa-md">
    <div class="row justify-center">
      <div class="col-12 col-md-2">.col-12 .col-md-2</div>
      <div class="col-12 col-md-auto">
        .col-12 .col-md-auto (Variable width content)
      </div>
      <div class="col-12 col-md-2">.col-12 .col-md-2</div>
    </div>
    <div class="row">
      <div class="col">.col</div>
      <div class="col-12 col-md-auto">
        .col-12 .col-md-auto (Variable width content)
      </div>
      <div class="col">.col</div>
    </div>
  </div>
</template>

<style lang="sass" scoped>
.row
    background: rgb(255,0,0)

.row > div
    padding: 10px 15px
    background: rgb(90, 12, 3)
    border: 1px solid rgb(86, 61, 124)

.row + .row
    margin-top: 1rem

</style>
