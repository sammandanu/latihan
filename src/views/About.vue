<template>
  <div class="">
    <h1 class="text-xl text-red font-semibold" v-if="nyala">Ini About</h1>
    <h1 class="text-xl text-red font-semibold" v-else>Ini Mati</h1>

    <div class="">
      <input class="border border-gray-900" type="text" v-model="nama" />
    </div>
    <div class="" v-if="nama">{{ nama }}</div>
    <div class="" v-else>Nama Belum Diisi</div>
    <Navbar />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
export default {
  name: "About",
  components: {
    Navbar,
  },
  data: function() {
    return {
      nyala: false,
      nama: null,
    };
  },
  mounted() {
    // this.nyala = true;
  },
};
</script>

<style></style>
