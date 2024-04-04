<script>
export default {
    props: ['value']
}
</script>

<template>
    <div class="price">

        {{ value }}

    </div>
</template>

<style scoped>
.price {
    color: rgb(12, 6, 210);
}
</style>