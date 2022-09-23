<template>
  <q-page class="flex bg-dark flex-center">
    <div style="height: 95vh; background: radial-gradient(circle, #0057FF 5%, #0057FF 1%)">
      <q-toolbar class="absolute-top">

        <q-toolbar-title class="titleFont">
          <q-btn href="javascript:location.reload(true)" to="/" size="lg"
            class=" q-pl-xl titleFont text-white text-bold" rounded flat class-flex-flex-center q-ma-sm>
            <q-img
              src="https://cdn.discordapp.com/attachments/459557016042471454/1022390261957021717/299085275_1297684320974924_880665858629312467_n-removebg-preview.png"
              style="width:3vw;">

            </q-img>
          </q-btn>
        </q-toolbar-title>

        <div class="text-dark flex flex-center q-gutter-x-md q-py-md q-pr-xl row">
          <q-btn-group outline>
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
      <div style="width: 100vw;" v-if="pageCounter == 0">
        <div style="width: 100vw; height: 100vh;" class="flex bgg-solana column flex-center ">
          <div style="border-radius: 15px;" class="bgg-dark shadow-8">
            <div style="margin-top: 5vh;" class="col text-end q-ml-md flex flex-center q-pa-lg">
              <div style="font-size: 9vh;" class="mainFont text-center text-bold flex flex-center ">
                <span class="typewriter text-grey-4" v-if="pt"><span style="opacity: 0.78;" class="text-accent"><span
                      style="opacity: 0.78;" class="text-primary">Block</span>chain</span> em doses diárias</span>
                <span class="typewriter text-grey-4" v-if="!pt"><span style="opacity: 0.78;" class="text-accent"><span
                      style="opacity: 0.78;" class="text-primary">Block</span>chain</span> in daily doses</span>

              </div>
            </div>
            <div style="margin-top: 1vh;" class="col text-end q-ml-md flex flex-center q-pa-lg">
              <div style="font-size: 5vh;" class="mainFont text-italic flex flex-center text-grey-4">
                <span data-show-after="1000" class="fadeIn" v-if="pt">você escolha a frequência</span>
                <span class="fadeIn" v-if="!pt">You choose the frequency</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="bg-dark" style="width: 100vw;" v-if="pageCounter == 1">
      <div style="width: 100vw; height: 100vh;" class="flex flex-center full-width full-height row">
        <div style="margin-top: -3vh;" class="col flex flex-center q-pa-lg">
          <transition appear enter-active-class="animated backInDown" leave-active-class="animated backOutDown">
            <div style="font-size: 6vh; text-align: end;" class="titleFont text-bold flex flex-center text-white">
              <span v-if="pt">
                AlphaC não é só uma DAO, mas sim um conceito. Um lugar.
              </span>
              <span v-if="!pt">
                AlphaC isn't just a DAO, but a concept. A place.
              </span>
            </div>
          </transition>
        </div>
        <div class="col flex flex-center q-pa-md">
          <transition appear enter-active-class="animated fadeIn">
            <div style="font-size: 15vh;" class="titleFont solanaImage text-center flex flex-center text-accent">
              <q-img style="width: 22vw; border-radius: 25px;"
                src="https://cdn.discordapp.com/attachments/459557016042471454/1022354189235519488/299085275_1297684320974924_880665858629312467_n.jpg">
              </q-img>
            </div>
          </transition>
        </div>
        <div style="margin-top: 30vh;" class="col flex flex-center q-pa-lg">
          <transition appear enter-active-class="animated backInUp" leave-active-class="animated backOutUp">
            <div style="font-size: 6vh;" class="titleFont text-bold flex flex-center text-white">
              <span v-if="pt">Completo, remodelado, feito pela comunidade, para a comunidade.</span>
              <span v-if="!pt">Complete, rebuilded, made by community, to the community</span>
            </div>
          </transition>
        </div>

      </div>
    </div>
    <div class="bg-dark" style="width: 100vw;" v-if="pageCounter == 2">
      <div style="width: 100vw; height: 100vh;" class="flex flex-center full-width full-height row">
        <div class="wrap q-gutter-y-md bg-dark">
          <a href="#" class="underlined underlined--gradient">Sobre o Time</a>
          <p><a href="#" class="underlined underlined--reverse">Sobre o Projeto</a></p>
        </div>


      </div>
    </div>
    <div v-if="pageCounter != 2" style="width: 100vw; height: 100vh; margin-top: vh; opacity: 0.9;"
      class="flex bg-dark flex-center full-width full-height items-center">
      <div style="width: 100vw;" class="flex flex-center row q-pa-lg">
        <q-btn @click="(pageCounter +++ 1)" style="width: 100vw; height: 5vh;"
          class="titleFont  absolute-bottom flex flex-center row q-gutter-x-sm q-pa-md">
          <span v-if="pt" style="text-decoration: underline;" class=" text-primary spanText col">Continuar</span>
          <span v-if="!pt" style="text-decoration: underline;" class=" text-primary spanText col">Continue</span>
          <q-icon class="text-white" size="xs" name="arrow_right"></q-icon>
        </q-btn>
      </div>

    </div>



  </q-page>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
      pageCounter: ref(0),
      pt: true
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
  box-sizing: border-box;
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
