<template>
    <view class="main">
        <view class="logo">
            <image style="width: 72px" mode="widthFix" src="/static/logo.png" />
        </view>
        <view class="title">
            <text>Uni-App</text>
        </view>
        <view class="text">
            <input placeholder="用户名" v-model="userId" />
        </view>
        <view class="text">
            <input type="password" placeholder="密码" v-model="pass" />
        </view>
        <view class="button">
            <button @click="login">登录</button>
        </view>
        <view class="button">
            <button @click="reg">注册</button>
        </view>
    </view>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const userId = ref('');
const pass = ref('');

const login = () => {
    console.log(userId.value + '--' + pass.value);
};
const reg = () => {
    uni.navigateTo({
        url: '/pages/reg/index',
    });
};
</script>

<style>
* {
    outline: red 1px solid;
}
.main {
    padding: 2% 2%;
}
.logo {
    padding: 2% 2%;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.title {
    padding: 2% 2%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.text {
    padding: 2% 2%;
}

.button {
    padding: 2% 2%;
}
</style>
