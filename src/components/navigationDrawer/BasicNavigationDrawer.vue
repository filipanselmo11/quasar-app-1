<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    const drawerLeft = ref(false);
    const drawerRight = ref(false);

    return { drawerLeft, drawerRight };
  },
});
</script>

<template>
  <div class="q-pa-md">
    <q-layout
      view="hHh Lpr lff"
      container
      style="height: 300px"
      class="shadow-2 rounded-borders"
    >
      <q-header elevated class="bg-black">
        <q-toolbar>
          <q-btn
            flat
            @click="drawerLeft = !drawerLeft"
            rounded
            dense
            icon="menu"
          />
          <q-toolbar>Header</q-toolbar>
          <q-btn
            flat
            @click="drawerRight = !drawerRight"
            round
            dense
            icon="menu"
          />
        </q-toolbar>
      </q-header>
      <q-drawer
        v-model="drawerLeft"
        show-if-above
        :width="200"
        :breakpoint="700"
        elevated
        class="bg-primary text-white"
      >
        <q-scroll-area class="fit">
          <div class="q-pa-sm">
            <div v-for="n in 10" :key="n">Drawer {{ n }}</div>
          </div>
        </q-scroll-area>
      </q-drawer>
      <q-drawer
        side="right"
        v-model="drawerRight"
        show-if-above
        bordered
        :width="200"
        :breakpoint="500"
        class="bg-grey-3"
      >
        <q-scroll-area class="fit">
          <div class="q-pa-sm">
            <div v-for="n in 20" :key="n">Drawer {{ n }}</div>
          </div>
        </q-scroll-area>
      </q-drawer>
      <q-page-container>
        <q-page padding>
          <p v-for="n in 15" :key="n">Lorem ipsum....</p>
        </q-page>
      </q-page-container>
    </q-layout>
  </div>
</template>

<style scoped></style>
