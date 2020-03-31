<template>
    <div class="parallax-body" v-on:scroll="handleScrollTextResize">
        <section class="parallax-body__section parallax-body__parallax parallax-body__bg0">
            <p ref="text" class="parallax-body__first-text">
                I like coffee.
            </p>
        </section>
        <section class="parallax-body__section parallax-body__parallax parallax-body__bg1">
            <CoffeeBeansSVG class="parallax-body__coffee-beans"/>
        </section>
        <section class="parallax-body__section parallax-body__static">
            <div class="parallax-body__image-strip">
                <img class="parallax-body__image-strip--image" src="../assets/coffee/coffee_brew.svg" alt="">
                <img class="parallax-body__image-strip--image" src="../assets/coffee/moka.svg" alt="">
                <img class="parallax-body__image-strip--image" src="../assets/coffee/coffee_filter.svg" alt="">
                <img class="parallax-body__image-strip--image" src="../assets/coffee/coffee_gahwah.svg" alt="">
                <img class="parallax-body__image-strip--image" src="../assets/coffee/coffee_turkish.svg" alt="">
            </div>
        </section>
        <section class="parallax-body__section parallax-body__parallax parallax-body__bg2">
            <div class="parallax-body__image--container">
                <img class="parallax-body__image--content" src="../assets/coffeenbg.png" alt="">
            </div>
        </section>
    </div>
</template>

<script>
import CoffeeBeansSVG from './CoffeeBeansSvg'
    export default {
        name: 'ParallaxBody',
        methods: {
            handleScrollTextResize() {
                console.log('hit')
                if (document.body.scrollTop < (document.documentElement.clientHeight)) {
                    this.$refs['text'].classList.add('parallax-body__text--grow')
                } else {
                    this.$refs['text'].style.fontSize = "90px";
                }
            }
        },
        components: {
            CoffeeBeansSVG
        }
    }
</script>

<style lang="scss" scoped>
@import '../styles/_parallax-body.scss'
</style>