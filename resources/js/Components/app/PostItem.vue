<script setup >
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { ChevronUpIcon } from '@heroicons/vue/20/solid'
defineProps({
   post: Object
});
function isImage(attachment) {
   const mime = attachment.mime.split('/')
   return mime[0].toLowerCase() === 'image'
}
</script>

<template>
   <div class="p-3 mb-3 bg-white border rounded shadow-md">
      <div class="flex items-center gap-2 mb-2">
         <a href="javascript:void(0)"><img class="w-[40px] rounded-full border-2 hover:border-blue-500 transition-all"
               :src="post.user.avatar" /></a>
         <div>
            <h3 class="font-bold "><a href="javascript:void(0)" class="hover:underline hover:text-blue-500">{{
               post.user.name }}</a>
               <template v-if="post.group"> >
                  <a href="javascript:void(0)" class="hover:underline hover:text-blue-500">{{ post.group.name }}</a>
               </template>
            </h3>
            <small class="text-gray-400">{{ post.created_at }}</small>
         </div>
      </div>
      <div>
         <Disclosure v-slot="{ open }">
            <div v-if="!open" v-html="post.body.substring(0, 150)" />
            <DisclosurePanel class="">
               <div v-html="post.body" />
            </DisclosurePanel>
            <div class="flex justify-end mb-3">
               <DisclosureButton class="text-blue-500">
                  <span class=" hover:underline hover:text-blue-400">{{ open ? 'Read less' : 'Read more...' }}</span>
               </DisclosureButton>
            </div>
         </Disclosure>

      </div>
      <div class="grid grid-cols-2 gap-3 mb-2 lg:grid-cols-3 ">
         <div v-for="attachment of post.attachments">

            <div class="relative flex flex-col items-center justify-center text-gray-500 bg-blue-100 group aspect-square">
               <button
                  class="absolute flex items-center justify-center p-1 bg-gray-400 rounded opacity-0 cursor-pointer right-2 top-2 hover:bg-gray-500 transtion-all group-hover:opacity-100">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                     stroke="currentColor" class="w-4 h-4 text-red-600 ">
                     <path stroke-linecap="round" stroke-linejoin="round"
                        d="M3 16.5v2.25A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75V16.5M16.5 12 12 16.5m0 0L7.5 12m4.5 4.5V3" />
                  </svg>
               </button>

               <img v-if="isImage(attachment)" :src="attachment.url" class="object-cover aspect-square" />

               <template v-else>
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                     stroke="currentColor" class="w-12 h-12">
                     <path stroke-linecap="round" stroke-linejoin="round"
                        d="M19.5 14.25v-2.625a3.375 3.375 0 0 0-3.375-3.375h-1.5A1.125 1.125 0 0 1 13.5 7.125v-1.5a3.375 3.375 0 0 0-3.375-3.375H8.25m2.25 0H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 0 0-9-9Z" />
                  </svg>
                  <small>
                     {{ attachment.name }}
                  </small>
               </template>
            </div>
         </div>
      </div>
      <div class="flex gap-2">
         <button class="flex items-center justify-center flex-1 gap-1 px-4 py-2 text-gray-800 bg-gray-100 rounded-lg hover:bg-gray-200">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
               stroke="currentColor" class="w-6 h-6">
               <path stroke-linecap="round" stroke-linejoin="round"
                  d="M6.633 10.25c.806 0 1.533-.446 2.031-1.08a9.041 9.041 0 0 1 2.861-2.4c.723-.384 1.35-.956 1.653-1.715a4.498 4.498 0 0 0 .322-1.672V2.75a.75.75 0 0 1 .75-.75 2.25 2.25 0 0 1 2.25 2.25c0 1.152-.26 2.243-.723 3.218-.266.558.107 1.282.725 1.282m0 0h3.126c1.026 0 1.945.694 2.054 1.715.045.422.068.85.068 1.285a11.95 11.95 0 0 1-2.649 7.521c-.388.482-.987.729-1.605.729H13.48c-.483 0-.964-.078-1.423-.23l-3.114-1.04a4.501 4.501 0 0 0-1.423-.23H5.904m10.598-9.75H14.25M5.904 18.5c.083.205.173.405.27.602.197.4-.078.898-.523.898h-.908c-.889 0-1.713-.518-1.972-1.368a12 12 0 0 1-.521-3.507c0-1.553.295-3.036.831-4.398C3.387 9.953 4.167 9.5 5 9.5h1.053c.472 0 .745.556.5.96a8.958 8.958 0 0 0-1.302 4.665c0 1.194.232 2.333.654 3.375Z" />
            </svg>

         </button>
         <button class="flex items-center justify-center flex-1 gap-1 px-4 py-2 text-gray-800 bg-gray-100 rounded-lg hover:bg-gray-200">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
               stroke="currentColor" class="w-6 h-6">
               <path stroke-linecap="round" stroke-linejoin="round"
                  d="M20.25 8.511c.884.284 1.5 1.128 1.5 2.097v4.286c0 1.136-.847 2.1-1.98 2.193-.34.027-.68.052-1.02.072v3.091l-3-3c-1.354 0-2.694-.055-4.02-.163a2.115 2.115 0 0 1-.825-.242m9.345-8.334a2.126 2.126 0 0 0-.476-.095 48.64 48.64 0 0 0-8.048 0c-1.131.094-1.976 1.057-1.976 2.192v4.286c0 .837.46 1.58 1.155 1.951m9.345-8.334V6.637c0-1.621-1.152-3.026-2.76-3.235A48.455 48.455 0 0 0 11.25 3c-2.115 0-4.198.137-6.24.402-1.608.209-2.76 1.614-2.76 3.235v6.226c0 1.621 1.152 3.026 2.76 3.235.577.075 1.157.14 1.74.194V21l4.155-4.155" />
            </svg>


         </button>
      </div>
   </div>
</template>

<style lang="scss" scoped></style>
