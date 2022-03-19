<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <Header></Header>
    <LevelOne></LevelOne>
	<LevelThree/>
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import LevelOne from "../components/levels/LevelOne.vue";
import LevelThree from "../components/levels/LevelThree.vue";

export default {
  name: 'Home',

  props: [],

  components: {
    Header,
    LevelOne,
	LevelThree
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
