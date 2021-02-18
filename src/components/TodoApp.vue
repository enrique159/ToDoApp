<template>
  <div id="contenedor" class="container-fluid w-100">
    <div id="contenedormini" class="container-lg">
      <div class="row justify-content-between">
        <h1 class="logotipo pt-1">TODO</h1>
        <button
          id="btnTheme"
          type="button"
          class="btn btn-light"
          @click="cambiarModoOscuro"
        >
          <img src="@/assets/icon-moon.svg" alt="" v-if="obtenerModo" />
          <img src="@/assets/icon-sun.svg" alt="" v-else />
        </button>
      </div>
      <div class="row pt-4">
        <input-bar />
      </div>
      <div class="row pt-4">
        <todo-list />
      </div>
      <div class="row pt-4 d-flex d-md-none">
        <MenuXSOptions />
      </div>
    </div>
  </div>
</template>

<script>
import InputBar from "./InputBar.vue";
import TodoList from "./TodoList.vue";
import MenuXSOptions from "./utilities/menuXSOptions.vue";

export default {
  data() {
    return {
      modoOscuro: this.$store.state.darkMode,
    };
  },
  methods: {
    cambiarModoOscuro() {
      this.$store.state.darkMode = !this.$store.state.darkMode;
      console.log(this.$store.state.darkMode);
    },
  },
  computed: {
    obtenerModo() {
      return this.$store.state.darkMode;
    },
  },
  components: {
    InputBar,
    TodoList,
    MenuXSOptions,
  },
};
</script>

<style lang="scss" scoped>
$Very-Light-Gray: hsl(0, 0%, 98%);

#contenedor {
  position: absolute;
  top: 68px;

  #contenedormini {
    padding: 0em 14em;
    @media screen and (max-width: 960px) {
      padding: 0em 4em;
    }
    @media screen and (max-width: 560px) {
      padding: 0em 1.5em;
    }

    #btnTheme {
      background-color: transparent;
      border-radius: 36px;
      height: fit-content;
      cursor: pointer;
      overflow: hidden;
      transition: 0.3s;
      padding: 12px;
      border: none;
      &:hover {
        background-color: rgba($color: #fff, $alpha: 0.2);
      }
      &:focus {
        border-style: none;
        outline: none;
      }
      img {
        height: 32px;
      }
      .fade-enter-active,
      .fade-leave-active {
        transition: opacity 0.5s;
      }
      @media screen and (max-width: 560px) {
        padding: 8px;
        img {
          height: 26px !important;
        }
      }
    }
    .logotipo {
      color: $Very-Light-Gray;
      font-size: 3em;
      font-weight: 700;
      letter-spacing: 0.8ch;
      @media screen and (max-width: 560px) {
        font-size: 2.2em
      }
    }
  }
}
</style>