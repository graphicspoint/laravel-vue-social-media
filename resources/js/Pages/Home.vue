<script setup>
import { Head, Link } from '@inertiajs/vue3';
import GroupList from '@/Components/app/GroupList.vue';
import FollowingList from '@/Components/app/FollowingList.vue';
import CreatePost from '@/Components/app/CreatePost.vue';
import PostList from '@/Components/app/PostList.vue';
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';



defineProps({

});
</script>

<template>
   <Head title="Social media Website" />
   <AuthenticatedLayout>
   <div class="grid h-full grid-cols-12 gap-3 px-3 py-2">
      <div class="h-full col-span-12 overflow-hidden lg:col-span-3 lg:order-1">
         <GroupList />
      </div>
      <div class="h-full col-span-12 overflow-hidden lg:col-span-3 lg:order-3">
         <FollowingList />
      </div>
      <div class="h-full col-span-12 overflow-auto lg:col-span-6 lg:order-2">
         <CreatePost/>
         <PostList/>
      </div>

   </div>
   </AuthenticatedLayout>
</template>

<style>
.bg-dots-darker {
   background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(0,0,0,0.07)'/%3E%3C/svg%3E");
}

@media (prefers-color-scheme: dark) {
   .dark\:bg-dots-lighter {
      background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(255,255,255,0.07)'/%3E%3C/svg%3E");
   }
}
</style>
