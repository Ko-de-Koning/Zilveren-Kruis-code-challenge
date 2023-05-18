<script setup lang="ts">
defineProps<{
    label: string;
    idLabel: string;
    options: string[];
}>();
</script>

<template>
    <div class="form-input my-4">
        <label id="{{idLabel}}" class="input__title">
            {{ label }}
        </label>

        <div class="input__group">
            <select class="form-control">
                <option v-for="option in options" :key="option">
                    {{ option }}
                </option>
            </select>
        </div>
    </div>
</template>
