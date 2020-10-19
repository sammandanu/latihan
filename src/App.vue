<template>
  <div id="app">
    <Navbar nama="Adi Feri Ismail Udah Nikah" :kelas="subuh" />
    <router-view />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";

export default {
  components: {
    Navbar,
  },
  data: function() {
    return {
      subuh: "Dua rakaat",
    };
  },
};
</script>
<style></style>
