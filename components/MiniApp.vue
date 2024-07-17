<script lang="ts" setup>
import { MainButton, useWebAppPopup } from 'vue-tg'
import { useWebApp } from 'vue-tg'

const initData = useWebApp().initData
const initDataUnsafe = useWebApp().initDataUnsafe

const { showAlert } = useWebAppPopup()
</script>

<template>
    <h1>Mini App - Shop Test</h1>

    <label for="initData">initData</label>
    <textarea class="w-100" name="initData">
        {{ initData }}
    </textarea>

    <label for="initDataUnsafe">initDataUnsafe</label>
    <textarea class="w-100" name="initDataUnsafe">
        {{ initDataUnsafe }}
    </textarea>
    <MainButton text="Open alert" @click="() => showAlert('Hello!')" />
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