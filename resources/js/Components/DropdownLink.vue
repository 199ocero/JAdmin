<script setup>
import { Link } from "@inertiajs/vue3";
</script>

<template>
  <Link
    class="block w-full px-4 py-2 text-left bg-gray-800 text-sm leading-5 text-gray-400 hover:bg-gray-700 focus:outline-none focus:bg-gray-700 transition duration-150 ease-in-out"
  >
    <slot />
  </Link>
</template>
