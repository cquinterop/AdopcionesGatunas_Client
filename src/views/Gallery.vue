<template>
  <v-content>
    <drawer />
    <navbar />
    <v-container grid-list-xl>
    <v-card flat>
      <v-bottom-nav
        :active.sync="current_gender"
        :value="true"
        @update:active="getData()"
        shift
      >
        <v-btn
          color="teal"
          value=" "
          flat
        >
          <span>Todos</span>
          <v-icon>mdi-gender-male-female</v-icon>
        </v-btn>

        <v-btn
          color="teal"
          flat
          value="Macho"
        >
          <span>Machos</span>
          <v-icon>mdi-gender-male</v-icon>
        </v-btn>

        <v-btn
          color="teal"
          flat
          value="Hembra"
        >
          <span>Hembras</span>
          <v-icon>mdi-gender-female</v-icon>
        </v-btn>
      </v-bottom-nav>
    </v-card>
  </v-container>
     <v-container grid-list-xl>
        <v-layout wrap>
          <v-layout  
            v-if="cats.length === 0" 
            align-center 
            justify-center 
            fill-height>
             <v-progress-circular
              :size="70"
              :width="7"
              indeterminate
              ></v-progress-circular>
            </v-layout>
            <card
              v-else
              v-for="cat in cats" 
              :key="cat.id" 
              :picture="cat.image"
              :gender="cat.gender"
              :age="cat.age"
              :isAdoptable="cat.isAdoptable"
              />
        </v-layout>
    </v-container>
  </v-content>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      cats: [],
      current_gender: ""
    };
  },
  methods: {
    getData() {
      this.cats = []
      axios
        .get(`http://localhost:3000/api/v1/get/cats?gender=${this.current_gender}`)
        .then(({ data: cats }) => (this.cats = cats))
        .catch(err => console.log(err));
    }
  },
  mounted() {
    this.getData();
  },
  components: {
    Navbar: () => import("@/components/Navbar"),
    Drawer: () => import("@/components/Drawer"),
    Card: () => import("@/components/Card")
  }
};
</script>
