<template>
  <div>
    <div class="wrapper">
      <div class="loading" v-if="isLoading">
        <img lazyload src="~/assets/img/logo-comuna.png" />
        <progress-bar
          class="loadingBar"
          bar-color="#fff"
          bg-color="#e40524"
          text-fg-color="#fff"
          size="medium"
          :val="increasing_pct"
          :text="increasing_pct + '%'"
        />
      </div>
      <div class="instructions" v-show="isCover">
        <p>Disfruta una navegación única, deslizando hacia abajo</p>
        <img src="~/assets/img/scroll.png" />
        <button class="instructions_btn" @click="isCover = !isCover">
          Empezar a navegar
        </button>
      </div>
      <span id="bricsa-square" class="bricsa-square"></span>
      <div class="section section01-container" id="section01">
        <div class="section-01">
          <div id="section-bg01" :class="{ move: !isCover }" />
          <img
            lazyload
            class="section-logo"
            src="~/assets/img/logo-comuna.png"
          />
          <div id="section-01__text">
            <p class="call">
              City Lovers
            </p>
            <p class="downgrade">
              Vive conectado a la energía urbana de Santiago
            </p>
          </div>
          <p id="section1_citylover" class="uptext">City Lovers</p>
        </div>
      </div>
      <div class="section section02-container" id="section02">
        <img src="~/assets/img/02.jpg" />
        <div class="section-02" id="section-02">
          <img src="~/assets/img/02-2.png" alt="" />
          <p class="title">Un edificio que</p>
          <p class="subtitle">marca tendencia</p>
          <p class="downgrade">Arquitectura integrada a la ciudad.</p>
        </div>
      </div>
      <div class="section section03-container" id="section03">
        <video
          muted
          playsinline
          autoplay
          loop
          preload="auto"
          class="section-bg"
        >
          <source src="~/assets/img/video01.mp4" type="video/mp4" />
        </video>
        <div class="section-03">
          <p class="title" id="section-03_title">
            La naturaleza también vive en la ciudad
          </p>
          <div class="section-03_02" id="section-03_02">
            <p class="title02">Jardineras colgantes</p>
            <p class="subtitle">La naturaleza siempre es una gran compañera.</p>
          </div>
          <img
            src="~/assets/img/08.jpg"
            class="section-03_02-img"
            id="section-03_02-img"
          />
        </div>
      </div>
      <div class="section section04-container" id="section04">
        <div class="section-04">
          <img
            src="~/assets/img/06.jpg"
            class="section04_img"
            id="section04_img"
          />
        </div>
      </div>
      <div class="section section05-container" id="section05">
        <div class="section-05">
          <div class="section05_video">
            <video
              muted
              playsinline
              autoplay
              loop
              preload="auto"
              class="section-bg"
              id="section05_video"
            >
              <source src="~/assets/img/video02.mp4" type="video/mp4" />
            </video>
            <p id="section05_video-text" class="title">¿Hagamos un picnic?</p>
          </div>
          <div class="section05_img">
            <img src="~/assets/img/12.jpg" id="section05_img" />
            <p id="section05_img-text" class="subtitle">
              Rodeado de plazas y áreas verdes
            </p>
          </div>
        </div>
      </div>
      <div class="section section06-container" id="section06">
        <div class="section-06">
          <video
            muted
            playsinline
            autoplay
            loop
            preload="auto"
            class="section-bg"
            id="section06_video"
          >
            <source src="~/assets/img/video03.mp4" type="video/mp4" />
          </video>
          <div id="section06_text">
            <p class="title">Conectado con</p>
            <p class="subtitle">una gran ciclovía</p>
          </div>
        </div>
      </div>
      <div class="section section07-container" id="section07">
        <video
          muted
          playsinline
          autoplay
          loop
          preload="auto"
          class="section-bg"
          id="section07_video"
        >
          <source src="~/assets/img/video04.mp4" type="video/mp4" />
        </video>
        <div class="section-07">
          <div class="section07_text">
            <p class="title">54</p>
            <p class="subtitle">
              <strong>bicicleteros con taller</strong><br />en acceso al
              edificio
            </p>
          </div>
          <p class="downgrade" id="section07_downgrade">
            Una ciudad que se pedalea es una mejor ciudad
          </p>
        </div>
      </div>
      <div class="section section08-container" id="section08">
        <video
          muted
          playsinline
          autoplay
          loop
          preload="auto"
          class="section-bg"
          id="section08_video"
        >
          <source src="~/assets/img/video05.mp4" type="video/mp4" />
        </video>
        <div class="section-08">
          <img src="~/assets/img/14.jpg" />
          <p class="title">¿Un cafecito?</p>
          <p class="subtitle">
            El corazón de <br />
            Providencia <br />
            está lleno de ellos.
          </p>
        </div>
      </div>
      <div class="section section09-container" id="section09">
        <video
          muted
          playsinline
          autoplay
          loop
          preload="auto"
          class="section-bg"
          id="section09_video"
        >
          <source src="~/assets/img/video06.mp4" type="video/mp4" />
        </video>
        <div class="section-09">
          <p class="title">¡Voy y vuelvo!</p>
          <p class="subtitle">
            Cercano a cafeterías, almacenes de barrios y servicios.
          </p>
        </div>
      </div>
      <div class="section section10-container" id="section10">
        <img class="section-bg" id="section10_bg" src="~/assets/img/05.jpg" />
        <div class="section-10" id="section10-content">
          <img src="~/assets/img/11.jpg" />
          <p class="title">La ciudad también se merece un descanso</p>
        </div>
      </div>
      <div class="section section11-container" id="section11">
        <img class="section-bg" id="section11_bg" src="~/assets/img/15.jpg" />
        <div class="section-11" id="section11-content">
          <p class="title">Un City lover pone ojo en...</p>
          <p class="subtitle">los detalles</p>
          <p class="downgrade">Terminaciones de 1er nivel.</p>
        </div>
      </div>
      <div class="section section12-container" id="section12">
        <img class="section-bg" id="section12_bg" src="~/assets/img/04.jpg" />
        <div class="section-12" id="section12_content">
          <p class="title">Nada como</p>
          <p class="subtitle">una buena ducha</p>
          <p class="downgrade">Cómodo baño principal con shower door.</p>
        </div>
      </div>
      <div class="section section13-container" id="section13">
        <img class="section-bg" id="section13_bg" src="~/assets/img/08.jpg" />
        <img id="section13_img" src="~/assets/img/10.jpg" />
        <div id="section13_content" class="section-13">
          <p class="title">Lleva la entretención a lo más alto</p>
          <p class="subtitle">Departamentos con terraza privada en rooftop.</p>
        </div>
      </div>
      <div class="section section14-container" id="section14">
        <img class="section-bg" id="section14_bg" src="~/assets/img/13.jpg" />
        <img id="section14_img" src="~/assets/img/03.jpg" />
        <p class="title" id="section14_title">Áreas comunes</p>
        <div id="section14_content" class="section-14">
          <p class="subtitle">Un City lover</p>
          <p class="downgrade">sabe pasarlo bien</p>
        </div>
      </div>
      <div class="section section15-container" id="section15">
        <video
          muted
          playsinline
          autoplay
          loop
          preload="auto"
          class="section-bg"
          id="section15_video"
        >
          <source src="~/assets/img/video07.mp4" type="video/mp4" />
        </video>
        <div class="section15_img01"></div>
        <div class="section15_img02"></div>
        <div class="section-15">
          <img src="~/assets/img/07.jpg" />
          <p class="title">Cuando la temperatura sube:</p>
          <p class="subtitle" id="section15_subtitle">
            ¡baja y refréscate!
          </p>
          <p class="downgrade" id="section15_downgrade">
            Piscina, Quincho y Salón Gourmet.
          </p>
        </div>
      </div>
      <div class="section section16-container" id="section16">
        
        <video
          muted
          playsinline
          autoplay
          loop
          preload="auto"
          class="section-bg"
          id="section16_video"
        >
          <source src="~/assets/img/video08.mp4" type="video/mp4" />
        </video>
        <div class="section-16">
          <p class="title">¿eres?</p>
          <p class="subtitle">
            #Citylover
          </p>
          <img lazyload src="~/assets/img/logo-comuna.png" />
        </div>
      </div>
      <div class="section section17-container" id="section17">
        <div class="section-17">
          <img lazyload class="logo" src="~/assets/img/bricsa.png" />

          <img lazyload class="bptl" src="~/assets/img/bptl.png" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ProgressBar from "vue-simple-progress";
