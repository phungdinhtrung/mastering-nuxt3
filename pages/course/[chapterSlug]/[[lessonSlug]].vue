<template>
    <h2>course/[chapterSlug]/[[lessonSlug]].vue</h2>
    <p>This is a lesson</p>    
    <p>Chapter slug: {{ $route.params.chapterSlug }}</p>    
    <p>lesson slug: {{ $route.params.lessonSlug }}</p>    
</template>