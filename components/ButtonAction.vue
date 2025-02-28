<template>
  <div class="pt-6 text-center space-y-4">
    <a
      :href="link"
      target="_blank"
      class="flex items-center rounded-2xl bg-gray-100 px-6 py-4 text-lg font-medium shadow-md hover:shadow-lg transition ease-in-out duration-150 border border-gray-300"
    >
      <p v-if="isEmoji(icon)" class="mr-3 h-8 w-8 text-2xl">{{ icon }}</p>
      <img v-else :src="icon" alt="icon" class="mr-3 h-8 w-8" />
      <span class="text-gray-800">{{ text }}</span>
      <div class="ml-auto pl-4">
        <svg
          class="h-5 w-5 text-gray-400"
          xmlns="http://www.w3.org/2000/svg"
          fill="currentColor"
          viewBox="0 0 20 20"
        >
          <path
            fill-rule="evenodd"
            d="M4.646 1.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1 0 .708l-6 6a.5.5 0 0 1-.708-.708L10.293 8 4.646 2.354a.5.5 0 0 1 0-.708z"
          />
        </svg>
      </div>
    </a>
  </div>
</template>

<script setup>
const { link, icon, text } = defineProps(["link", "icon", "text"]);

const isEmoji = (icon) => {
  return typeof icon === "string" && icon.length <= 2;
};
</script>

<style scoped>
a {
  transition: all 0.3s ease;
}
a:hover {
  background-color: #e5e7eb;
}
</style>
