<script setup>
definePageMeta({
  middleware: ["auth-logged-in"],
});
</script>

<template>
  <div class="mx-auto w-fit flex flex-col items-center">
    <h1 class="text-5xl">The dashboard page</h1>
    <p v-if="$auth.loggedIn">I'm signed in!</p>
    <p v-else>I'm signed out :(</p>
    <div class="mt-4">
      <UButton color="rose" variant="soft">
        <ULink to="/api/logout" external> Sign out </ULink>
      </UButton>
    </div>
  </div>
</template>
