<template>
  <div>
    <div class="container">
      <div class="bar">
        <div class="bold"><h3>Bold</h3></div>
        <div class="circle top"></div>
        <div class="circle middle"></div>
        <div class="circle bottom"></div>
        <div class="creamy"><h3>Creamy</h3></div>
      </div>
      <div class="coffee-cups">
        <div class="cup-small doppio">
          <div class="handle"></div>
        </div>
        <div class="cup americano">
          <div class="handle"></div>
        </div>
        <div class="cup-small macchiato">
          <div class="handle"></div>
        </div>
        <div class="cup-small flatwhite">
          <div class="handle"></div>
        </div>
        <div class="cup cappuccino">
          <div class="handle"></div>
        </div>
        <div class="cup-long latte">
          <div class="handle"></div>
          <div class="bottom-handle"></div>
        </div>
      </div>
      <div class="info">
        <div class="first">
          <h1>doppio</h1>
          <p>Double shot of espresso. Straight.</p>
        </div>
        <div class="second">
          <h1>americano</h1>
          <p>Shots of espresso diluted with water</p>
        </div>
        <div class="third">
          <h1>Macchiato</h1>
          <p>Espresso with a dash of frothy foamed milk.</p>
        </div>
        <div class="fourth">
          <h1>Flat White</h1>
          <p>Double shot of espresso with steamed milk.</p>
        </div>
        <div class="fifth">
          <h1>Cappuccino</h1>
          <p>Double shot of espresso topped with an airy thick layer of foamed milk.</p>
        </div>
        <div class="sixth">
          <h1>Caffe Latte</h1>
          <p>A shot of espresso in steamed milk lightly topped with foam.</p>
        </div>
        
      </div>
    </div>

    <div class="key">
      <div class="circle espresso"><p class="small">espresso</p></div>
      <div class="circle milk"><p class="small">steamed milk</p></div>
      <div class="circle foam"><p class="small">milk foam</p></div>
      <div class="circle water"><p class="small">water</p></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Coffee',
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
$dark: #252c32;
$brown: #5b4644;
$coffee: #87624f;
$tan: #dab7a3;
$white: #f4e8da;
$water: #859fb5;

$sans: 'IBM Plex Sans', sans-serif;
$serif: 'Lora', serif;

html {
  display: flex;
  justify-content: center;
  min-height: 100vh;
}

body {
  margin: 0;
  font-family: 'IBM Plex Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background: $dark;
  display: grid;
  font-family: $sans;
  text-transform: uppercase;
}

h3 {
  font-size: 0.8em;
  letter-spacing: 1px;
  font-weight: 100;
}

.container {
  position: relative;
  margin: auto;
  overflow: hidden;
  width: 500px;
  height: 95vh;
}

.bar {
  position: absolute;
  height: 85%;
  width: 2px;
  left: 7%;
  top: 7.5%;
  background: $white;
}

.circle {
  width: 10px;
  height: 10px;
  position: absolute;
  border-radius: 50%;
  left: -5px;
  border: 1px solid $white;
  box-shadow: 0px 0px 7px rgba($white, 100%);
}

.top {
  background: $brown;
  top: -1%;
}
.middle {
  background: $coffee;
  top: 38%;
}
.bottom {
  background: $tan;
  bottom: -1%;
}

.bold {
  color: $coffee;
  position: absolute;
  top: -7%;
  left: -17px;
}

.creamy {
  color: $tan;
  position: absolute;
  bottom: -7%;
  left: -27px;
}

.info {
  width: 55%;
  height: 100%;
  position: absolute;
  left: 43%;
}

//coffee cup drawings

.coffee-cups {
  width: 40%;
  height: 100%;
  position: absolute;
  left: 10%;
  top: 3%;
}

.handle {
  position: absolute;
  height: 20px;
  width: 15px;
  background: transparent;
  border-radius: 50% 30%;
  left: 95%;
  top: 10%;
  z-index: -1;
  border: 2px solid $white;
}

.cup {
  position: absolute;
  width: 70px;
  height: 55px;
  background: $dark;
  border: 2px solid $white;
  border-radius: 0 0 5rem 5rem;
  left: 20%;
}

.cup-small {
  position: absolute;
  width: 55px;
  height: 40px;
  background: $dark;
  border: 2px solid $white;
  border-radius: 0 0 5rem 5rem;
  left: 23%;
}

.cup-long {
  position: absolute;
  width: 60px;
  height: 70px;
  background: $dark;
  border: 2px solid $white;
  border-radius: 10% 10% 50% 50%;
  left: 22%;
}

.doppio {
  top: 5%;
  background: linear-gradient(to bottom, $dark 40%, $brown 40%, $coffee 70%);
}

.americano {
  top: 18.5%;
  background: linear-gradient(
    to bottom,
    $dark 13%,
    $water 13%,
    $water 50%,
    $coffee 50%
  );
}

.macchiato {
  top: 35%;
  background: linear-gradient(
    to bottom,
    $dark 20%,
    $white 20%,
    $white 40%,
    $coffee 40%
  );
}

.flatwhite {
  top: 50%;
  background: linear-gradient(
    to bottom,
    $dark 10%,
    $white 10%,
    $tan 60%,
    $coffee 65%,
    $brown 90%
  );
}

.cappuccino {
  top: 64%;
  background: linear-gradient(
    to bottom,
    $white 50%,
    $tan 50%,
    $tan 55%,
    $coffee 60%
  );
}

.latte {
  top: 81%;
  background: linear-gradient(
    to bottom,
    $dark 5%,
    $white 5%,
    $white 30%,
    $tan 30%,
    $tan 70%,
    $coffee 70%
  );
}

//description
h1 {
  color: $white;
  font-size: 1em;
  letter-spacing: 3px;
}

p {
  color: $white;
  font-family: $serif;
  text-transform: none;
  font-size: 0.7em;
  letter-spacing: 0.5px;
  margin-top: -5px;
}

.first,
.second,
.third,
.fourth,
.fifth,
.sixth {
  position: absolute;
}

.first {
  top: 7%;
}

.second {
  top: 21%;
}

.third {
  top: 36%;
}

.fourth {
  top: 52%;
}

.fifth {
  top: 65%;
}

.sixth {
  top: 83%;
}

// key for the colors
.small {
  margin-left: 20px;
  margin-top: -1px;
  font-family: $sans;
  text-transform: uppercase;
  letter-spacing: 2px;
}

.key {
  position: relative;
  margin: auto;
  width: 500px;
  height: 5vh;
}

.espresso {
  background: $brown;
  position: absolute;
  left: 17%;
}

.milk {
  background: $tan;
  position: absolute;
  left: 40%;
}

.foam {
  background: $white;
  position: absolute;
  left: 63%;
}

.water {
  background: $water;
  position: absolute;
  left: 83%;
}
</style>
