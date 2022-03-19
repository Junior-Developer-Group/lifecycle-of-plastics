<template>
    <header>
        <h1> {{ title }}  </h1>
        <section>

            <aside>
                <img :src="image.source" :alt="image.alt_text">
            </aside>

            <aside>
                <p> {{ paragraph }} </p>
            </aside>

        </section>

    </header>
</template>

<script>
    export default {
        name: 'Header',
        data() {
            return {
                title: 'LIFECYCLE OF PLASTICS',
                paragraph: 'Built by Junior Developer Group',
                image: {
                    source: 'https://junior-developer-group.com/assets/images/website-images/logo-with-background.png',
                    alt_text: 'Junior Developer Group'
                }
            }
        }
    }
</script>

<style lang="scss" scoped>
    header {
        background: #CBCBD5;
        min-height: 500px;
        // position: relative;
        // top: -35px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;

        h1 {
            font-style: normal;
            font-weight: 700;
            font-size: 48px;
            line-height: 56px;
            text-align: center;

            color: #55576B;

            text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
        }
    }

    section {
        display: flex;
        justify-content: center;
        align-items: center;

        aside {

            img {
                height: 100px;
                width: 100px;
            }

            p {
                font-style: normal;
                font-weight: 700;
                font-size: 36px;
                line-height: 42px;
                text-align: center;

                color: #55576B;
                margin-left: 20px;
            }
        }
    }


    @media (max-width: 780px) {
        h1 {
            font-size: 35px;
        }

        section aside p {
            font-size: 20px;
        }
    }
</style>