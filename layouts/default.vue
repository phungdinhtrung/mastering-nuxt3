<template>
    <div>
        <div class="header">Header shared across all pages</div>
        <!-- Navbar -->
        <NuxtLink to="/" class="mr-5 bg-slate-400 mt-5 mb-5">Trang chủ</NuxtLink>
        <NuxtLink to="/course" class="mr-5 bg-slate-400 mt-5 mb-5">Course</NuxtLink>
        <NuxtLink to="/course/chapter/chapter-1/lesson/lesson-1" class="mr-5 bg-slate-400 mt-5 mb-5">Lesson</NuxtLink>

      <!-- slot for show content by url -->
      <slot />

      <div class="footer">Footer shared across all pages</div>
    </div>
  </template>