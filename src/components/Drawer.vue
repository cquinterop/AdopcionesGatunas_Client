<template>
<div>
    <v-navigation-drawer
        app
        persistent
        right
        width="260"
        disable-resize-watcher
        mobile-break-point="991"
        v-model="$store.state.drawer"
        class="blue-grey darken-4">
        <v-list-tile avatar>
          <v-list-tile-avatar>
            <v-img
              src="https://via.placeholder.com/150x70"/>
          </v-list-tile-avatar>
          <v-list-tile-title class="title">
            Menu
          </v-list-tile-title>
        </v-list-tile>
        <v-divider/>
    </v-navigation-drawer>
</div>
</template>

<script>
export default {
    data() {
        return {
        }
    }
}
</script>

<style lang="sass">

</style>
