<template>
<div>
  <Piece @change-color="changeColor" :color="fillColor" />
  <span>{{fillColor}}</span>
<div></div>
  <div class="chess-wrap">
      <div class="checkerboard-h" v-for="(list,indexH) in checkerboardList" :key="indexH">
        <Lattice class="checkerboard-v" v-for="(item,indexV) in list" :key="indexV">
        </Lattice>
      </div>
  </div>

</div>
</template>

<script>
import Piece from "./Piece";
import Setting from "./Setting.js";
import Lattice from "./Lattice";

export default {
  name: "App",
  data() {
    return {
      fillColor: Setting.defaultPieceColor,
      checkerboardList: [
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ],
        [
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" },
          { color: "", key: "" }
        ]
      ]
    };
  },
  components: {
    Piece,
    Lattice
  },
  methods: {
    changeColor(color) {
      this.fillColor = color;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.chess-wrap {
  width: 560px;
  margin: 0 auto;
  background: #2c3e50;
}
.checkerboard-h {
  display: flex;
}
</style>
