<template>
   <canvas @mouseover="muover" @mouseout="muout" :class="mouseenter?'canvas-hover':''" width="40" height="40" v-drawLine>棋盘方格</canvas>
</template>
<script>
export default {
  name: "Lattice",
  data() {
    return {
      mouseenter: false
    };
  },
  methods: {
    muover() {
      this.mouseenter = true;
    },
    muout() {
      this.mouseenter = false;
    }
  },
  directives: {
    drawLine: {
      inserted: function(el) {
        const ctx = el.getContext("2d");
        ctx.lineWidth = 1;
        ctx.strokeStyle = "#999";
        ctx.beginPath();
        ctx.moveTo(0, 20);
        ctx.lineTo(40, 20);
        ctx.moveTo(20, 0);
        ctx.lineTo(20, 40);
        ctx.stroke();
      }
    }
  }
};
</script>
<style scoped>
.canvas-hover {
  background: rgb(250, 255, 177);
}
</style>
