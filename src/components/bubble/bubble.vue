<template>
    <div id="bubble-box">
        <canvas id="bubble"></canvas>
        <!-- asdasdhj -->
    </div>
</template>

<script>
import { start, end } from './bubble_move';

export default {
    data() {
        return {

        }
    },
    methods: {

    },
    mounted() {
        let canvas = document.getElementById('bubble');
        let parent = document.getElementById('bubble-box');
        start(canvas, parent);
    },
    beforeDestroy() {
        end();
    }
}
</script>

<style >
#bubble-box{
    width: 100%;
    height: 100%;

}
</style>

