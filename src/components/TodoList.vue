<template>
  <div :class="obtenerModo ? 'contenedor w-100' : 'contenedor-dark w-100'">
    <div v-for="item in lista" :key="item.id" class="lista">
      <div class="row">
        <div class="col-1">
          <div class="checkCircle mr-3">
            <div class="circle rounded-circle"></div>
          </div>
        </div>
        <div class="col-9 col-sm-10 pt-1 ml-md-0">
          <span class="textList ml-2" role="button"> {{ item.texto }} </span>
        </div>
        <div class="col-1">
          <img
            src="@/assets/icon-cross.svg"
            class="btnClose mt-1"
            role="button"
            alt="close"
          />
        </div>
      </div>
    </div>
    <div class="opciones">
      <div class="row">
        <div class="col text-left">
          <span class="textOption" role="button">5 items Left</span>
        </div>
        <div class="col text-center d-none d-md-flex">
          <menu-options />
        </div>
        <div class="col text-right">
          <span class="textOption" role="button">Clear Completes</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import menuOptions from "./utilities/menuOptions.vue";
export default {
  components: { menuOptions },
  data() {
    return {
      lista: [
        {
          texto: "Hola mundo",
          activo: true,
        },
        {
          texto: "Hola mundo",
          activo: true,
        },
      ],
    };
  },
  computed: {
    obtenerModo() {
      return this.$store.state.darkMode;
    },
  },
};
</script>

<style lang="scss" scoped>
$color-gradiente-1: #56ddff;
$color-gradiente-2: #bf58f3;
$color-purple: #9358f3;

$Very-Light-Gray: hsl(0, 0%, 98%);
$Dark-Grayish-Blue: hsl(236, 9%, 61%);
$Very-Dark-Grayis-Blue: hsl(235, 19%, 35%);

//Dark-theme
$Very-Dark-Blue: hsl(235, 21%, 11%);
$Very-Dark-Desaturated-Blue: hsl(235, 24%, 19%);
$Light-Grayish-Blue: hsl(234, 39%, 85%);
$Light-Grayish-Blue-hover: hsl(236, 33%, 92%);
$Dark-Grayish-Blue: hsl(234, 16%, 65%);
$Very-Dark-Grayish-Blue: hsl(233, 14%, 35%);
$Very-Dark-Grayish-Blue2: rgb(36, 39, 60);

.contenedor {
  background-color: $Very-Light-Gray;
  border-radius: 6px;
  box-shadow: 0px 46px 100px 9px rgba(148, 158, 160, 0.38);

  .opciones {
    padding: 18px 36px;
    .textOption {
      transition: 0.4s;
      color: $Dark-Grayish-Blue;
      &:hover {
        transition: 0.4s;
        color: $Very-Dark-Grayish-Blue;
      }
    }
  }

  .lista {
    padding: 24px 36px;
    border-bottom: 1px rgb(223, 223, 223) solid;
    @media screen and (max-width: 560px) {
      padding: 24px 24px;
    }
    .btnClose {
      transition: 0.2s;
      opacity: 0;
    }
    .checkCircle {
      .circle {
        transition: 0.2s;
        border-radius: 14px;
        height: 28px;
        width: 28px;
        border: 2px #dfdfdf solid;
      }
    }
    .textList {
      color: $Very-Dark-Grayis-Blue;
      font-size: 1.2em;
    }
    &:hover {
      .checkCircle {
        .circle {
          transition: 0.2s;
          border-radius: 14px;
          border: 2px solid $color-purple;
        }
      }
      .btnClose {
        transition: 0.2s;
        opacity: 1;
      }
    }
  }
}

.contenedor-dark {
  background-color: $Very-Dark-Grayish-Blue2;
  border-radius: 6px;
  box-shadow: 0px 46px 100px 9px rgba(0, 0, 0, 0.38);

  .opciones {
    padding: 18px 36px;
    .textOption {
      transition: 0.4s;
      color: $Dark-Grayish-Blue;
      &:hover {
        transition: 0.4s;
        color: $Light-Grayish-Blue-hover;
      }
    }
  }

  .lista {
    padding: 24px 36px;
    @media screen and (max-width: 560px) {
      padding: 24px 24px;
    }
    border-bottom: 1px #333333 solid;

    .btnClose {
      transition: 0.2s;
      opacity: 0;
    }
    .checkCircle {
      .circle {
        border-radius: 14px;
        height: 28px;
        width: 28px;
        border: 2px #333333 solid;
      }
    }
    .textList {
      color: $Light-Grayish-Blue;
      font-size: 1.2em;
    }
    &:hover {
      .checkCircle {
        .circle {
          transition: 0.2s;
          border-radius: 14px;
          border: 2px solid $color-gradiente-1;
        }
      }
      .btnClose {
        transition: 0.2s;
        opacity: 1;
      }
    }
  }
}
</style>