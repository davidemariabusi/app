<template>
    <div class="bg-slate-100 space-y-2 dark:bg-slate-800 rounded-sm px-2 p-1">
        <div v-html="props.payload.html"></div>
    </div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";
import { Payload } from "@/types/Payload";

const props = defineProps<{
    payload: Payload;
}>();
</script>
