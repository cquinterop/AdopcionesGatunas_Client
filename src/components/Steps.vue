<template>
    <v-container fill-height grid-list-xl>
    <v-layout row wrap>
            <v-flex xs12 text-xs-center>
                <h1>LOREM IPSUM</h1>
                <p>Dolor tia met concectetur sit amen</p>
            </v-flex>

            <v-flex class="step1" xs12>
                <v-flex xs8 offset-xs4>
                    <p> <b>Praesent iaculis mauris</b> a laoreet tristique. Duis est erat,
                        lobortis a feugiat a, gravida a massa. Donec id ante sed mi
                        hendrerit varius vitae non arcu. Fusce vitae ex id est tristique
                        aliquam sit amet et urna. Vestibulum venenatis ipsum ut odio
                        tempus, eget ultrices ex varius. Mauris ut velit justo. </p>
                </v-flex>
            </v-flex>

        <v-flex class="step2" xs12>
                <v-flex xs8>
                    <p> <b>Praesent iaculis mauris</b> a laoreet tristique. Duis est erat,
                        lobortis a feugiat a, gravida a massa. Donec id ante sed mi
                        hendrerit varius vitae non arcu. Fusce vitae ex id est tristique
                        aliquam sit amet et urna. Vestibulum venenatis ipsum ut odio
                        tempus, eget ultrices ex varius. Mauris ut velit justo. </p>
                </v-flex>
            </v-flex>

            <v-flex class="step3" xs12>
                <v-flex xs8 offset-xs4>
                    <p> <b>Praesent iaculis mauris</b> a laoreet tristique. Duis est erat,
                        lobortis a feugiat a, gravida a massa. Donec id ante sed mi
                        hendrerit varius vitae non arcu. Fusce vitae ex id est tristique
                        aliquam sit amet et urna. Vestibulum venenatis ipsum ut odio
                        tempus, eget ultrices ex varius. Mauris ut velit justo. </p>
                    <v-btn round dark flat to="/gallery">Galeria</v-btn>
                </v-flex>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<style lang="sass" scoped>
    .step1
        background: url('../../public/imgs/step1.png') left/50% no-repeat
    .step2
        background: url('../../public/imgs/step2.png') right/50% no-repeat
    .step3
        background: url('../../public/imgs/step3.png') left/25% no-repeat
</style>
