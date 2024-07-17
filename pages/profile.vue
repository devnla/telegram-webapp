<script lang="ts" setup>
import { useWebApp } from 'vue-tg'

const initDataUnsafe = useWebApp().initDataUnsafe

const user = {
    first_name: initDataUnsafe.user?.first_name,
    last_name: initDataUnsafe.user?.last_name,
    username: initDataUnsafe.user?.username,
    profile_image_url: 'https://i.pravatar.cc/300',
}
</script>
<template>
    <ClientOnly>
        <div class="my-4">
        <Profile :user="user" />
    </div>
    </ClientOnly>
</template>