<template>
  <div class="btn-group btn-group-toggle" data-toggle="buttons">
    <label class="btn btn-secondary active seleccion">
      <input
        type="radio"
        name="options"
        id="option1"
        autocomplete="off"
        checked
      />
      All
    </label>
    <label class="btn btn-secondary seleccion">
      <input type="radio" name="options" id="option2" autocomplete="off" />
      Active
    </label>
    <label class="btn btn-secondary seleccion">
      <input type="radio" name="options" id="option3" autocomplete="off" />
      Complete
    </label>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$color-primario: #3a7bfd;
$Very-Light-Gray: hsl(0, 0%, 98%);
$Dark-Grayish-Blue: hsl(236, 9%, 61%);
$Very-Dark-Grayis-Blue: hsl(235, 19%, 35%);

.seleccion {
  padding: 0px 12px;
  background: none;
  font-weight: 700;
  border: none;
  color: $Dark-Grayish-Blue;
}
.btn-secondary:active,
.btn-secondary.active {
  color: $color-primario !important;
  background-color: transparent;
}
.btn-secondary:not(:disabled):not(.disabled).active{
  background-color: transparent;
}
.btn-secondary.not:active,
.btn-secondary.not.active {
  color: $color-primario !important;
  background-color: transparent;
}
.btn:focus,
.btn.focus {
  outline: none;
}
.btn-secondary:focus,
.btn-secondary.focus {
  box-shadow: none;
}
.textOption {
  color: $Dark-Grayish-Blue;
}
</style>