export default {
  components: {
    ProgressBar
  },
  data() {
    return {
      isLoading: true,
      increasing_pct: 0,
      isCover: true
    };
  },
  mounted: function() {
    this.startAnimations();
  },
  methods: {
    startAnimations: function() {
      var tl = new TimelineMax({ onUpdate: updatePercentage });
      tl.to("#bricsa-square", 96, { top: "90%" }, 0);
      tl.to("#section-bg01", 2, { "background-position-x": "-630px" }, 0);
      tl.to("#section1_citylover", 3, { bottom: "100%" }, 0);
      tl.to("#section01", 2, { top: "-100%" }, 3);
      tl.to("#section-02", 2, { top: "-100%" }, 6);
      tl.to("#section02", 2, { top: "-100%" }, 7);
      tl.to("#section-03_title", 2, { top: "-100%" }, 10);
      tl.to("#section-03_02", 2, { top: "30%" }, 12);
      tl.to("#section-03_02-img", 2, { left: "0" }, 12);
      tl.to("#section-03_02", 2, { opacity: "0" }, 15);
      tl.to("#section-03_02-img", 2, { left: "-90%" }, 15);
      tl.to("#section03", 2, { top: "-100%" }, 17);
      tl.to("#section04_img", 7, { "object-position": "100%" }, 19);
      tl.to("#section04", 2, { top: "-100%" }, 27);
      tl.to("#section05_video-text", 2, { bottom: "10%" }, 30);
      tl.to("#section05_img-text", 2, { bottom: "30%" }, 30);
      tl.to("#section05", 2, { top: "-100%" }, 33);
      tl.to("#section06_text", 2, { top: "0" }, 35);
      tl.to("#section06", 2, { top: "-100%" }, 38);
      tl.to("#section07_downgrade", 2, { bottom: "10%" }, 40);
      tl.to("#section07", 2, { top: "-100%" }, 42);
      tl.to("#section08", 2, { top: "-100%" }, 45);
      tl.to("#section09", 2, { top: "-100%" }, 48);
      tl.to("#section10_bg", 3, { "object-position": "100%" }, 51);
      tl.to("#section10-content", 2, { opacity: "1", filter: "blur(0)" }, 52);
      tl.to("#section10", 2, { top: "-100%" }, 54);
      tl.to("#section11_bg", 4, { right: "0%" }, 56);
      tl.to("#section11", 2, { top: "-100%" }, 60);
      tl.to("#section12_bg", 4, { right: "0" }, 62);
      tl.to("#section12_content", 2, { opacity: "1", filter: "blur(0)" }, 63);
      tl.to("#section12", 2, { top: "-100%" }, 66);
      tl.to("#section13_bg", 2, { left: "-60%" }, 68);
      tl.to("#section13_img", 2, { top: "0" }, 69);
      tl.to("#section13_content", 2, { opacity: "1", filter: "blur(0)" }, 69);
      tl.to("#section13", 2, { top: "-100%" }, 72);
      tl.to("#section14_title", 4, { left: "-220%" }, 75);
      tl.to("#section14", 2, { top: "-100%" }, 80);
      tl.to("#section15_subtitle", 2, { bottom: "40%" }, 83);
      tl.to("#section15_downgrade", 2, { bottom: "30%" }, 85);
      tl.to("#section15", 2, { top: "-100%" }, 88);
      tl.to("#section16", 2, { top: "-100%" }, 91);

      const scene = this.$scrollmagic
        .scene({
          triggerElement: ".wrapper",
          triggerHook: 0,
          duration: "5000%"
        })
        .setPin(".wrapper")
        .setTween(tl);

      this.$scrollmagic.addScene(scene);

      function updatePercentage() {
        tl.progress();
      }
    },
    load() {
      this.isLoading = true;
      setTimeout(() => {
        this.isLoading = false;
      }, 5000);
    }
  },
  created() {
    this.load();
    setInterval(() => {
      if (this.is_paused) return;

      this.increasing_pct = Math.min(this.increasing_pct + 1, 100);
    }, 23);
  }
};
</script>

