<template>
    
      <div class="numberPad">
        <div class="output">100</div>
        <div class="buttons">
          <button>1</button>
          <button>2</button>
          <button>3</button>
          <button>清除</button>
          <button>4</button>
          <button>5</button>
          <button>6</button>
          <button>清空</button>
          <button>7</button>
          <button>8</button>
          <button>9</button>
          <button class="ok">OK</button>
          <button class="zero"> 0</button>
          <button>.</button>
        </div>
      </div>
</template>

<script lang="ts">

    export default ({
        
    })
</script>
<style lang="scss" scoped>
@import "~@/assets/styles/colo.scss";
@import "~@/assets/styles/helper.scss";
.numberPad {
  font-size: 36px;
  font-family: Consolas, monospace;
  .output {
    padding: 12px;
    text-align: right;
    background: #ffffff;
    box-shadow: inset 0px -2px 3px rgba(0, 0, 0, 0.25),inset 0px 2px 3px rgba(0, 0, 0, 0.25);
  }
  .buttons {
    @extend %clearFix;
    button {
      width: 25%;
      height: 64px;
      border: none;
      background: transparent;
      float: left;
    }
    .ok{
      height: 64*2px;
      float: right;

    }
    .zero{
      width: 50%;
    }
    :nth-child(1) {
      background: $bg;
    }
    :nth-child(2),
    :nth-child(5) {
      background: darken($bg,4%);
    }
    :nth-child(3),
    :nth-child(6),:nth-child(9) {
      background: darken($bg,8%);
    }
    :nth-child(4),
    :nth-child(7),:nth-child(10) {
      background: darken($bg,12%);
    }
    :nth-child(8), :nth-child(11), :nth-child(13) {
          background: darken($bg, 4*4%);
        }
   :nth-child(14) {
          background: darken($bg, 4*5%);
        }
       :nth-child(12) {
          background: darken($bg, 4*6%);
        }
  }
  .buttons::after{
    content: '';
    clear: both;
    display: block;

  }
}
</style>