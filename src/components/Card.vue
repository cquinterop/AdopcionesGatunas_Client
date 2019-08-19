<template>
<v-flex xs6 md4>
    <v-card
    :elevation="isAdoptable ? 5 : 0"
    flat
    >
        <v-img 
        :src="picture" aspect-ratio="1"
        :class="{ disabled: !isAdoptable}"
        >
        </v-img>
        <v-card-title primary-title>
           <h2 class="headline" v-if="isAdoptable">Disponible</h2>
           <h2 class="headline" v-else>No Disponible</h2>
        </v-card-title>
        <v-card-text>
            <span>Sexo: {{ gender }}</span><br>
            <span>Edad: {{ age }} meses</span>
        </v-card-text>
        <v-card-actions>
            <v-btn color="teal"
            :disabled="!isAdoptable" 
            flat>
            ADOPTAR
        </v-btn>
        </v-card-actions>
    </v-card>
</v-flex>
</template>

<script>
export default {
  props: ["picture", "gender", "age", "isAdoptable"]
}
</script>

<style lang="sass" scoped>
.disabled
    filter: grayscale(80%)
    opacity: 0.7
</style>
