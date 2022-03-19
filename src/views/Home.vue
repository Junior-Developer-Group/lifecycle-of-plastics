<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <Header></Header>
    <LevelOne></LevelOne>
    <LevelFour></LevelFour>
    <LevelFive></LevelFive>
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import LevelOne from "../components/levels/LevelOne.vue";
import LevelFour from "../components/levels/LevelFour.vue";
import LevelFive from "../components/levels/LevelFive.vue";

export default {
  name: 'Home',

  props: [],

  components: {
    Header,
    LevelOne,
    LevelFour,
    LevelFive
},
  data() {
    return {

    }
  },
  created() {

  },
  mounted(){

  },
  methods: {

  },
  computed: {

  },
  beforeDestroy() {

  }
}
</script>
