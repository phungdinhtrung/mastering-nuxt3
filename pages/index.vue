<template>
    <NuxtLink to="/" class="mr-5">Trang chủ</NuxtLink>
    <NuxtLink to="/course">Course</NuxtLink>
        
    <div @click="handChangeLogin()">Change Login: {{ isLogin }}</div>

</template>

<script setup>
// useState
var isLogin = useIsLogin()

const handChangeLogin = () => {
    isLogin.value = !isLogin.value
}

const useProgress = useState<Boolean>('progress', () => {
    return isLogin.value
})

</script>