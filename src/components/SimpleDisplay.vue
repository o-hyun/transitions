<template>
    <div class="mx-5 border border-dark p-2">
        <h3 class="bg-warning text-white text-center p-2">Display</h3>

        <transition enter-to-class="fadeIn" leave-to-class="fadeOut" mode="out-in">
            <div v-if="show" class="animated h4 bg-info text-center p-2" key="hello">Hello, Adam</div>
            <div v-else class="animated h4 bg-success text-center p-2" key="goodbye">Goodbye, Adam</div>
        </transition>

        <div class="text-center">
            <button v-on:click="toggle" class="btn btn-primary">Toggle Visibility</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: "SimpleDisplay",
        data() {
            return {
                show: true
            }
        },
        methods: {
            toggle() {
                this.show = !this.show;
            }
        }
    }
</script>

<style>
    .v-leave-active {
        opacity: 0;
        font-size: 0em;
        transition: all 250ms;
    }
    .v-enter {
        opacity: 0;
        font-size: 0em;
    }
    .v-enter-to {
        opcity: 1;
        font-size: x-large;
        transition: all 250ms;
    }
</style>
