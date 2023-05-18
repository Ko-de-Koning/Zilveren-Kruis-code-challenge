<script setup lang="ts">
defineProps<{
    label: string;
    idLabel: string;
    placeholder?: string;
    options: string[];
    disabled?: boolean; // TODO
}>();
</script>

<template>
    <div class="form-input my-4">
        <label id="{{idLabel}}" class="input__title">
            {{ label }}
        </label>

        <div class="input__group">
            <select class="form-control">
                <option
                    class="text-muted"
                    v-if="placeholder"
                    value=""
                    disabled
                    selected
                    hidden
                >
                    {{ placeholder }}
                </option>
                <option v-for="option in options" :key="option">
                    {{ option }}
                </option>
            </select>
        </div>
    </div>
</template>
