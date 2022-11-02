<template>
  <q-page class="flex bg-dark flex-center">
    <div style="height: 95vh; background: radial-gradient(circle, #0057FF 5%, #0057FF 1%)">
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
    </div>

    <div style="margin-top: -70vh;" class="flex flex-center text-center text-h4 text-bold titleFont text-white q-ma-md q-pa-md">
      <q-intersection transition="slide-down" transition-duration="800" once class="example-item">
      <span class="mainFont">Road-<span class="text-blue-2">map</span>.</span>
    </q-intersection>
    </div>

    <q-intersection transition="slide-up" transition-duration="1200" once class="example-item">
    <div style="height: 84vh; width: 100vw; margin-top: -82vh;" class="roadmap-grid row q-col-gutter-lg flex flex-center bg-dark">
      <q-btn v-if="!roadmap1" @click="roadmap1 = true" v-on:mouseleave="roadmap1 = false" style="border-radius: 10px 0 0 0" icon="swap_vertical_circle" size="xl" class="roadmap-card text-gray-8 bgg-button-1 q-mx-xs ">
      </q-btn>
      <q-btn v-if="roadmap1" @click="roadmap1 = false"  style="border-radius: 10px 0 0 0" icon="swap_vertical_circle" size="xl" class="roadmap-card text-gray-8 bg-white q-mx-xs ">

      </q-btn>

      <q-btn v-if="!roadmap2" @click="roadmap2 = true" v-on:mouseleave="roadmap2 = false" style="border-radius: 0 10px 0 0" icon="swap_vertical_circle" size="xl" class="roadmap-card text-gray-8 bgg-button-2 q-mx-xs ">
      </q-btn>
      <q-btn v-if="roadmap2" @click="roadmap2 = false"  style="border-radius: 0 10px 0 0" icon="swap_vertical_circle" size="xl" class="roadmap-card text-gray-8 bg-white q-mx-xs ">
      </q-btn>


      <q-btn v-if="!roadmap3" @click="roadmap3 = true" v-on:mouseleave="roadmap3 = false" style="border-radius: 0 0 0 10px" icon="swap_vertical_circle" size="xl" class="roadmap-card text-gray-8 bgg-button-3 q-mx-xs ">
      </q-btn>
      <q-btn v-if="roadmap3" @click="roadmap3 = false"  style="border-radius: 0 0 0 10px" icon="swap_vertical_circle" size="xl" class="roadmap-card text-gray-8 bg-white q-mx-xs ">
      </q-btn>

      <q-btn v-if="!roadmap4" @click="roadmap4 = true" v-on:mouseleave="roadmap4 = false" style="border-radius: 0 0 10px 0" icon="swap_vertical_circle" size="xl" class="roadmap-card text-gray-8 bgg-button-4 q-mx-xs ">
      </q-btn>
      <q-btn v-if="roadmap4" @click="roadmap4 = false"  style="border-radius: 0 0 10px 0" icon="swap_vertical_circle" size="xl" class="roadmap-card text-gray-8 bg-white q-mx-xs ">
      </q-btn>
    </div>
    </q-intersection>




  </q-page>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'about-project',
  data() {
    return {
      pageCounter: ref(0),
      pt: true,
      roadmap1: false,
      roadmap2: false,
      roadmap3: false,
      roadmap4: false,
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

.bgg-button-1 {
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1032959877863198720/col-1.png");
  background-size: cover;
  background-position: center;
  opacity: 0.89;
}

.bgg-button-1:hover {
  background-image: url("https://discussions.apple.com/content/attachment/906013040");
  transition-duration: 0.4s;
  background-size: cover;
  background-position: center;
}

.bgg-button-2 {
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1032959878991450162/col-2.png");
  background-size: cover;
  background-position: center;
  opacity: 0.89;
}

.bgg-button-2:hover {
  background-image: url("https://discussions.apple.com/content/attachment/906013040");
  transition-duration: 0.4s;
  background-size: cover;
  background-position: center;
}

.bgg-button-3 {
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1032960225650688010/col-3.png");
  background-size: cover;
  background-position: center;
  opacity: 0.89;
}

.bgg-button-3:hover {
  background-image: url("https://discussions.apple.com/content/attachment/906013040");
  transition-duration: 0.4s;
  background-size: cover;
  background-position: center;
}

.bgg-button-4 {
  background-image: url("https://cdn.discordapp.com/attachments/459557016042471454/1032962742191149066/unknown.png");
  background-size: cover;
  background-position: center;
  opacity: 0.89;
}

.bgg-button-4:hover {
  background-image: url("https://discussions.apple.com/content/attachment/906013040");
  transition-duration: 0.4s;
  background-size: cover;
  background-position: center;
}

.roadmap-card {
  width: 42vw;
  height: 41vh;
}

.roadmap-grid {
  width: 25vw;
  height: 25vh;
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
