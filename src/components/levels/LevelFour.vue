<template>
  <section>
    <aside>
      <img src="../../assets/six-pack-plastic-ring.png" :alt="item.alt_text" />
    </aside>

    <aside>
      <p v-if="showText">
        The {{ item.name }} will dissolve in {{ item.time_to_dissolve }}
      </p>

      <button @click="toggleText" :class="{ active: showText }">
        {{ item.button_text }}
      </button>
    </aside>
  </section>
</template>

<script>
export default {
  name: "LevelFour",

  data() {
    return {
      item: {
        name: "Six-pack Plastic Ring",
        time_to_dissolve: "400 years",
        alt_text: "six-pack plastic ring",
        button_text: "Reveal time to dissolve",
      },
      showText: false,
    };
  },

  methods: {
    toggleText() {
      this.showText = !this.showText;

      if (this.showText == true) {
        this.item.button_text = "Hide button text";
      } else {
        this.item.button_text = "Reveal time to dissolve";
      }
    },
  },
};
</script>

<style lang="scss" scoped>
section {
  height: 500px;
  background-color: #2f93ac;

  display: flex;
  justify-content: center;
  align-items: center;

  aside {
    img {
      height: 80px;
      margin-right: 50px;
    }

    button {
      border: none;
      padding: 5px 10px;
      background: white;
      color: darkslategrey;
    }

    button.active {
      background-color: grey;
      color: white;
    }
  }
}
</style>