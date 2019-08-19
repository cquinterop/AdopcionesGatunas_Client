<template>
<v-toolbar scroll-off-screen flat app class="transparent">
    <v-toolbar-title class="tertiary--text font-weight-light">
         <v-btn to="/" flat>Logo</v-btn>
    </v-toolbar-title>
    <v-spacer />
    <v-toolbar-items>
        <v-btn to="/about" flat>Nosotros</v-btn>
        <v-btn to="/gallery" flat>Galeria</v-btn>
        <v-btn to="/login" flat>Log In</v-btn>
        <v-btn @click="$store.commit('toggleDrawer')" icon>
            <v-icon>mdi-view-list</v-icon>
        </v-btn>
    </v-toolbar-items>
</v-toolbar>
</template>

<script>
export default {
    data() {
        return {}
    }
}
</script>

<style lang="sass" scoped>
    // a
    //     color: red!important
</style>