<script>
export default {
    props: {
        image: {
            type: String,
            required: true
        },
        text: {
            type: String,
            required: true
        }
    }
}

</script>

<template>

    <li class="list-item-buy">
        <img :src="image" alt="">
        {{ text }}
    </li>

</template>

<style lang="scss" scoped> 

.list-item-buy {
    display: flex;
    align-items: center;
    gap: 15px;
    text-transform: uppercase;

    img {
        height: 50px;
    }
}
 
</style>