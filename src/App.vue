<script lang="ts">
import { defineComponent } from "vue";
import QNavigationDrawer from "./components/navigationDrawer/QNavigationDrawer.vue";
import BasicNavigationDrawer from "./components/navigationDrawer/BasicNavigationDrawer.vue";
import HeaderPictureNavigationDrawer from "./components/navigationDrawer/HeaderPictureNavigationDrawer.vue";
import EqualWidth from "./components/gridRow/EqualWidth.vue";
import ColumnWidth from '@/components/gridRow/ColumnWidth.vue';
import VariableWidthContent from '@/components/gridRow/VariableWidthContent.vue';
import AllBreakPoints from '@/components/gridRow/ResponsiveClasses/AllBreakPoints.vue';
import StackedToHorizontal from '@/components/gridRow/ResponsiveClasses/StackedToHorizontal.vue';
import MixAndMatch from '@/components/gridRow/ResponsiveClasses/MixAndMatch.vue';
import Vertical from '@/components/gridRow/ResponsiveClasses/Alignment/Vertical.vue';
export default defineComponent({
  components: {
    QNavigationDrawer,
    BasicNavigationDrawer,
    HeaderPictureNavigationDrawer,
    EqualWidth,
    ColumnWidth,
    VariableWidthContent,
    AllBreakPoints,
    StackedToHorizontal,
    MixAndMatch,
    Vertical
  },
});
</script>

<template>
  <div>
    <h3>Vue 3 + TypeScript + Quasar App</h3>
    <section id="navigation-drawer">
      <!--  -->
      <QNavigationDrawer />
      <br />
      <BasicNavigationDrawer />
      <br />
      <HeaderPictureNavigationDrawer />
    </section>
    <section id="grid-row">
      <EqualWidth/>
      <br/>
      <ColumnWidth/>
      <br/>
      <VariableWidthContent/>
      <br/>
      <AllBreakPoints/>
      <br/>
      <StackedToHorizontal/>
      <br/>
      <MixAndMatch/>
      <br/>
      <Vertical/>
    </section>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
