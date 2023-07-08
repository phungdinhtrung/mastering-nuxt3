<template>
    <div>
        <div class="header">Header shared across all pages</div>
        <!-- Navbar -->
        <NuxtLink to="/" class="mr-5 bg-slate-400 mt-5 mb-5">Trang chủ</NuxtLink>
        <NuxtLink to="/course" class="mr-5 bg-slate-400 mt-5 mb-5">Course</NuxtLink>
        <NuxtLink to="/course/chapter-1/lesson-1" class="mr-5 bg-slate-400 mt-5 mb-5">Course chapter 1</NuxtLink>
        <NuxtLink :to="lesson_path" class="mr-5 bg-slate-400 mt-5 mb-5">Lesson</NuxtLink>
        <NuxtLink to="/login" class="mr-5 bg-slate-400 mt-5 mb-5">Login</NuxtLink>

      <!-- slot for show content by url -->
      <slot />

      <div class="footer">Footer shared across all pages</div>
    </div>
  </template>

<script setup>
// useState
const courses = useCourse()
const lesson_path = courses.chapters[0].lessons[0].path

</script>