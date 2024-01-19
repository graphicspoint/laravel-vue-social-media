<script setup>
import FollowingItem from '@/Components/app/FollowingItem.vue';
import TextInput from '@/Components/TextInput.vue';
import { ref } from 'vue';

const searchKeyword = ref("")
</script>

<template>
    <div class="col-span-12 bg-white border rounded lg:col-span-3 h-[500px] flex flex-col overflow-hidden">
        <h2 class="py-6 pl-3 text-2xl font-bold">My Friends</h2>
        <div class="px-5">
           <TextInput :model-value="searchKeyword" placeholder="Type to search" class="w-full"/>
        </div>

        <div class="flex-1 px-3 mt-3 overflow-auto">
            <div v-if="false" class="p-3 text-center text-gray-400 ">
                You dont have any friends
            </div>
            <div v-else>
                <FollowingItem image="https://picsum.photos/100" title="jayadev Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <FollowingItem image="https://picsum.photos/100" title="Umesh"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <FollowingItem image="https://picsum.photos/100" title="jayadev Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <FollowingItem image="https://picsum.photos/100" title="Umesh"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <FollowingItem image="https://picsum.photos/100" title="jayadev Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <FollowingItem image="https://picsum.photos/100" title="Umesh"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <FollowingItem image="https://picsum.photos/100" title="jayadev Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <FollowingItem image="https://picsum.photos/100" title="Umesh"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />

                    <FollowingItem image="https://picsum.photos/100" title="jayadev Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <FollowingItem image="https://picsum.photos/100" title="Umesh"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <FollowingItem image="https://picsum.photos/100" title="jayadev Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <FollowingItem image="https://picsum.photos/100" title="Umesh"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />


                    <FollowingItem image="https://picsum.photos/100" title="jayadev Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <FollowingItem image="https://picsum.photos/100" title="Umesh"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <FollowingItem image="https://picsum.photos/100" title="jayadev Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <FollowingItem image="https://picsum.photos/100" title="Umesh"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <FollowingItem image="https://picsum.photos/100" title="jayadev Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <FollowingItem image="https://picsum.photos/100" title="Umesh"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />

            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped></style>
