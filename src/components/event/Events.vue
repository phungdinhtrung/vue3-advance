<script setup>
import { ref } from "vue";

const count = ref(0);

const handleClick = () => {
    console.log("Button clicked!");
};

const onSubmit = () => {
    console.log("Form submitted!");
};

const onKeyUpEnter = () => {
    console.log("onKeyUpEnter!");
};

const clear = () => {
    console.log("clear!");
};

const doSomething = () => {
    console.log("doSomething!");
};
</script>

<template>
    <h1>Events</h1>
    <button @click="handleClick">Click me!</button>

    <h1>Counts</h1>
    <button @click="count++">Count: {{ count }}</button>

    <h1>submit form</h1>
    <form @submit.prevent="onSubmit">
        <input type="text" />
        <button type="submit">Submit</button>
    </form>

    <h1>Keyup Enter</h1>
    <input @keyup.enter="onKeyUpEnter" />

    <h1>Key Alt + Enter</h1>
    <input @keyup.alt.enter="clear" />

    <h1>Mouse Click + Ctrl</h1>
    <div @click.ctrl="doSomething">Do something</div>
</template>
