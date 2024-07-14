<script setup>
import { ref } from "vue";

const styleObject = ref({
    color: "red",
    fontSize: "20px",
});
</script>

<template>
    <h1>Class</h1>

    <!-- $attrs.class: chỉ truyền class từ component cha vào thẻ này -->
    <p :class="$attrs.class">Hi!</p>

    <!-- styleObject: truyền object chứa style vào thẻ này -->
    <p :style="styleObject">Hi!</p>
</template>

<style>
.error {
    color: red;
}

.success {
    color: green;
}
</style>
