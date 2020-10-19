<template>
  <div class="home">
    <h1 class="text-4xl bg-red-900">Coba an dari adiferi</h1>
    <div class="flex" v-for="(kuli, index) in kuliah" :key="index">
      <div class="">{{ index + 1 }}</div>
      <div class="flex">
        <div class="">Kulian Makul :</div>
        <div class="">{{ kuli.makul }}</div>
      </div>
    </div>
    <div class="">
      {{ namalain }}
    </div>
    <button @click="aksi()">Aksi</button>
  </div>
</template>

<script>
// @ is an alias to /src
// import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    // HelloWorld
  },
  data: function() {
    return {
      nama: "M  Almadanu",
      kelas: 10,
      umur: 23,
      kuliah: [
        {
          makul: "ipa",
          dosen: "Pak Damar",
        },
        {
          makul: "ips",
          dosen: "Bu yuli",
        },
      ],
    };
  },
  computed: {
    namalain: function() {
      return this.nama + " lain";
    },
  },
  created() {},
  mounted() {
    console.log("data kuliah", this.kuliah);
  },
  methods: {
    aksi() {
      this.kuliah.forEach((kul) => {
        console.log(kul.makul);
      });
    },
  },
};
</script>

<style></style>
