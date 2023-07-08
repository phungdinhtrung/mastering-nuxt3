<template>
    <h2>course/chapter-[chapterSlug]/lesson-[lessonSlug].vue</h2>
    <p>This is a lesson</p>    
    <p>Chapter slug: {{ $route.params.chapterSlug }}</p>    
    <p>lesson slug: {{ $route.params.lessonSlug }}</p>    
</template>

<script lang="ts" setup>

 definePageMeta({
    middleware: [
        function(to, from){
            console.log('$route.params.chapterSlug');
            console.log('to', to);
            console.log('from', from);
            
            if(from.params.chapterSlug == 'chapter-1') return;
            
            return navigateTo('/')
        }
    ]
 })

</script>
