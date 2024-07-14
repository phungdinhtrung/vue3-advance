<script setup>
import { ref } from "vue";

const isError = ref(true);
const isSussess = ref(true);
</script>

<template>
    <!-- Class -->
    <Class class="success" />
    <Class :class="{ success: isSussess }" />
    <Class :class="{ error: isError }" />
</template>

<style scoped>
.error {
    color: red;
}

.success {
    color: green;
}
</style>
