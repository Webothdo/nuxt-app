<script setup>
const links = [
  {
    label: "Dashboard",
    to: "/dashboard",
  },
  {
    label: "About",
    to: "/about",
  },
  {
    label: "Setting",
    to: "/dashboard/settings",
  },
];
</script>

<template>
  <div>
    <div class="flex gap-4 justify-between m-4">
      <ULink to="/" class="text-green-400">Home</ULink>
      <div class="flex gap-4 justify-between">
        <div v-for="(link, index) in links" :key="link.to" class="text-red-400">
          <ULink
            :class="[index === 0 && !$auth.loggedIn ? 'hidden' : '']"
            :to="link.to"
            >{{ link.label }}</ULink
          >
        </div>
      </div>
    </div>
  </div>
</template>
