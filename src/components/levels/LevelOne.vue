<template>
    <section>
        <aside>
            <img src="../../assets/plastic-bag.png" :alt="item.alt_text">
        </aside>

        <aside>
            <p v-if="shouldShowText"> 
                The {{ item.name}} will disolve in {{ item.time_to_disolve }}
            </p>
            <button @click="showMeTheText" :class="{'active' : shouldShowText}"> {{ item.button_text }} </button>
        </aside>
    </section>
</template>

<script>
export default {
    name: 'LevelOne',

    data() {
        return {
            item: {
                name: 'Plastic Bag',
                time_to_disolve: '20 years',
                alt_text: 'plastic bag',
                button_text: 'Reveal time to disolve'
            },
            shouldShowText: false,
        }
    },
    methods: {
        showMeTheText() {
            this.shouldShowText = !this.shouldShowText;

            if (this.shouldShowText == true) {
                this.item.button_text = 'Hide button text'
            } else {
                this.item.button_text = 'Reveal time to disolve'
            }
        }
    }
}
</script>

<style lang="scss" scoped>
    section {
        height: 500px;
        background: #40B6D3;

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