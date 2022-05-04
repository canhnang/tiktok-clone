<template>
  <div id="wrapper">
    <div id="content-wrapper" class="d-flex flex-column">
      <div id="content">
        <NavBar></NavBar>
        <nuxt />
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from "../components/Layouts/TopBar.vue";

export default {
  name: "default",
  components: { NavBar },
};
</script>

