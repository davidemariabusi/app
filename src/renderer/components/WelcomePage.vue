<template>
    <div>
        <div class="right-0 flex justify-center items-center">
            <div id="output"></div>

            <!-- welcome page -->
            <div class="w-full px-4 text-sm dark:text-slate-300 leading-6">
                <!-- app guide -->
                <AppGuide />
            </div>
        </div>
        <div class="fixed left-[80px] bottom-10 w-auto">
            <div class="flex gap-2 justify-end text-right">
                <div v-for="shortcut in globalShortcutList">
                    <span
                        v-if="shortcut.hasOwnProperty('shortcut')"
                        :key="shortcut.alias"
                        class="font-light bg-slate-100 dark:bg-slate-800 dark:text-slate-400 rounded-md p-1 px-2 text-xs"
                        ><strong>{{ $t(shortcut.label) }}</strong
                        >: {{ shortcut.originalValue }}</span
                    >
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import AppGuide from "@/components/AppGuide.vue";

defineProps({
    globalShortcutList: {
        required: true,
        type: Array
    }
});
</script>
