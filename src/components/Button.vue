<template>
    <div>
        <button class="button" @click="$emit('click',$event)">
            <slot/>
        </button>
    </div>
</template>

<script lang="ts">
    import Vue from 'vue';
    import {Component} from 'vue-property-decorator';

    @Component
    export default class Button extends Vue {
    }
</script>

<style lang="scss" scoped>
    .button {
        background: #00a9ea;
        color: white;
        border-radius: 4px;
        border: none;
        height: 30px;
        width: auto;
        padding: 0 16px;

        &-wrapper {
            text-align: center;
            padding: 16px;
            margin-top: 44-16px;
        }
    }
</style>