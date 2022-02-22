<template>
    <div
        class="bg-gray-400 overflow-hidden shadow p-6 absolute top-0 left-0 w-screen"
    >
        <h1 class="display-4">{{ titre }}</h1>
    </div>
</template>

<script>
export default {
    name: "titrePage",
    props: ["titre"],
};
</script>

<style scoped>
h1 {
    font-family: Roboto, sans-serif;
}
</style>
