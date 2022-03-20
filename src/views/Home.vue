<template>
  <div class="home">
    <!-- LIST ANY COMPONENTS YOU'D LIKE TO SEE ON THE SCREEN HERE -->
    <Header></Header>
    <LevelOne></LevelOne>
    <LevelTwo></LevelTwo>
    <LevelThree></LevelThree>
    <LevelFour></LevelFour>
    <LevelFive></LevelFive>
  </div>
</template>

<script>
/// import the component from the folder we created it in
import Header from "../components/Header.vue";
import LevelOne from "../components/levels/LevelOne.vue";
import LevelTwo from "../components/levels/LevelTwo.vue";
import LevelThree from "../components/levels/LevelThree.vue";
import LevelFour from "../components/levels/LevelFour.vue";
import LevelFive from "../components/levels/LevelFive.vue";

export default {

  // set a name for the current component 
  // keep it the same as the name of the file e.g Home.vue
  name: 'Home',

  // props are used to pass data from one component to the other
  props: [],

  // register components inside of the component block
  components: {
    Header,
    LevelOne,
    LevelTwo,
    LevelThree,
    LevelFour,
    LevelFive
  },

  // data are like variables in vanilla JS
  // we can set static ones and display them with string interpolation e.g {{ text }}
  // we can set them as empty values and edit them later
  // we can set them as null, undefined or anything else we want
  data() {
    return {

    }
  },

  // created block is used to run functions when our component is created
   // we can refer to our functions inside of it e.g this.myFunctionName()
  created() {

  },

  // mounted block is used to run functions when our component is mounted/loaded
  // we can refer to our functions inside of it e.g this.myFunctionName()
  mounted(){

  },

  // methods block is where we write all our functions/methods we'd like to use
  // we can refer to them inside of the mounted, created, beforeDestroy or any other lifecycle hook 
  // we can trigger them via button clicks 
  methods: {

  },

  // computed block runs when our component is created/mounted
  // we can use computed values inside of string interpolation just the same as we would use things from our data block
  // it always has to return a value, if you don't use 'return' keyword you'll see an error
  computed: {

  },

  // beforeDestroy block runs just before we exit the page
  // we can refer to our functions inside of it e.g this.myFunctionName()
  beforeDestroy() {

  }
}
</script>
