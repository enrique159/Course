<template>
  <div class="home">
    <draw-menu/>
    <medium-menu/>
    <side-menu/>
  </div>
</template>

<script>
import DrawMenu from '../components/DrawMenu.vue'
import MediumMenu from '../components/MediumMenu.vue'
import SideMenu from '../components/SideMenu.vue'
export default {
  components: { DrawMenu, MediumMenu, SideMenu },
  name: 'Home',
}
</script>

<style lang="scss" scoped>
.home {
  background-color: rgb(255, 255, 255);
  display: flex;
  height: 100vh;
  width: 100vw;
}
</style>
