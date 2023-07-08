
<script setup>
// useState
const isLogin = useIsLogin()

definePageMeta({
    middleware: function(to, from){
        // Phải đưa isLogin vào mặc dù phía trên đã có vì middle khởi tạo đầu tiên trước, sau đó mới đến các useState, biến, hàm trong script nằm ngoài middleware
        const isLogin = useIsLogin()
        if(isLogin.value == false) return navigateTo('/')
    }
})

</script>

<template>   
    <div class="my-5">
        Login status: {{  isLogin }}
    </div>
    
</template>
