<template>
  <div id="app">
    <div class="parallax">
    <div class="parallax__layer parallax__layer__0">
        <img src="https://sam.beckham.io/images/articles/firewatch/layer_0.png" />
    </div>
    <div class="parallax__layer parallax__layer__1">
        <img src="https://sam.beckham.io/images/articles/firewatch/layer_1.png" />
    </div>
    <div class="parallax__layer parallax__layer__2">
        <img src="https://sam.beckham.io/images/articles/firewatch/layer_2.png" />
    </div>
    <div class="parallax__layer parallax__layer__3">
        <img src="https://sam.beckham.io/images/articles/firewatch/layer_3.png" />
    </div>
    <div class="parallax__layer parallax__layer__4">
        <img src="https://sam.beckham.io/images/articles/firewatch/layer_4.png" />
    </div>
    <div class="parallax__layer parallax__layer__5">
        <img src="https://sam.beckham.io/images/articles/firewatch/layer_5.png" />
    </div>
    <div class="parallax__layer parallax__layer__6">
        <img src="https://sam.beckham.io/images/articles/firewatch/layer_6.png" />
    </div>
    <div class="parallax__cover"></div>
</div>
    
  </div>
</template>

<style lang="scss">


*{
  box-sizing: border-box;
}

html,
body{
  background-color: #FEDCC8;
}

.parallax {
  perspective: 100px;
  height: 100vh;
  overflow-x: hidden;
  overflow-y: auto;
  position: absolute;
  top: 0;
  left: 50%;
  right: 0;
  bottom: 0;
  margin-left: -1500px;
}

.parallax__layer{
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  
  img{
    display: block;
    position: absolute;
    bottom: 0;
  }
}

.parallax__cover{
  background: #2D112B;
  display: block;
  position: absolute;
  top: 100%;
  left: 0;
  right: 0;
  height: 2000px;
  z-index: 2;
}

$parallax__layers: 6;

@for $i from 0 through $parallax__layers {
  $x: ($parallax__layers - $i) / 2;
  .parallax__layer__#{$i}{
     transform: translateZ(-100 * $x#{px}) scale($x + 1);
  }
}

</style>
