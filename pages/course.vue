
<script setup>
// useState
const courses = useCourse()
const lesson_path = courses.chapters[0].lessons[0].path

</script>

<template>   
    <div class="my-5">
        Course: {{  courses.title }}
    </div>
    <div class="my-5">
        <div class="prose bg-white my-5 ">
            Chapter {{ courses.chapters[0].title }}
        </div>
        <div class="prose bg-white my-5 ">
            <NuxtLink :to="lesson_path"><button class="bg-slate-500 my-5">Lesson</button></NuxtLink>
        </div>
        <div class="prose bg-stone-500">
            <NuxtPage />
        </div>
    </div>
</template>
