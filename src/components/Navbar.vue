<template>
  <dir class="color nav-bar"></dir>
</template>

<script>
export default {
  name: "Navbar",
  props: {
    msg: String
  },
  methods: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
  color: #d4e9df;
}
.color {
  margin: 0;
  padding: 0;
  height: 60px;
  background: rgb(55, 158, 117);
  background: linear-gradient(
    27deg,
    rgba(55, 158, 117, 1) 0%,
    rgba(151, 222, 188, 1) 37%,
    rgba(106, 237, 112, 0.9836309523809523) 100%
  );
}
</style>
