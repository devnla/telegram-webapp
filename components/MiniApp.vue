<script lang="ts" setup>
import { MainButton, useWebAppPopup } from 'vue-tg'
import { useWebApp } from 'vue-tg'

const initData = useWebApp().initData
const initDataUnsafe = useWebApp().initDataUnsafe

const user = {
    first_name: initDataUnsafe.user?.first_name,
    last_name: initDataUnsafe.user?.last_name,
    username: initDataUnsafe.user?.username,
    profile_image_url: 'https://i.pravatar.cc/300',
}

const { showAlert } = useWebAppPopup()
</script>

<template>
    <div>
        <h1>Mini App - Shop Test</h1>

        <code class="w-100">
            {{ initDataUnsafe }}
        </code>
        <MainButton text="Open alert" @click="() => showAlert('Hello!')" />
    </div>
</template>