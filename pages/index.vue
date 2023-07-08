<template>
    <div @click="handChangeLogin()"><button class="bg-slate-500 my-5">Change Login</button> {{ isLogin }}</div>

</template>

<script setup>
// useState
var isLogin = useIsLogin()

const handChangeLogin = () => {
    isLogin.value = !isLogin.value
    progress.value = isLogin.value;
}

// useLocalStorage
const progress = useLocalStorage('progress', true)

</script>