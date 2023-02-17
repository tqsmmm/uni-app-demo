<template>
    <view class="main">
        <view class="text">
            <input placeholder="用户名" v-model="userId" />
        </view>
        <view class="text">
            <input password placeholder="密码" v-model="pass" />
        </view>
        <view class="text">
            <input password placeholder="确认密码" v-model="pass1" />
        </view>
        <view class="button">
            <button @click="submit">确定</button>
        </view>
        <view class="button">
            <button @click="reset">重置</button>
        </view>
        <view>
            <text>{{ userId }}</text>
        </view>
    </view>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const userId = ref('');
const pass = ref('');
const pass1 = ref('');

const submit = () => {
    console.log(userId.value, '--', pass.value, '--', pass1.value);
};

const reset = () => {
    userId.value = '';
    pass.value = '';
    pass1.value = '';
};
</script>

<style scoped>
*{
    outline: red 1px solid;
}
.main {
    padding: 2% 2%;
}
.text {
    padding: 2% 2%;
}
.button {
    padding: 2% 2%;
}
</style>
