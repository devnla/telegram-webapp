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

        <Profile :user="user" />

        <label for="initData">initData</label>
        <textarea class="w-100" name="initData">
            {{ initData }}
        </textarea>

        <label for="initDataUnsafe">initDataUnsafe</label>
        <textarea class="w-100" name="initDataUnsafe">
            {{ initDataUnsafe }}
        </textarea>
        <Signup />
        <MainButton text="Open alert" @click="() => showAlert('Hello!')" />
    </div>
</template>

<style scoped>
h1{
    text-align: center;
}
textarea{
    margin: 0;
    width: 100%;
    height: 200px;
    padding: 0;
}
</style>