<style>
.wrapper {
  max-width: 426px;
  width: 100% !important;
  overflow: hidden;
  margin: 0 auto;
  font-family: "Source Sans Pro", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
  position: relative;
  justify-content: center;
  align-items: flex-end;
}
body {
  max-width: 426px;
  margin: 0 auto !important;
}
.lookbook-container {
  position: relative;
}
.section {
  position: relative;
  overflow: hidden;
  width: 100%;
  min-height: 100vh;
}
.bricsa-square {
  display: block;
  position: absolute;
  right: 0;
  top: 20px;
  width: 50px;
  height: 50px;
  background: #e40524;
  z-index: 99;
}
.section-bg {
  height: 100%;
  object-fit: cover;
  position: absolute;
  z-index: -1;
  left: -100%;
}
#section01,
#section02,
#section03,
#section04,
#section05,
#section06,
#section07,
#section08,
#section09,
#section10,
#section11,
#section12,
#section13,
#section14,
#section15,
#section16,
#section17 {
  top: 0%;
  position: absolute !important;
  transition-timing-function: ease;
  transition-duration: 100ms;
}
#section01 {
  z-index: 19;
}
#section02 {
  z-index: 18;
}
#section03 {
  z-index: 17;
}
#section04 {
  z-index: 16;
}
#section05 {
  z-index: 15;
}
#section06 {
  z-index: 14;
}
#section07 {
  z-index: 13;
}
#section08 {
  z-index: 12;
}
#section09 {
  z-index: 11;
}
#section10 {
  z-index: 10;
}
#section11 {
  z-index: 9;
}
#section12 {
  z-index: 8;
}
#section13 {
  z-index: 7;
}
#section14 {
  z-index: 6;
}
#section15 {
  z-index: 5;
}
#section16 {
  z-index: 4;
}
#section17 {
  z-index: 3;
}
.loading {
  transition: all 1s both;
  background: #e40524;
  z-index: 100;
  position: absolute;
  display: grid;
  grid-template-rows: repeat(2, min-content);
  row-gap: 20px;
  justify-content: center;
  justify-items: center;
  align-items: center;
  align-content: center;
  width: 100%;
  height: 100%;
}
.loading img {
  animation: breath 1s both infinite alternate-reverse;
  width: 40%;
}
.loading .loadingBar {
  width: 60%;
}
@keyframes breath {
  0% {
    transform: scale(0.9);
  }
  100% {
    transform: scale(1);
  }
}
.instructions {
  background: #e40524;
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: grid;
  grid-template-rows: min-content 80px min-content;
  justify-content: center;
  justify-items: center;
  align-content: center;
  align-items: center;
  row-gap: 30px;
  z-index: 20;
}
.instructions p {
  color: #fff;
  font-size: 26px;
  width: 90%;
  text-align: center;
  font-weight: 300;
}
.instructions img {
  width: 10%;
  animation: arrow-down 0.5s both infinite alternate-reverse;
}
@keyframes arrow-down {
  0% {
    margin-top: 0;
  }
  100% {
    margin-top: 10px;
  }
}
.instructions .instructions_btn {
  color: #fff;
  background: rgba(0, 0, 0, 0);
  border: solid 2px #fff;
  border-radius: 10px;
  padding: 10px;
  cursor: pointer;
  transition: 400ms;
}
.instructions .instructions_btn:hover {
  background: #b9041c;
}
.section01-container #section-bg01 {
  width: 100%;
  height: 100vh;
  background: url("~/assets/img/01.jpg") no-repeat;
  background-position-x: -100px;
  filter: brightness(0.8);
}
.section01-container .section-01 {
  background: rgba(0, 0, 0, 0.3);
  width: 100%;
  height: 100%;
  position: absolute;
  display: block;
  top: 0;
  left: 0;
  z-index: 1;
}
.section01-container .section-01 .section-logo {
  width: 100px;
  position: absolute;
  top: 50px;
  left: 20px;
}
.section01-container .section-01 .call {
  transition: all 400ms;
  text-align: left;

  color: #fff;
  font-size: 54px;
  font-weight: bolder;
  line-height: 0.8;
}
.section01-container .section-01 .downgrade {
  text-align: left;
  color: #fff;
  font-size: 29px;
  font-weight: 300;
  line-height: 1;
}
.section01-container .section-01 #section1_citylover {
  transform: rotate(-90deg) scale(2.2);
  font-size: 120px;
  position: absolute;
  right: -230px;
  margin: 0;
  font-weight: bolder;
  color: #e40524;
  bottom: -180%;
  z-index: 1;
  white-space: nowrap;
}
.section01-container .section-01 #section-01__text {
  width: 70%;
  display: grid;
  row-gap: 20px;
  position: absolute;
  top: 28%;
  left: 20px;
  z-index: 2;
}
.section02-container {
  position: relative;
}
.section02-container img {
  width: 100%;
  height: 100%;
  left: 0;
  position: absolute;
  object-fit: cover;
}
.section02-container .section-02 {
  position: absolute;
  width: 80%;
  height: 60%;
  left: 10%;
  top: 20%;
  display: grid;
  justify-content: center;
  justify-items: center;
  align-items: center;
  align-content: center;
  grid-template-rows: repeat(3, min-content);
  row-gap: 20px;
}
.section02-container .section-02 img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: brightness(0.7);
  z-index: 0;
}
.section02-container .section-02 .title {
  color: #fff;
  width: 100%;
  font-size: 40px;
  text-align: center;
  top: 20%;
  font-weight: 300;
  line-height: 0.9;
  z-index: 1;
}
.section02-container .section-02 .subtitle {
  color: #fff;
  width: 100%;
  font-weight: 800;
  font-size: 50px;
  text-align: center;
  top: 30%;
  line-height: 1;
  z-index: 1;
}
.section02-container .section-02 .downgrade {
  color: #fff;
  width: 80%;
  font-weight: 300;
  font-size: 30px;
  text-align: center;
  top: 70%;
  left: 10%;
  line-height: 1;
  z-index: 1;
}
.section-03 {
  position: relative;
}
.section03-container .section-bg {
  position: absolute;
  z-index: 3;
  width: 100%;
  height: 100vh;
  top: 0;
  left: 0;
}
.section03-container .section-03 {
  background: rgba(0, 0, 0, 0.3);
  width: 100%;
  height: 100%;
  position: absolute;
  display: block;
  top: 0;
  left: 0;
  z-index: 3;
  display: grid;
  align-items: center;
  justify-content: center;
}
.section03-container .section-03 .title {
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  color: #fff;
  width: 80%;
  height: 40%;
  font-size: 60px;
  text-align: center;
  top: 30%;
  left: 10%;
  font-weight: 800;
  line-height: 0.9;
  z-index: 3;
}

