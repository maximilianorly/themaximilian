<template class="nav-animate">
    <fixed-header>
        <header class="nav-animate__header" ref="header">
            <div class="branding">
                <h1 class="branding__brand-name">the maximilian</h1>
            </div>
            <div v-on:click="this.runAnimation" class="nav-animate__hamburger-container">
                <div :class="{'nav-animate__hamburger-bar--top-animated': this.animate, 'nav-animate__hamburger-bar--top-close': this.close}"
                class="nav-animate__hamburger-bar nav-animate__hamburger-bar--top">
                </div>
                <div :class="{'nav-animate__hamburger-bar--center-animated': this.animate, 'nav-animate__hamburger-bar--center-close': this.close}"
                class="nav-animate__hamburger-bar nav-animate__hamburger-bar--center">
                </div>
                <div :class="{'nav-animate__hamburger-bar--bottom-animated': this.animate, 'nav-animate__hamburger-bar--bottom-close': this.close}"
                class="nav-animate__hamburger-bar nav-animate__hamburger-bar--bottom">
                </div>
            </div>
        </header>
    </fixed-header>
</template>

<script>
import FixedHeader from 'vue-fixed-header';

    export default {
        name: 'HeaderBar',
        data: function() {
            return {
                animate: false,
                close: false
            }
        },
        components: {
            FixedHeader
        },
        methods: {
            runAnimation() {

                if (!this.animate) {
                    this.animate = !this.animate;
                    this.close = false;
                } else {
                    this.animate = !this.animate;
                    this.close = !this.close
                }
                console.log(`animate: ${this.animate}`)
                console.log(`close: ${this.close}`)
            }
        }
    }
</script>

<style lang="scss">
  @import "../styles/_nav-animate.scss";
  @import "../styles/_branding.scss";
  body {
      margin: 0;
  }
</style>