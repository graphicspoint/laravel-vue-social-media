<script setup >
import PostItem from './PostItem.vue';
const post1 = {
   user: {
      id:1,
      avatar: 'https://randomuser.me/api/portraits/men/57.jpg',
      name: 'jayadev'
   },
   group: null,
   attachments:[
      {
         id: 1,
         name: 'test.png',
         mime: 'image/png',
         url:'https://picsum.photos/999'
      },
      {
         id: 2,
         name: 'test.png',
         mime: 'image/png',
         url:'https://picsum.photos/997'
      }
   ],
   body:
   `<p class="my-1">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum molestias totam, delectus cupiditate error praesentium quam ad voluptates perspiciatis illum!</p>
   <p class="my-1">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum molestias totam, delectus cupiditate error praesentium quam ad voluptates perspiciatis illum!</p>
   `,
   created_at: '2024-01-13'
}
const post2 = {
   user: {
      id:2,
      avatar: 'https://randomuser.me/api/portraits/men/77.jpg',
      name: 'Umesh'
   },
   group: {
      id: 1,
      name: 'Vue Js Developers'
   },
   attachments:[
      {
         id: 1,
         name: 'test.png',
         mime: 'image/png',
         url:'https://picsum.photos/950'
      },
      {
         id: 2,
         name: 'test.png',
         mime: 'image/png',
         url:'https://picsum.photos/991'
      }
   ],
   body:
   `<p class="my-1">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum molestias totam, delectus cupiditate error praesentium quam ad voluptates perspiciatis illum!</p>
   <p class="my-1">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum molestias totam, delectus cupiditate error praesentium quam ad voluptates perspiciatis illum!</p>
   `,
   created_at: '2024-01-13'
}
const post3 = {
   user: {
      id:2,
      avatar: 'https://randomuser.me/api/portraits/men/77.jpg',
      name: 'Smruti'
   },
   group: {
      id: 1,
      name: 'Laravel Developers'
   },
   attachments:[
      {
         id: 1,
         name: 'test.png',
         mime: 'image/png',
         url:'https://picsum.photos/1000'
      },
      {
         id: 2,
         name: 'test.png',
         mime: 'image/png',
         url:'https://picsum.photos/1000'
      },
      {
         id: 3,
         name: 'mydoc.docx',
         mime: 'application/msword',
         url:'#'
      }
   ],
   body:
   `<p class="my-1">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum molestias totam, delectus cupiditate error praesentium quam ad voluptates perspiciatis illum!</p>
   <p class="my-1">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum molestias totam, delectus cupiditate error praesentium quam ad voluptates perspiciatis illum!</p>
   `,
   created_at: '2024-01-13'
}

</script>

<template>
   <div>
      <div>
         <PostItem :post="post1"/>
         <PostItem :post="post2"/>
         <PostItem :post="post3"/>

      </div>

   </div>
</template>

<style lang="scss" scoped>

</style>
