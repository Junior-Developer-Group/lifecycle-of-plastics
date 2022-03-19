<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <Header></Header>
    <LevelOne></LevelOne>
    <LevelFive></LevelFive>
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import LevelOne from "../components/levels/LevelOne.vue";
import LevelFive from "../components/levels/LevelFive.vue";

export default {
  name: 'Home',

  props: [],

  components: {
    Header,
    LevelOne,
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
