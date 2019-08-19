<template>
  <v-content fill-height>
    <drawer/>
    <navbar/>
    <home-header/>
    <steps />
    <footer />
  </v-content>
</template>

<script>
  export default {
    components: {
      Navbar: () => import('@/components/Navbar'),
      Drawer: () => import('@/components/Drawer'),
      HomeHeader: () => import('@/components/HomeHeader'),
      Steps: () => import('@/components/Steps'),
      Footer: () => import('@/components/Footer')
    }
  }
</script>

<style lang="sass" scoped>
  main
      background: #EBEBEB url('../../public/imgs/home-bg.jpg') center/cover no-repeat 
</style>

