<template>
    <section>
        <aside>
            <img src="../../assets/plastic-bottle.png" :alt="item.alt_text">
        </aside>
        <aside>
            <p v-if="shouldShowText"> The {{ item.name }} will disolve in {{ item.time_to_disolve }} </p>
            <button @click="showMeTheText" :class="{'active' : shouldShowText}"> {{ item.button_text }} </button>
        </aside>
    </section>
</template>

<script>
export default {
    name: 'LevelFive',

    data() {
        return {
            item: {
                name: 'Plastic Bottle',
                time_to_disolve: '450 years',
                alt_text: 'Plastic Bottle',
                button_text: 'Reveal Time to Disolve'
            },
            
            shouldShowText: false,
        }
    },
    methods: {
        showMeTheText() {
            this.shouldShowText = !this.shouldShowText;
            if(this.shouldShowText == true ){
                this.item.button_text = 'Hide time to disolve'
            }
            else {
                this.item.button_text = 'Reveal time to disolve'
            }
        }
    }
}
</script>

<style lang="scss" scoped>
    section {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 500px;
        background: #2A869D;
    }
    aside {
            img {
                height: 100px;
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
</style>