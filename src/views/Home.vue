<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <Header></Header>
    <LevelOne></LevelOne>
	  <LevelThree/>
    <LevelFour></LevelFour>
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import LevelOne from "../components/levels/LevelOne.vue";
import LevelThree from "../components/levels/LevelThree.vue";
import LevelFour from "../components/levels/LevelFour.vue"

export default {
  name: 'Home',

  props: [],

  components: {
    Header,
    LevelOne,
	  LevelThree,
    LevelFour
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
