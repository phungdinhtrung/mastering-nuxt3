<template>
    <div @click="handChangeLogin()">Change Login: {{ isLogin }}</div>

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