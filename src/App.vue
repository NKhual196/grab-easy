<template>
  <div class="wrapper">
    <!-- v-bind:style="{ width: widthSize + 'px', height: heightSize }" -->
    <router-view />
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      widthSize: 0,
      heightSize: 0,
    };
  },
  methods: {
    getScreenSize() {
      this.widthSize = window.innerWidth;
      this.heightSize = window.innerHeight;
      console.log(window.innerWidth);
    },
  },
};
</script>

<style>
* {
  font-family: "Roboto", sans-serif;
  font-size: 12px;
}
body {
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
}
input {
  border: none;
}
.wrapper {
  width: 100vw;
  height: 100vh;
  max-width: 420px;
}
</style>
