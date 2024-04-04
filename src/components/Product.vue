<script>

import Name from './Name.vue';
import Price from './Price.vue';
import Description from './Description.vue';

export default {
    components: {
        Name,
        Price,
        Description
    },

    props: {
        name: String,
        price: String,
        description: String
    }

}

</script>

<template>
    <Name :value='name' />
    <Price :value='price' />
    <Description :value='description' />
</template>