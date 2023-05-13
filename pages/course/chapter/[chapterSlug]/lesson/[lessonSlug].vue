<script lang="ts" setup>
const course = useCourse()
const chapter = course.chapters[0].title
const lesson = course.chapters[0].lessons[0].title

// useHead
useHead({
    title: 'Course'
})

// Use layout
definePageMeta({
    layout: 'custom'
})

</script>

<template>
    <h2>course/chapter-[chapterSlug]/lesson-[lessonSlug].vue</h2>
    <p>This is a lesson</p>    
    <p>Chapter slug: {{ $route.params.chapterSlug }}, {{ chapter }}</p>    
    <p>lesson slug: {{ $route.params.lessonSlug }}, {{ lesson }}</p>    

    <div>Video player</div>
    <VideoPlayer :videoId="`video1`"></VideoPlayer>

    <div></div>
    
</template>