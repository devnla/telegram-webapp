<script lang="ts" setup>

defineProps({
    user: {
        type: Object,
        required: true,
    },
})


</script>

<template>
    <div class="w-96 mx-auto px-6 py-6  text-center bg-gray-800 rounded-lg lg:mt-0 xl:px-10">
        <div class="space-y-4 xl:space-y-6">
            <img class="mx-auto rounded-full h-36 w-36" :src="user.profile_image_url" alt="author avatar">
            <div class="space-y-2">
                <div class="flex justify-center items-center flex-col space-y-3 text-lg font-medium leading-6">
                    <h3 class="text-white">{{ user.first_name }} {{ user.last_name }}</h3>
                    <p class="text-indigo-300">{{ user.username ? '@' + user.username : 'No username' }}</p>
                </div>
            </div>
        </div>
    </div>
</template>
