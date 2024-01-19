<script setup>
defineProps({
    image: String,
    title: String,

})
</script>

<template>
    <div class="cursor-pointer hover:bg-gray-100">
        <div class="flex items-start gap-3 py-2 mb-3">
            <img :src="image" alt="" class="w-[48px] rounded-full">
            <div>
                <h3 class="text-xl font-black">{{ title }}</h3>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped></style>
