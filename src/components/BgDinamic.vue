<template>
  <div id="bg-dynamic" class="container-fluid bg-properties"></div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$color-primario: #3a7bfd;

.bg-properties {
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

#bg-dynamic {
  background-image: url("~@/assets/bg-desktop-light.jpg");
  height: 44vh;
}
</style>