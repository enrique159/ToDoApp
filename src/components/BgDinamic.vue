<template>
  <div :class="obtenerModo ? 'container-fluid bg-properties bg-dynamic' : 'container-fluid bg-properties bg-dynamic-dark'"></div>
</template>

<script>
export default {
  computed: {
    obtenerModo() {
      return this.$store.state.darkMode;
    },
  },
};
</script>

<style lang="scss" scoped>
$color-primario: #3a7bfd;

.bg-properties {
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

.bg-dynamic {
  background-image: url("~@/assets/bg-desktop-light.jpg");
  height: 44vh;
}

.bg-dynamic-dark {
  background-image: url("~@/assets/bg-desktop-dark.jpg");
  height: 44vh;
}
</style>