.section03-container .section-03 .section-03_02 {
  position: absolute;
  top: 100%;
  left: 10%;
  width: 80%;
  height: 40%;
  display: grid;
  justify-items: center;
  align-items: center;
  row-gap: 20px;
  grid-template-rows: repeat(2, min-content);
  z-index: 2;
}

.section03-container .section-03 .section-03_02 .title02 {
  font-size: 56px;
  color: #fff;
  font-weight: 800;
  text-align: center;
  line-height: 1;
}

.section03-container .section-03 .section-03_02 .subtitle {
  font-size: 26px;
  font-weight: 300;
  text-align: center;
  color: #fff;
}

.section03-container .section-03 .section-03_02-img {
  position: absolute;
  height: 80%;
  width: 70%;
  top: 10%;
  left: -90%;
  object-fit: cover;
  object-position: 90% 0;
  filter: brightness(0.7);
  z-index: 1;
}

.section04-container .section-04 img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  object-fit: cover;
  object-position: 0 0;
  filter: brightness(0.8);
}

.section05-container .section-bg {
  height: 70%;
  width: 100%;
  object-fit: cover;
  position: absolute;
  z-index: -1;
  left: 0;
  filter: brightness(0.6);
}
.section05-container .section-05 {
  background: rgba(0, 0, 0, 0.3);
  width: 100%;
  height: 100%;
  position: absolute;
  display: block;
  top: 0;
  left: 0;
  z-index: 1;
}
.section05-container .section-05 .section05_video {
  width: 100%;
  height: 70%;
  position: relative;
}
.section05-container .section-05 #section05_video {
  height: 100%;
}
.section05-container .section-05 #section05_video-text {
  position: absolute;
  bottom: -50%;
  left: 5%;
  color: #fff;
  width: 90%;
  font-size: 60px;
  text-align: center;
  font-weight: 800;
  line-height: 0.9;
}
.section05-container .section-05 #section05_img-text {
  position: absolute;
  bottom: -50%;
  width: 80%;
  left: 10%;
  color: #fff;
  font-size: 36px;
  font-weight: 300;
  text-align: center;
  line-height: 1;
}
.section05-container .section-05 .section05_img {
  width: 100%;
  height: 30%;
  object-fit: cover;
  object-position: center;
  position: absolute;
  bottom: 0;
  left: 0;
}
.section05-container .section-05 #section05_text {
  position: absolute;
  top: 100%;
  width: 80%;
  height: 30%;
  left: 10%;
  display: grid;
  grid-template-rows: repeat(2, min-content);
  row-gap: 10px;
  justify-items: center;
  align-items: center;
}
.section05-container .section-05 .section05_img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  filter: brightness(0.6);
}
.section06-container .section-bg {
  filter: brightness(0.6);
}
.section06-container .section-06 #section06_text {
  padding: 10px 0;
  position: absolute;
  display: grid;
  grid-template-rows: repeat(2, min-content);
  row-gap: 10px;
  justify-content: center;
  justify-items: center;
  align-items: center;
  align-content: center;
  top: -300px;
  left: 0;
  width: 100%;
  height: 300px;
}
.section06-container .section-06 .title {
  color: #fff;
  width: 90%;
  font-size: 50px;
  text-align: center;
  top: 5%;
  left: 5%;
  font-weight: 300;
  line-height: 0.9;
  margin: 0;
}
.section06-container .section-06 .subtitle {
  color: #fff;
  width: 80%;
  font-size: 70px;
  font-weight: 800;
  text-align: center;
  top: 20%;
  left: 10%;
  line-height: 1;
  margin: 0;
}
.section07-container .section-bg {
  left: 0;
  width: 100%;
  filter: brightness(0.7);
}
.section07-container .section07_text {
  width: 100%;
  height: 60%;
  position: absolute;
  display: grid;
  grid-template-rows: repeat(3, min-content);
  justify-content: center;
  justify-items: center;
  align-content: center;
  align-items: center;
  top: 0;
  left: 0;
  z-index: 1;
}
.section07-container .section-07 .title {
  color: #fff;
  width: 90%;
  font-size: 230px;
  text-align: center;
  font-weight: 800;
  line-height: 0.9;
}
.section07-container .section-07 .subtitle {
  color: #fff;
  width: 80%;
  font-size: 60px;
  font-weight: 300;
  text-align: center;
  line-height: 1;
}
.section07-container .section-07 .downgrade {
  position: absolute;
  bottom: -10%;
  color: #fff;
  width: 80%;
  font-size: 26px;
  font-weight: 300;
  left: 10%;
}
.section08-container .section-bg {
  position: absolute;
  height: 100vh;
  filter: brightness(0.7);
  z-index: 0;
}
.section08-container .section-08 {
  position: absolute;
  display: grid;
  grid-template-rows: repeat(2, min-content);
  row-gap: 10px;
  justify-content: center;
  justify-items: center;
  align-items: center;
  align-content: center;
  width: 80%;
  height: 80%;
  top: 10%;
  left: 10%;
  color: #fff;
}
.section08-container .section-08 img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  filter: brightness(0.7);
  position: absolute;
  left: 0;
  top: 0;
}
.section08-container .section-08 .title {
  color: #fff;
  width: 90%;
  font-size: 50px;
  text-align: center;
  font-weight: 800;
  line-height: 1.1;
  z-index: 1;
}
.section08-container .section-08 .subtitle {
  color: #fff;
  width: 80%;
  font-size: 24px;
  font-weight: 300;
  text-align: center;
  line-height: 1.2;
  z-index: 1;
}
.section09-container .section-bg {
  position: absolute;
  height: 100vh;
  filter: brightness(0.6);
  z-index: 0;
}
.section09-container .section-09 {
  position: absolute;
  display: grid;
  grid-template-rows: repeat(2, min-content);
  row-gap: 10px;
  justify-content: center;
  justify-items: center;
  align-items: center;
  align-content: center;
  width: 90%;
  height: 80%;
  top: 10%;
  left: 5%;
  color: #fff;
}
.section09-container .section-09 .title {
  color: #fff;
  width: 90%;
  font-size: 70px;
  text-align: center;
  font-weight: 800;
  line-height: 1.1;
  z-index: 1;
}
.section09-container .section-09 .subtitle {
  color: #fff;
  width: 80%;
  font-size: 36px;
  font-weight: 300;
  text-align: center;
  line-height: 1.2;
  z-index: 1;
}
.section10-container .section-bg {
  position: absolute;
  height: 100vh;
  width: 100%;
  filter: brightness(0.7);
  left: 0;
  object-fit: cover;
  object-position: 0;
}
.section10-container .section-10 {
  position: absolute;
  display: grid;
  justify-content: center;
  justify-items: center;
  align-items: center;
  align-content: center;
  width: 80%;
  height: 100%;
  top: 0;
  left: 10%;
  color: #fff;
  opacity: 0;
  filter: blur(20px);
}
.section10-container .section-10 img {
  filter: brightness(0.8);
  width: 100%;
  height: 300px;
  object-fit: cover;
  grid-column: 1/2;
  grid-row: 1/2;
}
.section10-container .section-10 .title {
  color: #fff;
  width: 90%;
  font-size: 60px;
  text-align: center;
  font-weight: 800;
  line-height: 0.9;
  grid-column: 1/2;
  grid-row: 1/2;
  z-index: 1;
}
.section10-container .section-10 .subtitle {
  position: absolute;
  color: #fff;
  width: 80%;
  font-size: 26px;
  font-weight: 300;
  text-align: center;
  bottom: 10%;
  left: 10%;
  line-height: 1;
  filter: blur(20px);
  opacity: 0;
}
.section11-container .section-bg {
  filter: brightness(0.7);
  right: -100%;
  left: auto;
}
.section11-container .section-11 {
  color: #fff;
  display: grid;
  padding: 30px;
  position: absolute;
  width: 100%;
  bottom: 20%;
  left: 0;
}
.section11-container .section-11 .title {
  z-index: 2;
  width: 80%;
  justify-self: flex-start;
  text-align: left;
  font-size: 44px;
  font-weight: 400;
}
.section11-container .section-11 .subtitle {
  z-index: 2;
  width: 70%;
  justify-self: flex-end;
  font-size: 64px;
  font-weight: 800;
  text-align: left;
  line-height: 1;
}
.section11-container .section-11 .downgrade {
  z-index: 2;
  font-size: 20px;
  width: 70%;
  justify-self: flex-end;
  text-align: left;
}
.section12-container .section-bg {
  right: -30%;
  left: auto;
  object-position: 100%;
  filter: brightness(0.7);
}
.section12-container .section-12 {
  display: grid;
  grid-template-rows: repeat(3, min-content);
  row-gap: 10px;
  padding: 20px;
  background: #fff;
  width: 60%;
  height: min-content;
  color: #444;
  z-index: 2;
  position: absolute;
  left: 0;
  bottom: 5%;
  opacity: 0;
  filter: blur(20px);
}
.section12-container .section-12 .title {
  font-size: 40px;
  font-weight: 300;
  line-height: 0.9;
}
.section12-container .section-12 .subtitle {
  font-size: 60px;
  font-weight: 800;
  line-height: 0.9;
}
.section12-container .section-12 .downgrade {
  font-size: 17px;
  font-weight: 400;
}
.section13-container .section-bg {
  position: absolute;
  height: 100%;
  filter: brightness(0.7);
  left: 0;
}
.section13-container .section-13 {
  color: #fff;
  display: grid;
  height: 100vh;
  grid-template-rows: repeat(2, min-content);
  justify-content: center;
  align-items: center;
  align-content: center;
  justify-items: center;
  row-gap: 10px;
  opacity: 0;
  filter: blur(20px);
}
.section13-container #section13_img {
  position: absolute;
  top: -40%;
  left: 15%;
  width: 70%;
  height: 250px;
  object-fit: cover;
  filter: brightness(0.7);
}
.section13-container .section-13 .title {
  z-index: 2;
  width: 80%;
  font-size: 38px;
  font-weight: 800;
  line-height: 1;
}
.section13-container .section-13 .subtitle {
  z-index: 2;
  width: 80%;
  font-size: 29px;
  font-weight: 300;
  line-height: 0.9;
}
.section14-container {
  background: #fff;
}
.section14-container .section-bg {
  height: 90vh;
  position: absolute;
  top: 0;
  left: 0;
  object-fit: cover;
}
.section14-container .section-14 {
  color: #fff;
  width: 100%;
  height: 100vh;
  display: grid;
  grid-template-rows: repeat(2, min-content);
  grid-template-columns: 100%;
  justify-content: center;
  justify-items: center;
  align-content: center;
  align-items: center;
}
.section14-container #section14_img {
  width: 60%;
  height: 30%;
  position: absolute;
  bottom: 0;
  right: 0;
  object-fit: cover;
  object-position: center;
}
.section14-container .title {
  z-index: 2;
  position: absolute;
  width: 80%;
  left: 0;
  top: -5%;
  font-size: 170px;
  font-weight: 800;
  line-height: 1;
  white-space: nowrap;
  color: #e40524;
}
.section14-container .section-14 .subtitle {
  z-index: 2;
  width: 90%;
  font-size: 60px;
  text-align: center;
  font-weight: 300;
}
.section14-container .section-14 .downgrade {
  z-index: 2;
  width: 90%;
  font-size: 60px;
  text-align: center;
  font-weight: 800;
  line-height: 1;
}
.section15-container .section-bg {
  height: 100vh;
}
.section15-container .section-15 {
  color: #fff;
  position: absolute;
  row-gap: 20px;
  justify-content: center;
  justify-items: center;
  align-items: center;
  align-content: center;
  width: 80%;
  height: 80%;
  top: 10%;
  left: 10%;
}
.section15-container .section-15 img {
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  object-fit: cover;
  object-position: right;
  filter: brightness(0.7);
}

