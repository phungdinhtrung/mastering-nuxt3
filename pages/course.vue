
<script setup>
// useState
const isLogin = useIsLogin()

</script>

<template>   
    <div class="flex justify-center">
        Course
    </div>
    <div class="flex flex-row justify-center flex-grow">
        <div class="prose bg-white mr-4 ">
            Chapter {{ isLogin }}
        </div>
        <div class="prose bg-stone-500">
            <NuxtPage />
        </div>
    </div>
</template>
