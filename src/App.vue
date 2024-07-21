<template>
    <div id="app">
      <transition name="slide-bota">
        <div v-if="showFull" class="whole">
          <component :is="'viewPlayer'" />
        </div>
      </transition>
      <div v-if="!showFull" class="body">
        <transition name="slide-fade">
          <div v-if="sideNav" class="sidebarz">
            <component :is="'sidebar'" />
          </div>
        </transition>
        <div class="sidebar">
          <component :is="'sidebar'" />
        </div>
        <div class="header">
          <component :is="'headerNav'" />
        </div>
        <div class="main-content">
          <div class="content" @click="$store.commit('setSideNavFalse')">
            <router-view />
          </div>
          
        </div>
        <div class="footer">
            <component :is="'footerSection'" />
          </div>
        <transition name="slide-bota">
          <div class="player" v-if="current">
            <component :is="'player'" />
          </div>
        </transition>
      </div>
    </div>
  </template>
  
<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'
import player from './components/player.vue'
import headerNav from './components/header.vue'
import footerSection from './components/footer.vue'
import sidebar from './components/sidebar.vue'
import viewPlayer from './views/view.vue'

@Component({
    components: {
        player,
        headerNav,
        sidebar,
        viewPlayer,
        footerSection
    }
})
export default class App extends Vue {
    get sideNav() {
        return this.$store.getters['getSideNav']
    }

    get current() {
        return this.$store.getters['getCurrent']
    }

    get showFull() {
        return this.$store.getters['getShowFull']
    }
}
</script>

<style lang="scss">
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.body {
  display: flex;
  flex-direction: column;
  flex: 1;
}

.main-content {
  display: flex;
  flex-direction: column;
  flex: 1;
  padding-bottom: 60px; /* Height of the footer */
}

.header {
  padding: 10px;
  background: var(--white);
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 1500;
  box-shadow: 0px 3px 6px #00000021;
}

.content {
  padding-top: 60px; /* Ensure content starts below the fixed header */
  box-sizing: border-box;
  width: 100%;
  background: var(--white-body);
  flex: 1;
}

.footer {
  background: var(--white);
  width: 100%;
  text-align: center;
  padding: 10px;
  position: relative;
  bottom: 0;
}

.player {
  padding: 0 10px;
  box-shadow: 0 3px 20px #2b2424;
  background: var(--white);
  position: fixed;
  width: 100%;
  z-index: 2000;
  bottom: 0;
  margin: 0 auto;
}

.sidebar,
.sidebarz {
  background: var(--white);
  padding: 10px;
  position: fixed;
  left: 0;
  top: 0;
  overflow-y: hidden;
  height: 100%;
  width: 230px;
  box-shadow: 2px 2px 10px rgba(26, 19, 19, 0.164);
}

.sidebar {
  z-index: 1600;
}

.sidebarz {
  z-index: 1400;
}

.slide-fade-enter-active {
  transition: all 0.3s ease-in-out;
}

.slide-fade-leave-active {
  transition: all 0.1s ease-in-out;
}

.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateX(-100px);
}

.slide-bota-enter-active {
  transition: all 0.3s ease-in-out;
}

.slide-bota-leave-active {
  transition: all 0.1s ease-in-out;
}

.slide-bota-enter,
.slide-bota-leave-to {
  transform: translateY(100px);
}

@media (max-width: 576px) {
  #app {
    width: 80%;
  }
}

@media (max-width: 800px) {
  .sidebar {
    display: none;
  }

  .header {
    grid-column: 1/4;
  }

  .content {
    grid-column: 1/4;
    margin-left: 0; /* Reset margin for smaller screens */
  }
}

</style>
