<template>
  <q-page stylçe=" height: 100vh;" class="flex bg-dark flex-center">
    <div class="bg-dark" style="width: 100vw; height: 100%;">
      <q-toolbar class="absolute-top">
        <q-toolbar-title class="titleFont">
          <q-btn to="/" size="lg" class=" q-pl-xl titleFont text-white text-bold" rounded flat class-flex-flex-center
            q-ma-sm>
            <q-img
              src="https://cdn.discordapp.com/attachments/459557016042471454/1022390261957021717/299085275_1297684320974924_880665858629312467_n-removebg-preview.png"
              style="width:3vw;">

            </q-img>
          </q-btn>
        </q-toolbar-title>

        <div class="text-dark q-gutter-md flex flex-center q-gutter-x-md q-py-md q-pr-xl row">
          <q-btn-group outline>
            <div style="border-radius: 5px;" class="flex q-ma-xs q-gutter-x-none bg-grey-7 ">
              <q-btn @click="pt = false" rounded color="dark" flat style="opacity: 0.8;"
                class="titleFont  text-white text-bold" v-if="pt" label="Sobre o Projeto" />
                <q-btn @click="pt = false" rounded color="dark" flat style="opacity: 0.8;"
                class="titleFont  text-white text-bold" v-if="!pt" label="About Project" />
                </div>
            <div style="border-radius: 5px;" class="flex q-ma-xs q-gutter-x-none bg-white">
              <q-btn @click="pt = false" rounded color="dark" flat style="opacity: 0.8;"
                class="titleFont  text-dark text-bold" v-if="pt" label="EN" />
              <q-btn @click="pt = true" rounded color="dark" flat style="opacity: 0.8;"
                class="titleFont text-dark text-bold" v-if="!pt" label="PT" />
            </div>
            <q-btn color="dark" flat style="opacity: 0.8;" icon="fa-brands text-white fa-discord" />
            <q-btn color="dark" flat style="opacity: 0.8;" icon="fa-brands text-white fa-twitter" />
          </q-btn-group>

        </div>
      </q-toolbar>

        <div style="width: 100vw; heigh: 14vh; margin-top: 25vh;" class="flex items-center justify-center flex-center text-center ">
          <h2 class="text-bold mainFont text-white">
            Founders <span class="blink">|</span>
          </h2>
        </div>

      <div style="width: 100vw; padding-bottom: 40vh; margin-top: 30vh;"
        class="container bg-dark flex q-mb-md row flex-center q-gutter-x-sm  justify-center">
        <div class="col bg-dark flex flex-center">
          <q-card style="top: -7em; border-radius: 25px;" class="my-card-xl q-mb-xl bg-transparent" flat bordered>
            <div style="border-radius: 25px;" class="flex items-center justify-center">
              <q-img style="border-radius: 25px 25px 0px 0px;" class="backgroundImage0-xl" />
            </div>


            <q-card-section style="opacity: 0.9" class="bg-black">
              <div class="text-overline textKdam text-white">co-founder.</div>
              <div class="text-h5 text-white textKdam q-mt-sm q-mb-xs">Fernando</div>
              <div class="text-caption textKdam bg-black text-grey">
                <span class="text-italic" v-if="pt">RainbowD</span> <span v-if="!pt">Aka RainbowD</span> <br> <br> <span
                  class="q-gutter-x-xs text-center"> </span>
                <span v-if="pt">Streamer/Empresário</span> <span v-if="!pt">Streamer/Businessman</span> <br> <br> <span
                  class="q-gutter-x-xs text-center">
                  <q-icon size="xs" color="green" name="fa-solid fa-flag" /> <span
                    class="text-bold text-subtitle2">BR</span>
                </span>
              </div>
            </q-card-section>

            <q-card-actions style="opacity: 0.8; border-radius: 0px 0px 4px 4px;" class="bg-black">
              <q-btn class="textKdam text-caption" icon-right="fa-brands fa-twitter" flat color="dark"
                text-color="white" />

              <q-space />
              <q-btn v-if="pt" class="text-bold text-italic text-white" :label="expanded1 ? 'OK' : 'Sobre'"
                color="white" rounded flat dense :icon="expanded1 ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded1 = !expanded1" />
              <q-btn v-if="!pt" class="text-bold text-italic text-white" :label="expanded1 ? 'OK' : 'About'"
                color="white" rounded flat dense :icon="expanded1 ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded1 = !expanded1" />
            </q-card-actions>

            <q-slide-transition style="border-radius: 0px 0px 30px 30px;">
              <div style="border-radius: 0px 0px 20px 20px;" v-show="expanded1">
                <q-separator />
                <q-card-section style="opacity: 0.9; border-radius: 0px 0px 20px 20px;"
                  class="text-subitle2 titleFont text-white bg-black">
                  <div v-if="pt" class="flex flex-center">
                    <span clas="text-h5">"</span> Streamer Brasileiro, Nº1 em CryptoGames , atualmente tem parcerias no
                    ramo de casino, e direciona suas
                    lives para tais assuntos. <br>
                    <span style="text-decoration: underline;" class="text-italic"> Criador do AlphaC </span> <span
                      clas="text-h5"> "</span>
                  </div>
                  <div v-if="!pt" class="flex flex-center">
                    <span clas="text-h5">"</span> Brazilian Streamer, Number 1 in crypto on SA and partner of some
                    online casino
                    <br>
                    <span style="text-decoration: underline;" class="text-italic">Alpha C creator</span> <span
                      clas="text-h5"> "</span>
                  </div>
                </q-card-section>
              </div>
            </q-slide-transition>
          </q-card>
        </div>
        <div class="col bg-dark flex flex-center">
          <q-card style="top: -7em; border-radius: 25px;" class="my-card-xl q-mb-xl bg-transparent" flat bordered>
            <div style="border-radius: 25px;" class="flex items-center justify-center">
              <q-img style="border-radius: 25px 25px 0px 0px;" class="backgroundImage1-xl" />
            </div>

            <q-card-section style="opacity: 0.9" class="bg-black">
              <div class="text-overline textKdam text-white">co-founder.</div>
              <div class="text-h5 text-white textKdam q-mt-sm q-mb-xs">Fernando</div>
              <div class="text-caption textKdam bg-black text-grey">
                <span class="text-italic" v-if="pt">Soneca</span> <span v-if="!pt">Aka Soneca</span> <br> <br> <span
                  class="q-gutter-x-xs text-center"> </span>
                <span v-if="pt">Streamer/Empresário</span> <span v-if="!pt">Streamer/Businessman</span> <br> <br> <span
                  class="q-gutter-x-xs text-center">
                  <q-icon size="xs" color="green" name="fa-solid fa-flag" /> <span
                    class="text-bold text-subtitle2">BR</span>
                </span>
              </div>
            </q-card-section>

            <q-card-actions style="opacity: 0.8; border-radius: 0px 0px 4px 4px;" class="bg-black">
              <q-btn class="textKdam text-caption" icon-right="fa-brands fa-twitter" flat color="dark"
                text-color="white" />

              <q-space />
              <q-btn v-if="pt" class="text-bold text-italic text-white" :label="expanded1 ? 'OK' : 'Sobre'"
                color="white" rounded flat dense :icon="expanded1 ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded1 = !expanded1" />
              <q-btn v-if="!pt" class="text-bold text-italic text-white" :label="expanded1 ? 'OK' : 'About'"
                color="white" rounded flat dense :icon="expanded1 ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded1 = !expanded1" />
            </q-card-actions>

            <q-slide-transition style="border-radius: 0px 0px 30px 30px;">
              <div style="border-radius: 0px 0px 20px 20px;" v-show="expanded1">
                <q-separator />
                <q-card-section style="opacity: 0.9; border-radius: 0px 0px 20px 20px;"
                  class="text-subitle2 titleFont text-white bg-black">
                  <div v-if="pt" class="flex flex-center">
                    <span clas="text-h5">"</span> Streamer Brasileiro, Nº1 em CryptoGames , atualmente tem parcerias no
                    ramo de casino, e direciona suas
                    lives para tais assuntos. <br>
                    <span style="text-decoration: underline;" class="text-italic"> Criador do AlphaC </span> <span
                      clas="text-h5"> "</span>
                  </div>
                  <div v-if="!pt" class="flex flex-center">
                    <span clas="text-h5">"</span> Brazilian Streamer, Number 1 in crypto on SA and partner of some
                    online casino
                    <br>
                    <span style="text-decoration: underline;" class="text-italic">Alpha C creator</span> <span
                      clas="text-h5"> "</span>
                  </div>
                </q-card-section>
              </div>
            </q-slide-transition>
          </q-card>
        </div>

        </div>
        <div style="width: 100vw; heigh: 14vh; margin-top: 15vh;" class="flex items-center justify-center flex-center text-center ">
          <h2 class="text-bold mainFont text-white">
            Team members <span class="blink">|</span>
          </h2>
        </div>

      <div style="width: 100vw; padding-bottom: 40vh; margin-top: 30vh;"
        class="container bg-dark flex q-mb-md row flex-center q-gutter-x-sm  justify-center">
        <div class="col bg-dark flex flex-center">
          <q-card style="top: -7em; border-radius: 25px;" class="my-card-xl q-mb-xl bg-transparent" flat bordered>
            <div style="border-radius: 25px;" class="flex items-center justify-center">
              <q-img style="border-radius: 25px 25px 0px 0px;" class="backgroundImage2-xl" />
            </div>

            <q-card-section style="opacity: 0.9" class="bg-black">
              <div class="text-overline textKdam text-white">CTO.</div>
              <div class="text-h5 text-white textKdam q-mt-sm q-mb-xs">Joey Diab</div>
              <div class="text-caption textKdam bg-black text-grey">
                <span class="text-italic" v-if="pt">gynchiii.sol</span> <span v-if="!pt">Aka gynchiii.sol</span> <br> <br> <span
                  class="q-gutter-x-xs text-center"> </span>
                <span class="text-bold" v-if="pt">Developer</span> <span v-if="!pt">Developer</span> <br> <br> <span
                  class="q-gutter-x-xs text-center">
                  <q-icon size="xs" color="green" name="fa-solid fa-flag" /> <span
                    class="text-bold text-subtitle2">BR</span>
                </span>
              </div>
            </q-card-section>

            <q-card-actions style="opacity: 0.8; border-radius: 0px 0px 4px 4px;" class="bg-black">
              <q-btn class="textKdam text-caption" icon-right="fa-brands fa-twitter" flat color="dark"
                text-color="white" />

              <q-space />
              <q-btn v-if="pt" class="text-bold text-italic text-white" :label="expanded1 ? 'OK' : 'Sobre'"
                color="white" rounded flat dense :icon="expanded1 ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded1 = !expanded1" />
              <q-btn v-if="!pt" class="text-bold text-italic text-white" :label="expanded1 ? 'OK' : 'About'"
                color="white" rounded flat dense :icon="expanded1 ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded1 = !expanded1" />
            </q-card-actions>

            <q-slide-transition style="border-radius: 0px 0px 30px 30px;">
              <div style="border-radius: 0px 0px 20px 20px;" v-show="expanded1">
                <q-separator />
                <q-card-section style="opacity: 0.9; border-radius: 0px 0px 20px 20px;"
                  class="text-subitle2 titleFont text-white bg-black">
                  <div v-if="pt" class="flex flex-center">
                    <span clas="text-h5">"</span> Streamer Brasileiro, Nº1 em CryptoGames , atualmente tem parcerias no
                    ramo de casino, e direciona suas
                    lives para tais assuntos. <br>
                    <span style="text-decoration: underline;" class="text-italic"> Criador do AlphaC </span> <span
                      clas="text-h5"> "</span>
                  </div>
                  <div v-if="!pt" class="flex flex-center">
                    <span clas="text-h5">"</span> Brazilian Streamer, Number 1 in crypto on SA and partner of some
                    online casino
                    <br>
                    <span style="text-decoration: underline;" class="text-italic">Alpha C creator</span> <span
                      clas="text-h5"> "</span>
                  </div>
                </q-card-section>
              </div>
            </q-slide-transition>
          </q-card>
        </div>
        <div class="col bg-dark flex flex-center">
          <q-card style="top: -7em; border-radius: 25px;" class="my-card-xl q-mb-xl bg-transparent" flat bordered>
            <div style="border-radius: 25px;" class="flex items-center justify-center">
              <q-img style="border-radius: 25px 25px 0px 0px;" class="backgroundImage1-xl" />
            </div>

            <q-card-section style="opacity: 0.9" class="bg-black">
              <div class="text-overline textKdam text-white">co-founder.</div>
              <div class="text-h5 text-white textKdam q-mt-sm q-mb-xs">Fernando</div>
              <div class="text-caption textKdam bg-black text-grey">
                <span v-if="pt">Streamer/Empresário</span> <span v-if="!pt">Streamer/Businessman</span> <br> <br> <span
                  class="q-gutter-x-xs text-center">
                  <q-icon size="xs" color="green" name="fa-solid fa-flag" /> <span
                    class="text-bold text-subtitle2">BR</span>
                </span>
              </div>
            </q-card-section>

            <q-card-actions style="opacity: 0.8; border-radius: 0px 0px 4px 4px;" class="bg-black">
              <q-btn class="textKdam text-caption" icon-right="fa-brands fa-twitter" flat color="dark"
                text-color="white" />

              <q-space />
              <q-btn v-if="pt" class="text-bold text-italic text-white" :label="expanded1 ? 'OK' : 'Sobre'"
                color="white" rounded flat dense :icon="expanded1 ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded1 = !expanded1" />
              <q-btn v-if="!pt" class="text-bold text-italic text-white" :label="expanded1 ? 'OK' : 'About'"
                color="white" rounded flat dense :icon="expanded1 ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded1 = !expanded1" />
            </q-card-actions>

            <q-slide-transition style="border-radius: 0px 0px 30px 30px;">
              <div style="border-radius: 0px 0px 20px 20px;" v-show="expanded1">
                <q-separator />
                <q-card-section style="opacity: 0.9; border-radius: 0px 0px 20px 20px;"
                  class="text-subitle2 titleFont text-white bg-black">
                  <div v-if="pt" class="flex flex-center">
                    <span clas="text-h5">"</span> Streamer Brasileiro, Nº1 em CryptoGames , atualmente tem parcerias no
                    ramo de casino, e direciona suas
                    lives para tais assuntos. <br>
                    <span style="text-decoration: underline;" class="text-italic"> Criador do AlphaC </span> <span
                      clas="text-h5"> "</span>
                  </div>
                  <div v-if="!pt" class="flex flex-center">
                    <span clas="text-h5">"</span> Brazilian Streamer, Number 1 in crypto on SA and partner of some
                    online casino
                    <br>
                    <span style="text-decoration: underline;" class="text-italic">Alpha C creator</span> <span
                      clas="text-h5"> "</span>
                  </div>
                </q-card-section>
              </div>
            </q-slide-transition>
          </q-card>
        </div>

        </div>
      </div>




  </q-page>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'about-team',
  data() {
    return {
      pageCounter: ref(0),
      pt: true
    }
  },
  setup() {
    return {
      expanded0: ref(false),
      expanded1: ref(false),
      expanded2: ref(false),
      expanded3: ref(false),
      expanded4: ref(false),
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
    }
  }
})
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Spline+Sans+Mono:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,500;1,600;1,700&display=swap');
@import url('https://fonts.googleapis.com/css?family=Titan+One');
@import url('https://fonts.googleapis.com/css2?family=Source+Code+Pro:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Spline+Sans+Mono:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,500;1,600;1,700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Lobster&display=swap');

