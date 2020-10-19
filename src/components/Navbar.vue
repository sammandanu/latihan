<template>
  <div class="w-full p-8 bg-blue-600 text-white">
    <div class="flex">
      <div class="flex-1">Logo</div>

      <ul class="flex w-1/4 justify-between">
        <li><router-link to="/">Home </router-link></li>
        <li>
          <router-link to="/about">
            <span
              :class="
                $router.currentRoute.name == 'About'
                  ? 'text-red-900'
                  : 'text-blue-800'
              "
            >
              About
            </span></router-link
          >
        </li>
        <li>Portofolio</li>
        <li>Contact</li>
      </ul>
    </div>
    <div class="">{{ nama }}</div>
    <div class="">{{ kelas }}</div>
  </div>
</template>

<script>
export default {
  name: "NavbarComponent",
  props: {
    nama: null,
    kelas: null,
  },
  mounted() {
    // console.log("ini router", this.);
  },
};
</script>

<style></style>
