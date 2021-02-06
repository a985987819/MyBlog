<template>
    <div>
        <div class="cover">

        </div>
        <div class="container">
            <div class="dialog">
                <div class="head">
                    <span>登</span>
                    &nbsp;
                    <span>录</span>
                </div>
                <div class="content">
                    <Myinput>UserAccount</Myinput>
                    <Myinput>Password</Myinput>
                    <Button class="login">登录</Button>
                </div>
                <div class="others">
                    <a href="">
                        <div class="forget">忘记密码</div>
                    </a>

                    <a href="">
                        <div class="logon">现在注册</div>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
    import Vue from 'vue';
    import {Component} from 'vue-property-decorator';
    import Myinput from '@/components/Myinput.vue';
    import Button from '@/components/Button.vue';

    @Component({
        components: {Myinput, Button}
    })
    export default class Login extends Vue {

    }
</script>

<style lang="scss" scoped>
    a {
        color: #7dc9b6;
        text-decoration: none;
    }

    .head {
        font-size: 40px;
        display: flex;
        justify-content: space-between;
        width: 150px;
        margin: 20px auto 0;
    }

    .cover {
        background-image: url('../assets/img/WheatherChild.jpg');
        z-index: 0;
        filter:blur(5px);
        width: 100vw;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        background-repeat:no-repeat;
        background-size:cover;
    }
    .container{
        border: 1px solid red;
        height: 100vh;
        width: 100vw;
        position: relative;
        top: 0;
        left: 0;
    }

    .dialog {
        background: #2d3845;
        width: 600px;
        height: 400px;
        box-shadow: 0 20px 15px #1f262f;
        position: absolute;
        text-align: center;
        color: white;
        z-index: 10;
    }

    .content {
        /*border: 1px solid red;*/
        width: 450px;
        height: 200px;
        text-align: center;
        position: relative;
        left: 50%;
        top: 40%;
        transform: translate(-50%, -50%);
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    .others {
        margin: auto 10px 0 auto;
        transform: translateY(350%);
        height: 1.5em;
        display: flex;
        padding: 0 10px;
        width: 170px;
        /*border: 1px solid pink;*/
        justify-content: space-between;
    }

    .login {
        /*border: 1px solid red;*/
    }

</style>