* {
  padding: 0;
  margin: 0;
}

.my-card-xl {
  width: 25vw;
  height: 33vh;
}

.backgroundImage0-xl {
  width: 40vw;
  height: 42vh;
  background-size: cover;
  transition-duration: 1.3s;
  background-position: 0;
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1024795505173213255/danilobw.jpg");
}

.backgroundImage0-xl:hover {
  width: 40vw;
  height: 42vh;
  background-size: cover;
  transition-duration: 1.3s;
  background-position: 0;
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1024794987663196170/unknown.png");
}

.backgroundImage1-xl {
  width: 40vw;
  height: 42vh;
  background-size: cover;
  transition-duration: 1.3s;
  background-position: 0;
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1024795504908980305/sonecabw.jpg");
}

.backgroundImage1-xl:hover {
  width: 40vw;
  height: 42vh;
  background-size: cover;
  transition-duration: 1.3s;
  background-position: 0;
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1024794938711494666/unknown.png");
}

.backgroundImage2-xl {
  width: 40vw;
  height: 42vh;
  background-size: cover;
  transition-duration: 1.3s;
  background-position: 0;
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1027823649480257536/gynchiiibw.png");
}

.backgroundImage2-xl:hover {
  width: 40vw;
  height: 42vh;
  background-size: cover;
  transition-duration: 1.3s;
  background-position: 0;
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1027823057634594856/unknown.png");
}

