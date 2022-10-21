<template>
    <div>
      <NuxtLayout :name="layout">
        <NuxtPage />
      </NuxtLayout>
    </div>
  </template>
  <script setup lang="ts">
  const layout = "min-layout";
  </script>
  