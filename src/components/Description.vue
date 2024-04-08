<script>
export default {
    props: {
        value: String,
    }
}
</script>

<template>
    <div class="description">
        <p>{{ value }}</p>
    </div>
</template>

<style scoped>
.description {

    font-style: italic;
}
</style>