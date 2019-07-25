<template>
  <div class="grid">
    <figure class="effect-julia">
      <img src="../../assets/img/24.jpg" alt="img21" />

      <figcaption>
        <h2>奋斗的少年</h2>
        <div>
          <p>把每一天都过好</p>
          <p>把每顿饭吃好</p>
          <p>把每件事情做好</p>
        </div>
      </figcaption>
    </figure>
  </div>
</template>

<script>
export default {};
</script>

<style>
@import url('../../assets/css/components.css');

figure.effect-julia {
  background: #2f3238;
}

figure.effect-julia img {
  max-width: none;
  height: 400px;
  -webkit-transition: opacity 1s, -webkit-transform 1s;
  transition: opacity 1s, transform 1s;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
}

figure.effect-julia figcaption {
  text-align: left;
}

figure.effect-julia h2 {
  position: relative;
  padding: 0.5em 0;
}

figure.effect-julia p {
  display: table;
  margin: 0 0 0.25em;
  padding: 0.4em 1em;
  background: rgba(255, 255, 255, 0.9);
  color: #2f3238;
  text-transform: none;
  font-weight: 500;
  font-size: 75%;
  transition: opacity 0.35s, transform 0.35s;
  transform: translate3d(-360px, 0, 0);
}

figure.effect-julia p:first-child {
  -webkit-transition-delay: 0.15s;
  transition-delay: 0.15s;
}

figure.effect-julia p:nth-of-type(2) {
  -webkit-transition-delay: 0.1s;
  transition-delay: 0.1s;
}

figure.effect-julia p:nth-of-type(3) {
  -webkit-transition-delay: 0.05s;
  transition-delay: 0.05s;
}

figure.effect-julia:hover p:first-child {
  -webkit-transition-delay: 0s;
  transition-delay: 0s;
}

figure.effect-julia:hover p:nth-of-type(2) {
  -webkit-transition-delay: 0.05s;
  transition-delay: 0.05s;
}

figure.effect-julia:hover p:nth-of-type(3) {
  -webkit-transition-delay: 0.1s;
  transition-delay: 0.1s;
}

figure.effect-julia:hover img {
  opacity: 0.4;
  -webkit-transform: scale3d(1.1, 1.1, 1);
  transform: scale3d(1.1, 1.1, 1);
}

figure.effect-julia:hover p {
  opacity: 1;
  -webkit-transform: translate3d(0, 0, 0);
  transform: translate3d(0, 0, 0);
}
</style>
