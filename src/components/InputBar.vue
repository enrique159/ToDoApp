<template>
  <div class="contenedor w-100">
    <div class="row">
      <div class="col-1">
        <div class="checkCircle mr-3">
          <div class="circle"></div>
        </div>
      </div>
      <div class="col-11">
        <input type="text" id="inputTODO" placeholder="Create a new todo.." class="w-100" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$Very-Light-Gray: hsl(0, 0%, 98%);
$Dark-Grayish-Blue: hsl(236, 9%, 61%);
$Very-Dark-Grayis-Blue: hsl(235, 19%, 35%);

.contenedor {
  background-color: $Very-Light-Gray;
  padding: 24px 36px;
  border-radius: 6px;
  .checkCircle {
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
</style>