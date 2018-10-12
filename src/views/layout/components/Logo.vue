<template>
  <div class="logo">
    <transition name="slide-fade">
      <p v-if="isCollapse">Vue Admin</p>
      <p v-else>VA</p>
    </transition>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
  name: 'Logo',
  computed: {
    ...mapGetters([
      'sidebar'
    ]),
    isCollapse() {
      return this.sidebar.opened
    }
  }
}
</script>

<style lang="scss" scoped>
.logo {
  height: 50px;
  width: 100%;
  background-color: white;
  p {
    height: 50px;
    width: 100%;
    font-size: 20px;
    margin: 0;
    line-height: 50px;
    text-align: center;
  }
}
</style>
