<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <!-- <div :style="{ color: $store.state.colorCode }" class="counter">
      {{ counter }}
      {{ $store.state.counter }}
    </div> -->

    <counter />

    <!-- <div class="counter-squared">
      {{ $store.state.counter }}
      <sup>2</sup> = {{ $store.getters.counterSquared }}
    </div> -->

    <countersquared />
    <!-- <div class="buttons">
      <button @click="$store.dispatch('decreaseCounter')">
        -
      </button>
      <button @click="$store.dispatch('increaseCounter')">
        +
      </button>
    </div> -->

    <buttons />
    <!-- <div>
      <input v-model="colorCode" placeholder="Enter Color Code" type="text" />
    </div> -->

    <colorcode />
  </div>
</template>

<script>
export default {
  name: "Home",
  // computed: {
  //   colorCode: {
  //     get() {
  //       return this.$store.state.colorCode;
  //     },
  //     set(newValue) {
  //       this.$store.dispatch("setColorCode", newValue);
  //     },
  //   },
  // },

  components: {
    counter: require("@/components/Counter.vue").default,
    countersquared: require("@/components/CounterSquared.vue").default,
    buttons: require("@/components/Buttons.vue").default,
    colorcode: require("@/components/ColorCode.vue").default,
  },

  // data() {
  //   return {
  //     counter: 0,
  //   };
  // },

  // methods: {
  //   increaseCounter() {
  //     this.counter++;
  //   },

  //   decreaseCounter() {
  //     this.counter--;
  //   },
  // },
};
</script>

<style>
div {
  margin-bottom: 10px;
}

.counter {
  font-size: 80px;
}

.buttons button {
  font-size: 40px;
  width: 100px;
  margin: 0 10px;
}
</style>
