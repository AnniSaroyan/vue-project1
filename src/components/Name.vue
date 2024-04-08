<script>
export default {
    props: {
        value: String,
    }
}
</script>

<template>
    <div class="name">
        <h2> {{ value }} </h2>
    </div>
</template>

<style scoped>
.name {

    font-weight: bold;
    margin-top: 10px;

}
</style>