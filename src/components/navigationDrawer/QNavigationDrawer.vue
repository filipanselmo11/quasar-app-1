<script lang="ts">
import { defineComponent, ref } from "vue";

const menuList = [
  {
    icon: "inbox",
    label: "Inbox",
    separator: true,
  },
  {
    icon: "send",
    label: "Outbox",
    separator: false,
  },
];

export default defineComponent({
  name: 'QNavigationDrawer',
  setup() {
    const drawer = ref(false);
    return { drawer, menuList };
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
          <q-btn flat @click="drawer = !drawer" round dense icon="menu">
            <q-toolbar-title> Header </q-toolbar-title>
          </q-btn>
        </q-toolbar>
      </q-header>

      <q-drawer
        v-model="drawer"
        show-if-above
        :width="200"
        :breakpoint="500"
        bordered
        class="bg grey-3"
      >
        <q-scroll-area class="fit">
          <q-list>
            <template v-for="(item, index) in menuList" :key="index">
              <q-item clickable :active="item.label === 'Outbox'" v-ripple>
                <q-item-section avatar>
                  <q-icon :name="item.icon" />
                </q-item-section>
                <q-item-section>
                  {{ item.label }}
                </q-item-section>
              </q-item>
              <q-separator :key="'sep' + index" v-if="item.separator" />
            </template>
          </q-list>
        </q-scroll-area>
      </q-drawer>

      <q-page-container>
        <q-page padding>
            <p v-for="n in 15" :key="n">
                Lorem ipsum dolor ......
            </p>
        </q-page>
      </q-page-container>
    </q-layout>
  </div>
</template>

<style scoped></style>
