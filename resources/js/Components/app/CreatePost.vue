<script setup >
import { ref } from 'vue';

const postCreating = ref(false);
</script>

<template>
   <div class="p-3 mb-3 bg-white rounded">
      <div @click="postCreating = true" class="px-2 py-3 mb-3 text-gray-500 border-2 border-gray-200 rounded-md">
         <h2>Click here to create new post</h2>

      </div>
      <div v-if="postCreating" class="flex justify-between">
         <button type="button"
            class=" flex rounded-md bg-white px-2.5 py-1.5 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 hover:bg-gray-50 relative">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
               stroke="currentColor" class="w-6 h-6">
               <path stroke-linecap="round" stroke-linejoin="round"
                  d="m18.375 12.739-7.693 7.693a4.5 4.5 0 0 1-6.364-6.364l10.94-10.94A3 3 0 1 1 19.5 7.372L8.552 18.32m.009-.01-.01.01m5.699-9.941-7.81 7.81a1.5 1.5 0 0 0 2.112 2.13" />
            </svg>

            Attach Files
            <input type="file" name="" id="" class="absolute top-0 bottom-0 left-0 right-0 opacity-0">
         </button>

         <button type="submit"
            class="px-3 py-2 text-sm font-semibold text-white bg-indigo-600 rounded-md shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Submit</button>
      </div>
   </div>
</template>

<style lang="scss" scoped></style>
