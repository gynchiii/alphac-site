<template>
  <q-page class="flex bg-dark flex-center">
    <div class="flex flex-center full-width full-height"
    style="max-height: 100vh; background: radial-gradient(circle, #0057FF 5%, #0057FF 1%)">
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
          <q-btn-group class="q-gutter-x-sm" outline>
            <div class="flex q-ma-xs q-gutter-x-none">
              <q-btn @click="pageCounter = 4" color="dark" dense style="opacity: 0.8;"
                class="titleFont bg-transparent text-dark text-bold" icon="menu" />
            </div>
            <div style="border-radius: 5px; background-color: rgb(255, 255, 255, 0.88);" class="flex shadow-4 q-ma-xs q-gutter-x-none">
              <q-btn @click="pt = false" color="dark" flat style="opacity: 0.8;"
                class="titleFont   text-dark text-bold" v-if="pt" label="EN" />
              <q-btn @click="pt = true" color="dark" flat style="opacity: 0.8;"
                class="titleFont  text-dark text-bold" v-if="!pt" label="PT" />
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
                <span class="typewriter text-grey-4" v-if="(pt) && (!mintButton)"> Não se perca mais na
                  <span style="opacity: 0.78;" class="text-accent">
                    <span style="opacity: 0.78;" class="text-primary">
                      Block
                    </span>
                    chain
                  </span>
                </span>

                <span class="typewriter text-grey-4" v-if="(pt) && (mintButton)"> Vem <span
                    class="text-accent">mintar</span> com a gente </span>

                <span class="typewriter text-grey-4" v-if="!pt">
                  <span style="opacity: 0.78;" class="text-accent">
                    <span style="opacity: 0.78;" class="text-primary">
                      Block
                    </span>
                    chain
                  </span>
                  in daily doses
                </span>
              </div>
            </div>
            <div style="margin-top: 1vh;" class="col text-end q-ml-md flex flex-center q-pa-lg">
              <div style="font-size: 5vh;" class="mainFont text-italic flex flex-center text-grey-4">
                <span data-show-after="1000" class="fadeIn" v-if="(pt) && (!mintButton)">Não Navegue mais
                  sozinho!</span>
                <span data-show-after="10000" class=" type2title text-bold" v-if="(pt) && (mintButton)">O que ta
                  esperando? Bora!</span>
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
          <transition appear enter-active-class="animated backInDown">
            <div v-if="slideCounter === 0" style="font-size: 6vh; text-align: end;" class="titleFont text-bold flex flex-center text-white">
              <span v-if="pt">
                AlphaC não é só um grupo, mas sim um conceito.
              </span>
              <span v-if="!pt">
                <!-- AlphaC isn't just a DAO, but a concept. A place. -->
              </span>
            </div>
          </transition>
        </div>
        <div v-if="slideCounter === 0" class="col flex flex-center q-pa-md">
          <transition appear leave-active-class="animated fadeOut" enter-active-class="animated fadeIn">
            <div  v-if="slideCounter === 0" style="font-size: 15vh;" class="titleFont solanaImage text-center flex flex-center text-accent">
              <q-img style="width: 22vw; border-radius: 25px;"
                src="https://cdn.discordapp.com/attachments/459557016042471454/1022354189235519488/299085275_1297684320974924_880665858629312467_n.jpg">
              </q-img>
            </div>
          </transition>
        </div>
        <div style="margin-top: 30vh;" class="col flex flex-center q-pa-lg">
          <transition appear enter-active-class="animated backInUp">
            <div v-if="(slideCounter != 1)" style="font-size: 5.5vh;" class="titleFont text-bold flex flex-center text-white">
              <span v-if="(pt)">Um clube, uma DAO, uma família. <br> <br> Um lugar.</span>
              <span v-if="!pt">Complete, rebuilded, made by community, to the community</span>
            </div>
          </transition>
          <div v-if="(slideCounter === 2)" style="font-size: 5.5vh; width: 90vw;" class=" text-bold flex flex-center text-white">
              <span class="fadeIn" v-if="(pt)">Oportunidades infinitas <br> te esperam na Web3</span>
              <span v-if="!pt">Complete, rebuilded, made by community, to the community</span>
            </div>
        </div>

      </div>
    </div>
    <div class="bg-dark flex flex-center" style="width: 100vw;" v-if="pageCounter == 2">
      <div style="width: 100vw; height: 100vh;" class="flex flex-center full-width full-height row">
        <div class="wrap q-gutter-y-md bg-dark">
          <transition appear class="transition-11" enter-active-class="animated  backInUp"
            leave-active-class="animated backInDown">
            <p><a @mouseover="aboutTeamBg = true" @mouseleave="aboutTeamBg = false" href="/#/aboutteam" target=""
                to="/aboutteam" class="underlined underlined--reverse">
                <q-tooltip style="width: 14vw; height: 13vh;">
                  <q-img style="width: 100%; height: 100%;"
                    src="https://cdn.discordapp.com/attachments/459557016042471454/1028440057780129792/unknown.png">

                  </q-img>
                </q-tooltip>
                Sobre o Time
              </a></p>
          </transition>
          <transition appear class="transition-22" enter-active-class="animated backInUp"
            leave-active-class="animated backInDown">
            <p><a @mouseover="aboutProjectBg = true" @mouseleave="aboutProjectBg = false" href="/#/aboutproject"
                target="" to="/aboutproject" class="underlined underlined--reverse">
                <q-tooltip style="width: 14vw; height: 13vh;">
                  <q-img style="width: 100%; height: 100%;"
                    src="https://cdn.discordapp.com/attachments/459557016042471454/1029663637981376572/unknown.png">

                  </q-img>
                </q-tooltip>
                Sobre o Projeto
              </a></p>
          </transition>
        </div>


      </div>

    </div>

    <div class="flex flex-center" style="width: 100vw;" v-if="pageCounter == 4">
      <div style="width: 100vw; height: 100vh;" class="flex flex-center full-width full-height row">
        <div class="wrap q-gutter-y-md">
          <transition appear class="transition-1" enter-active-class="animated  backInUp"
            leave-active-class="animated backInDown">
            <p><a @mouseover="aboutTeamBg = true" @mouseleave="aboutTeamBg = false" href="/#/aboutteam" target=""
                to="/aboutteam" class="underlined underlined--reverse">
                <q-tooltip style="width: 14vw; height: 13vh;">
                  <q-img style="width: 100%; height: 100%;"
                    src="https://cdn.discordapp.com/attachments/459557016042471454/1028440057780129792/unknown.png">

                  </q-img>
                </q-tooltip>
                Como Fazer Parte
              </a></p>
          </transition>
          <transition appear class="transition-2" enter-active-class="animated  backInUp"
            leave-active-class="animated backInDown">
            <p><a @mouseover="aboutTeamBg = true" @mouseleave="aboutTeamBg = false" href="/#/aboutteam" target=""
                to="/aboutteam" class="underlined underlined--reverse">
                <q-tooltip style="width: 14vw; height: 13vh;">
                  <q-img style="width: 100%; height: 100%;"
                    src="https://cdn.discordapp.com/attachments/459557016042471454/1028440057780129792/unknown.png">

                  </q-img>
                </q-tooltip>
                Sobre o Time
              </a></p>
          </transition>
          <transition appear class="transition-3" enter-active-class="animated backInUp"
            leave-active-class="animated backInDown">
            <p><a @mouseover="aboutProjectBg = true" @mouseleave="aboutProjectBg = false" href="/#/aboutproject"
                target="" to="/aboutproject" class="underlined underlined--reverse">
                <q-tooltip style="width: 14vw; height: 13vh;">
                  <q-img style="width: 100%; height: 100%;"
                    src="https://cdn.discordapp.com/attachments/459557016042471454/1029663637981376572/unknown.png">

                  </q-img>
                </q-tooltip>
                Sobre o Projeto
              </a></p>
          </transition>
          <transition appear class="transition-4" enter-active-class="animated backInUp"
            leave-active-class="animated backInDown">
            <p><a @mouseover="aboutProjectBg = true" @mouseleave="aboutProjectBg = false" href="/#/aboutproject"
                target="" to="/aboutproject" class="underlined underlined--reverse">
                <q-tooltip style="width: 14vw; height: 13vh;">
                  <q-img style="width: 100%; height: 100%;"
                    src="https://cdn.discordapp.com/attachments/459557016042471454/1029663637981376572/unknown.png">

                  </q-img>
                </q-tooltip>
                Guia Iniciante
              </a></p>
          </transition>
        </div>


      </div>

    </div>


    <div v-if="(pageCounter === 0) && (pageCounter != 2)" style="width: 50vw; margin-top: -18vh;"
      class="flex flex-center items-center justify-center q-pa-lg">
      <q-btn v-on:mouseleave="mintButton = false" v-on:mouseover="mintButton = true" @click="(pageCounter +++ 1)"
        style="width: 15vw; border-radius: 8px; height: 9vh; background: radial-gradient(circle, #8A3BD8 55%, #6CEAFF 165%)"
        class="titleFont  flex flex-center shadow-11 row q-gutter-x-sm q-pa-md">
        <span v-if="pt && !mintButton" style="text-decoration: ;" class=" text-secondary spanText col">Continuar</span>
        <span v-if="pt && mintButton" style="text-decoration: ;" class=" text-secondary spanText col">Mint</span>
        <span v-if="!pt && !mintButton" style="text-decoration: ;" class=" text-secondary spanText col">Continue</span>
        <span v-if="!pt && mintButton" style="text-decoration: ;" class=" text-secondary spanText col">Mint</span>
        <q-icon class="text-white" size="xs" name="arrow_right"></q-icon>
      </q-btn>
    </div>

    <transition appear class="transition-33"  enter-active-class="animated fadeInRight">
      <div v-if="(pageCounter === 1) && (pageCounter != 2)"
        style="width: 50vw; margin-top: -18vh; margin-left: -15vw;" class="flex items-start justify-start q-pa-lg">
        <q-btn v-if="slideCounter === 0" @click="(pageCounter +++ 1)"
          style="width: 12vw; border-radius: 8px; height: 9vh; background: radial-gradient(circle, #5A6AFF 75%, #FFFFFF 165%)"
          class="titleFont  flex flex-center shadow-11 row q-gutter-x-sm q-pa-md">
          <span v-if="pt " style="text-decoration: ;" class=" text-white spanText col">Seguinte</span>
          <span v-if="!pt " style="text-decoration: ;" class=" text-white spanText col">Seguinte</span>
          <span v-if="!pt" style="text-decoration: ;" class=" text-white spanText col">Mint</span>
          <q-icon class="text-white" size="xs" name="arrow_right"></q-icon>
        </q-btn>
      </div>
    </transition>




  </q-page>