.section15-container .section15_img01 {
  background-image: url("~/assets/img/03.jpg");
  background-size: 200%;
  background-position: bottom right;
  position: absolute;
  top: 0;
  right: 0;
  width: 40%;
  z-index: 2;
  height: 150px;
  object-fit: cover;
  filter: brightness(0.7);
}

.section15-container .section15_img02 {
  background-image: url("~/assets/img/09.jpg");
  background-size: 200%;
  background-position: bottom right;
  position: absolute;
  bottom: 0;
  left: 0;
  width: 40%;
  z-index: 2;
  height: 150px;
  object-fit: cover;
  filter: brightness(0.7);
}
.section15-container .title {
  z-index: 2;
  width: 80%;
  font-size: 40px;
  font-weight: 300;
  line-height: 1;
  align-self: flex-start;
  position: absolute;
  top: 20%;
  left: 10%;
}
.section15-container .section-15 .subtitle {
  z-index: 2;
  width: 80%;
  font-size: 50px;
  text-align: center;
  font-weight: 800;
  position: absolute;
  bottom: -50%;
  left: 10%;
}
.section15-container .section-15 .downgrade {
  z-index: 2;
  width: 80%;
  font-size: 30px;
  text-align: center;
  font-weight: 400;
  line-height: 1;
  position: absolute;
  bottom: -50%;
  left: 10%;
}
.section16-container .section-bg {
  left: 0;
  width: 100%;
  filter: brightness(0.7);
}
.section16-container .section-16 {
  color: #fff;
  width: 80%;
  height: 70%;
  position: absolute;
  top: 10%;
  left: 10%;
  display: grid;
  grid-template-columns: 100%;
  grid-template-rows: min-content min-content 30%;
  row-gap: 20px;
  justify-content: center;
  justify-items: center;
  align-content: flex-end;
  align-items: center;
}
.section16-container .section-16 .title {
  color: #fff;
  width: 100%;
  font-size: 50px;
  text-align: center;
  font-weight: 800;
  line-height: 0.9;
}
.section16-container .section-16 .subtitle {
  color: #fff;
  width: 100%;
  font-size: 60px;
  font-weight: 300;
  text-align: center;
  line-height: 1;
}
.section16-container .section-16 img {
  width: 50%;
  align-self: flex-end;
}
.section17-container {
  background: #e40524;
  display: flex;
}
.section17-container .section-17 {
  display: grid;
  height: 100%;
  grid-template-columns: 100%;
  grid-template-rows: repeat(2, min-content);
  row-gap: 30px;
  justify-content: center;
  justify-items: center;
  align-items: center;
  align-content: center;
  align-self: center;
}
.section17-container .section-17 .logo {
  width: 60%;
}
.section17-container .section-17 .bptl {
  width: 40%;
}

