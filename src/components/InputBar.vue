<template>
  <div :class="obtenerModo ? 'contenedor w-100' : 'contenedor-dark w-100'">
    <div class="row">
      <div class="col-1">
        <div class="checkCircle mr-3">
          <div class="circle"></div>
        </div>
      </div>
      <div class="col-10 col-sm-11">
        <input
          type="text"
          id="inputTODO"
          placeholder="Create a new todo.."
          class="pl-2 ml-md-0 pt-1 w-100"
        />
      </div>
    </div>
  </div>
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
$Very-Light-Gray: hsl(0, 0%, 98%);
$Dark-Grayish-Blue: hsl(236, 9%, 61%);
$Very-Dark-Grayis-Blue: hsl(235, 19%, 35%);

//Dark-theme
$Very-Dark-Blue: hsl(235, 21%, 11%);
$Very-Dark-Desaturated-Blue: hsl(235, 24%, 19%);
$Light-Grayish-Blue: hsl(234, 39%, 85%);
$Light-Grayish-Blue-hover: hsl(236, 33%, 92%);
$Dark-Grayish-Blue: hsl(234, 11%, 52%);
$Very-Dark-Grayish-Blue: hsl(233, 14%, 35%);
$Very-Dark-Grayish-Blue2: rgb(36, 39, 60);

.contenedor {
  background-color: $Very-Light-Gray;
  box-shadow: 0px 46px 100px 9px rgba(136, 136, 136, 0.38);
  @media screen and (max-width: 560px) {
    padding: 24px 24px;
  }
  padding: 24px 36px;
  border-radius: 6px;
  .checkCircle {
    padding-top: 1px;
    .circle {
      border-radius: 14px;
      height: 28px;
      width: 28px;
      border: 2px #dfdfdf solid;
    }
  }
  #inputTODO {
    color: $Very-Dark-Grayis-Blue;
    background: none;
    font-size: 1.2em;
    border: none;
    outline: none;
    &::placeholder {
      color: $Dark-Grayish-Blue;
    }
  }
}

.contenedor-dark {
  background-color: $Very-Dark-Grayish-Blue2;
  @media screen and (max-width: 560px) {
    padding: 24px 24px;
  }
  padding: 24px 36px;
  border-radius: 6px;
  .checkCircle {
    .circle {
      border-radius: 14px;
      height: 28px;
      width: 28px;
      border: 2px #333333 solid;
    }
  }
  #inputTODO {
    color: $Light-Grayish-Blue;
    background: none;
    font-size: 1.2em;
    border: none;
    outline: none;
    &::placeholder {
      color: $Very-Dark-Grayish-Blue;
    }
  }
}
</style>