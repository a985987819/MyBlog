<template>
    <div class="Myinput">
        <div class="text">
            <slot></slot>
        </div>
        <label>
            <input>
        </label>
    </div>
</template>

<script lang="ts">
    import Vue from 'vue';
    import {Component} from 'vue-property-decorator';

    @Component
    export default class Input extends Vue {

    }
</script>

<style lang="scss">

    .Myinput {
        /*border: 1px solid black;*/
        width: 450px;
        display: flex;
        justify-content: space-between;
    }

    .text {
        /*border: 1px solid black;*/
        font-size: 18px;
        min-width: 100px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-basis: 100px;
    }

    input {
        width: 250px;
        /*border: 1px solid red;*/
        height: 30px;
        border: none;
        flex: 1;
    }
</style>