</template>

<script>
import { defineComponent, ref } from 'vue'


export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
      pageCounter: ref(0),
      slideCounter: ref(0),
      pageCounter2: ref(0),
      pt: true,
      mintButton: false
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
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1030317230556201050/solanabgg2.gif");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

.bgg-solana2 {
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1029628478380851281/bgwhib.gif");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

.transition-11 {
  animation-delay: 1s;
  transition-duration: 1;
}


.transition-1 {
  animation-delay: 1.6s;
  transition-duration: 1.6;
}

.transition-2 {
  animation-delay: 1s;
  transition-duration: 1;
}

.transition-3 {
  animation-delay: 0.7s;
  transition-duration: 0.7;
}


.animationMint {
  transition-delay: 1s;
  animation-delay: 1s;
  animation-duration: 2s;
}


.bgg-dark {
  background-color: rgba(51, 49, 56, 0.65);
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
  text-align: center;;
  /* Ensures the content is not revealed until the animation */
  border-right: .11em solid rgb(125, 64, 153, 0.5);
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

.typewriter-2 {
  color: #fff;
  overflow: hidden;
  text-align: center;;
  /* Ensures the content is not revealed until the animation */
  /* The typwriter cursor */
  white-space: nowrap;
  /* Keeps the content on a single line */
  margin: 0 auto;
  /* Gives that scrolling effect as the typing happens */
  letter-spacing: .06em;
  /* Adjust as needed */
  animation:
    typing 1.34s steps(30, end),
}

.typewriter-3 {
  color: #fff;
  overflow: hidden;
  text-align: end;;
  /* Ensures the content is not revealed until the animation */
  /* The typwriter cursor */
  white-space: nowrap;
  /* Keeps the content on a single line */
  margin: 0 auto;
  /* Gives that scrolling effect as the typing happens */
  letter-spacing: .06em;
  /* Adjust as needed */
  animation:
    typing 1.34s steps(30, end),
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
    border-color: rgb(151, 80, 202, 0.4)
  }
}
</style>
