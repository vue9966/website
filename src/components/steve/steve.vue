<template>
  <div class="grid">
    <figure class="effect-steve">
      <img src="../../assets/img/33.jpg" alt="img33" />

      <figcaption>
        <h2>生活</h2>
        <!-- <p>生活本就是柴米油盐酱醋茶,平平淡淡</p> -->
        <p>生活是柴米油盐的平淡；是行色匆匆早出晚归的奔波</p>
      </figcaption>
    </figure>
  </div>
</template>

<script>
export default {};
</script>

<style>
@import url("../../assets/css/components.css");
.grid figure figcaption, .grid figure figcaption > a{
    width: auto;
    margin: 0 auto;
}
figure.effect-steve {
  z-index: auto;
  overflow: visible;
  background: #000;
}

figure.effect-steve:before,
figure.effect-steve h2:before {
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  width: 100%;
  height: 100%;
  background: #000;
  content: "";
  -webkit-transition: opacity 0.35s;
  transition: opacity 0.35s;
}

figure.effect-steve:before {
  box-shadow: 0 3px 30px rgba(0, 0, 0, 0.8);
  opacity: 0;
}

figure.effect-steve figcaption {
  z-index: 1;
}

figure.effect-steve img {
  opacity: 1;
  -webkit-transition: -webkit-transform 0.35s;
  transition: transform 0.35s;
  -webkit-transform: perspective(1000px) translate3d(0, 0, 0);
  transform: perspective(1000px) translate3d(0, 0, 0);
}

figure.effect-steve h2,
figure.effect-steve p {
  background: #fff;
  color: #2d434e;
}

figure.effect-steve h2 {
  position: relative;
  margin-top: 2em;
  padding: 0.25em;
}

figure.effect-steve h2:before {
  box-shadow: 0 1px 10px rgba(0, 0, 0, 0.5);
}

figure.effect-steve p {
  margin-top: 1em;
  padding: 0.5em;
  font-weight: 800;
  opacity: 0;
  -webkit-transition: opacity 0.35s, -webkit-transform 0.35s;
  transition: opacity 0.35s, transform 0.35s;
  -webkit-transform: scale3d(0.9, 0.9, 1);
  transform: scale3d(0.9, 0.9, 1);
}

figure.effect-steve:hover:before {
  opacity: 1;
}

figure.effect-steve:hover img {
  -webkit-transform: perspective(1000px) translate3d(0, 0, 21px);
  transform: perspective(1000px) translate3d(0, 0, 21px);
}

figure.effect-steve:hover h2:before {
  opacity: 0;
}

figure.effect-steve:hover p {
  opacity: 1;
  -webkit-transform: scale3d(1, 1, 1);
  transform: scale3d(1, 1, 1);
}
</style>
