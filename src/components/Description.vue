<script>
export default {
    props: ['value']
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