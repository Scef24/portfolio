<script>
export default{
    props:['fruitName'],

    methods:{
        RemoveFruit(){
            this.$emit('remove',this.fruitName)
        }
    }
};

</script>

<template>
    <li @click="RemoveFruit">{{ fruitName }}</li>
</template>


<style>
</style>