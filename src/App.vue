<template>
  <div>
    <bg-dinamic />
    <todo-app />
  </div>
</template>

<script>
import BgDinamic from "./components/BgDinamic.vue";
import TodoApp from "./components/TodoApp.vue";
export default {
  name: "App",
  components: {
    TodoApp,
    BgDinamic,
  },
};
</script>

<style lang="scss">
:root{
  $color-primario: #3a7bfd;
  $color-gradiente-1: #56ddff;
  $color-gradiente-2: #bf58f3;

  //light-theme
  $Very-Light-Gray: hsl(0, 0%, 98%);
  $Very-Light-Grayis-Blue: hsl(236, 33%, 92%);
  $Light-Grayish-Blue: hsl(233, 11%, 84%);
  $Dark-Grayish-Blue: hsl(236, 9%, 61%);
  $Very-Dark-Grayis-Blue: hsl(235, 19%, 35%);

  //Dark-theme
  $Very-Dark-Blue: hsl(235, 21%, 11%);
  $Very-Dark-Desaturated-Blue: hsl(235, 24%, 19%);
  $Light-Grayish-Blue: hsl(234, 39%, 85%);
  $Light-Grayish-Blue-hover: hsl(236, 33%, 92%);
  $Dark-Grayish-Blue: hsl(234, 11%, 52%);
  $Very-Dark-Grayish-Blue: hsl(233, 14%, 35%);
  $Very-Dark-Grayish-Blue2: hsl(237, 14%, 26%);
}

#app {
  font-family: "Josefin Sans", sans-serif;
}
</style>
