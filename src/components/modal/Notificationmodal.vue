<template>
    <div class="fixed top-0 left-0 w-screen h-screen 
    flex justify-center items-center 
    z-30 font-notosans-light">
        <div class="relative pc:w-[830px] pc:h-[297px]         
        flex justify-center items-center 
        text-style3 text-base tracking-[3px]
        rounded-px35 bg-white z-10">
            <div class="">{{ props.notification_msg }}</div>
            <div class="absolute right-4 bottom-4 w-44 h-14
            flex justify-center items-center
            text-white bg-bg4 rounded-full cursor-pointer" @click="emits('togglenotificationmodal')">
                ζη₯ιδΊ
            </div>
        </div>

        <div class="absolute top-0 w-full h-full bg-black opacity-20"></div>
    </div>
</template>

<script setup lang="ts">
const props = defineProps<{ notification_msg: String, }>()
const emits = defineEmits<{ (e: 'togglenotificationmodal'): void }>()
</script>