@media screen and (max-height: 735px) {
  .section15-container .title {
    font-size: 30px;
  }
  .section15-container .section-15 .subtitle {
    font-size: 44px;
  }
  .section15-container .section-15 .downgrade {
    font-size: 26px;
  }
}

@media screen and (max-width: 378px) {
  .section01-container .section-01 .call {
    font-size: 44px;
    bottom: 40%;
  }
  .section01-container .section-01 #section1_citylover {
    font-size: 130px;
    right: -270px;
  }
  .section02-container .section-02 .title {
    font-size: 40px;
  }
  .section02-container .section-02 .subtitle {
    font-size: 50px;
  }
  .section02-container .section-02 .downgrade {
    font-size: 27px;
  }
  .section03-container .section-03 .subtitle {
    font-size: 25px;
    bottom: 15%;
  }
  .section03-container .section-03 .section-03_02 .title02 {
    font-size: 50px;
  }
  .section03-container .section-03 .subtitle02 {
    font-size: 25px;
    bottom: 15%;
  }
  .section05-container .section-05 .title {
    font-size: 50px;
  }
  .section06-container .section-06 .title {
    font-size: 40px;
  }
  .section06-container .section-06 .subtitle {
    font-size: 60px;
  }
  .section08-container .section-08 .title {
    font-size: 50px;
  }
  .section08-container .section-08 .subtitle {
    font-size: 24px;
  }
  .section09-container .section-09 .subtitle {
    font-size: 26px;
  }
  .section10-container .section-10 .title {
    font-size: 50px;
  }
  .section11-container .section-11 .title {
    font-size: 34px;
  }
  .section11-container .section-11 .subtitle {
    font-size: 50px;
  }
  .section11-container .section-11 .downgrade {
    font-size: 16px;
  }
  .section12-container .section-12 .title {
    font-size: 32px;
  }
  .section12-container .section-12 .downgrade {
    font-size: 14px;
  }
  .section13-container .section-13 .title {
    font-size: 38px;
  }
  .section13-container .section-13 .subtitle {
    font-size: 26px;
  }
  .section14-container .section-14 .subtitle {
    font-size: 49px;
  }
  .section14-container .section-14 .downgrade {
    font-size: 60px;
  }
  .section15-container .title {
    font-size: 30px;
  }
  .section15-container .section-15 .subtitle {
    font-size: 44px;
  }
  .section15-container .section-15 .downgrade {
    font-size: 26px;
  }
}
@media screen and (max-width: 321px) {
  .section01-container .section-01 .call {
    font-size: 40px;
  }

  .section02-container .section-02 .downgrade {
    font-size: 23px;
  }
  .section05-container .section-05 .title {
    font-size: 46px;
  }
  .section05-container .section-05 .subtitle {
    top: 21%;
  }
  .section06-container .section-06 .subtitle {
    font-size: 50px;
  }
  .section07-container .section-07 .subtitle {
    font-size: 40px;
  }
  .section10-container .section-10 .title {
    font-size: 46px;
  }
  .section11-container .section-11 .title {
    font-size: 32px;
  }
  .section12-container .section-12 .subtitle {
    font-size: 50px;
  }

  .section13-container .section-13 .title {
    font-size: 32px;
    bottom: 63%;
  }

  .section13-container .section-13 .downgrade {
    font-size: 20px;
  }

  .section15-container .title {
    font-size: 26px;
  }
  .section15-container .section-15 .subtitle {
    font-size: 40px;
  }
  .section15-container .section-15 .downgrade {
    font-size: 24px;
  }
}
</style>
