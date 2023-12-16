<script setup></script>

<template>
  <div class="mx-auto w-fit flex flex-col items-center">
    <h1 class="text-5xl">The Home</h1>
    <div class="flex gap-2 items-baseline mt-4">
      <UButton>
        <ULink to="/api/login" external> Sign in </ULink>
      </UButton>
      <ULink to="/api/register" external> Sign up </ULink>
    </div>
  </div>
</template>
