<template>
  <canvas  width="20" height="20" @click="clickpiece" v-drawCircle="color">canvas
  </canvas>
</template>

<script>
import Setting from "./Setting.js";
export default {
  name: "Piece",
  props: {
    color: {
      type: String,
      required: true
    }
  },
  methods: {
    clickpiece() {
      const vm = this;
      let color =
        this.color === Setting.defaultPieceColor
          ? "red"
          : Setting.defaultPieceColor;
      vm.$emit("change-color", color);
    }
  },
  data() {
    return {};
  },
  directives: {
    drawCircle: {
      inserted: function(el, binding) {
        const ctx = el.getContext("2d");
        ctx.fillStyle = binding.value;
        ctx.beginPath();
        ctx.arc(10, 10, 10, 0, 2 * Math.PI);
        ctx.fill();
      }
    }
  }
};
</script>
