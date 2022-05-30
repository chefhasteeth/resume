<template>
    <h4 :class="['font-medium text-slate-900', $attrs.class]">
        {{ title }}
    </h4>
    <p class="mt-2">
        <span
            v-for="(item, index) in items"
            :key="item"
        >
            {{ item }}
            <span
                v-if="index < items.length - 1"
                class="separator"
            >
                /
            </span>
        </span>

        <span
            v-if="etc"
            class="separator"
        >
            etc
        </span>
    </p>
</template>

<script setup>
defineProps({
    title: {
        type: String,
        required: true,
    },

    items: {
        type: Array,
        required: true,
    },

    etc: {
        type: Boolean,
        default: false,
    },
})
</script>
