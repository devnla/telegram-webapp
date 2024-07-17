<script lang="ts" setup>

defineProps({
    user: {
        type: Object,
        required: true,
    },
})


</script>

<template>
    <div class="flex items-center">
        <img
            :src="user.profile_image_url"
            alt="User image"
            class="w-16 h-16 rounded-full mr-4"
        >
        <div>
            <h2>{{ user.first_name }} {{ user.last_name }}</h2>
            <p>@{{ user.username }}</p>
        </div>
    </div>
</template>
