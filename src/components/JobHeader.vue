<template>
    <h4 :class="['text-base font-semibold text-purple-500', $attrs.class]">
        {{ company }}
    </h4>
    <div class="flex justify-between">
        <h5 class="italic text-xs text-slate-500">
            {{ title }}
        </h5>

        <span class="text-xs text-slate-500 font-semibold">{{ startDate }} &mdash; {{ endDate }}</span>
    </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
    company: {
        type: String,
        required: true,
    },

    title: {
        type: String,
        required: true,
    },

    active: {
        type: Array,
        required: true,
        validator(value) {
            return value.some(part => isNaN(part)) === false
        },
    },
})

const startDate = computed(() => props.active[0])
const endDate = computed(() => props.active[1] ?? 'present')
</script>