.bgg-solana {
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1022733258749915146/Untitled-video-Made-with-Clipchamp.gif");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

.bgg-dark {
  background-color: rgba(51, 49, 56, 0.18);
}

.spilineFont {
  font-family: 'Spline Sans Mono', monospace;
}

.titleFont {
  font-family: 'Spline Sans Mono', monospace;
}

.mainFont {
  font-family: 'Lobster', cursive;
}

.bgg-init {
  background-image: url("https://cdn.suwalls.com/wallpapers/abstract/blue-triangles-44901-2560x1600.jpg");
  background-position: 0;
  background-size: cover;
  background-repeat: no-repeat;
}

.fadeIn {
  transition-duration: 6s;
  animation-duration: 6s;
}

.backInDown {
  transition-duration: 2s;
  animation-duration: 2.2s;
}

.backInUp {
  transition-duration: 2s;
  animation-duration: 2.2s;
}


.blink {
  animation: blink-animation 2s steps(2, start) infinite;
  -webkit-animation: blink-animation 1.2s steps(2, start) infinite;
}


@keyframes blink-animation {
  to {
    visibility: hidden;
  }
}

.solanaImage {
  transition-delay: 6s;
  transform: translatey(0px);
  animation: float 3s ease-in-out infinite;
}

.solanaImage:hover {
  transition-delay: 4s;
  animation: float-hover 1.6s ease-in-out infinite;
}


@keyframes float {


  50% {
    transform: translatey(-40px);
  }


}

@keyframes float-hover {

  50% {
    transform: translatey(-50px);
  }

  100% {
    transform: translatey(0px);
  }
}

.wrap {
  padding: 10% 20%;
  font-family: "Source Code Pro", sans-serif;
}

h2 {
  margin-top: 3em;
  color: #00FFA3;

  &:first-child {
    margin-top: 0;
  }
}

.underlined {
  color: #00FFA3;
  flex: 1;
  font-size: 2.5em;
  line-height: 1.2;
  text-decoration: none;
  background-image: linear-gradient(to right, rgb(133, 75, 75) 0, yellow 100%);
  background-position: 0 1.2em;
  background-size: 0 100%;
  background-repeat: no-repeat;
  transition: background 0.5s;

  &:hover {
    background-size: 100% 100%;
    color: rgb(0, 0, 0);

  }

  &--thin {
    background-image: linear-gradient(to right, black 0, black 100%);
  }

  &--thick {
    background-position: 0 -0.3em;
  }

  &--offset {
    background-position: 0 0.2em;
    //didn't find another solution than mask the underline shape by a box shadow with the same color than the bg
    box-shadow: inset 0 -0.5em 0 0 white;
  }

  &--gradient {
    background-position: 0 -0.1em;
    background-image: linear-gradient(to right, yellow 0, lightgreen 100%);
  }

  &--reverse {
    background-position: 100% -0.1em;
    transition: background 1s; //yep, that's a long link
    background-image: linear-gradient(to right, yellow 0, yellow 100%);
  }
}

.typewriter {
  color: #fff;
  overflow: hidden;
  /* Ensures the content is not revealed until the animation */
  border-right: .11em solid orange;
  /* The typwriter cursor */
  white-space: nowrap;
  /* Keeps the content on a single line */
  margin: 0 auto;
  /* Gives that scrolling effect as the typing happens */
  letter-spacing: .06em;
  /* Adjust as needed */
  animation:
    typing 1.34s steps(30, end),
    blink-caret .5s step-end infinite;
}

/* The typing effect */
@keyframes typing {
  from {
    width: 0
  }

  to {
    width: 100%
  }
}

/* The typewriter cursor effect */
@keyframes blink-caret {

  from,
  to {
    border-color: transparent
  }

  50% {
    border-color: orange
  }
}
</style>
