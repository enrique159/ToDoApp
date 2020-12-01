<template>
  <div class="contenedor w-100">
    <div class="row justify-content-center">
      <div class="col opciones align-self-center">
        <menu-options/>
      </div>
    </div>
  </div>
</template>

<script>
import menuOptions from './menuOptions.vue';
export default {
  components: { menuOptions },};
</script>

<style lang="scss" scoped>
$Very-Light-Gray: hsl(0, 0%, 98%);
$Dark-Grayish-Blue: hsl(236, 9%, 61%);
$Very-Dark-Grayis-Blue: hsl(235, 19%, 35%);

.contenedor {
  background-color: $Very-Light-Gray;
  box-shadow: 0px 80px 100px 9px rgba(178, 189, 189, 0.38);
  padding: 18px 36px;
  border-radius: 6px;

  .opciones{
    text-align: center;
  }
}
</style>