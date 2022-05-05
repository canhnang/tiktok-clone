<template>
  <div id="wrapper">
    <div>
      <TopBar></TopBar>
    </div>
    <b-container>
      <b-row>
        <b-col md="4"><SideBar /></b-col>
        <b-col md="8" class="nuxt"><nuxt /></b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import TopBar from "../components/Layouts/TopBar.vue";
import SideBar from "../components/Layouts/SideBar.vue";

export default {
  name: "default",
  components: { TopBar, SideBar },
};
</script>
<style>
.nuxt {
  margin-top: 60px;
}
</style>

