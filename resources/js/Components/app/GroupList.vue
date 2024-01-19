<script setup>
import Groupitem from '@/Components/app/Groupitem.vue';
import TextInput from '@/Components/TextInput.vue';
import { ref } from 'vue';

const searchKeyword = ref("")
</script>

<template>
    <div class="bg-white rounded-lg h-[500px] flex flex-col overflow-hidden">
        <h2 class="py-6 pl-3 text-2xl font-bold">My Groups</h2>
        <div class="px-5">
           <TextInput :model-value="searchKeyword" placeholder="Type to search" class="w-full"/>
        </div>

        <div class="flex-1 mt-3 overflow-auto">
            <div v-if="false" class="p-3 text-center text-gray-400 ">
                You are not join any group
            </div>
            <div v-else>
                <Groupitem image="https://picsum.photos/100" title="Laravel Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <Groupitem image="https://picsum.photos/100" title="Vue js Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <Groupitem image="https://picsum.photos/100" title="Laravel Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <Groupitem image="https://picsum.photos/100" title="Vue js Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <Groupitem image="https://picsum.photos/100" title="Laravel Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <Groupitem image="https://picsum.photos/100" title="Vue js Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <Groupitem image="https://picsum.photos/100" title="Laravel Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <Groupitem image="https://picsum.photos/100" title="Vue js Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <Groupitem image="https://picsum.photos/100" title="Laravel Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <Groupitem image="https://picsum.photos/100" title="Vue js Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <Groupitem image="https://picsum.photos/100" title="Laravel Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <Groupitem image="https://picsum.photos/100" title="Vue js Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                    <Groupitem image="https://picsum.photos/100" title="Laravel Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <Groupitem image="https://picsum.photos/100" title="Vue js Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />

                    <Groupitem image="https://picsum.photos/100" title="Laravel Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <Groupitem image="https://picsum.photos/100" title="Vue js Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />

                    <Groupitem image="https://picsum.photos/100" title="Laravel Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />
                <Groupitem image="https://picsum.photos/100" title="Vue js Developers"
                    description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, nisi!" />


            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped></style>
