<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <Header></Header>
    <LevelOne></LevelOne>
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import LevelOne from "../components/levels/LevelOne.vue";

export default {
  name: 'Home',

  props: [],

  components: {
    Header,
    LevelOne
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
