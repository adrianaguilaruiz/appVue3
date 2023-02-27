<script>
export default {
    data(){
        return {
            title: "FemCoders Málaga P1",
            person:{
                id: 1,
                name: 'Adri',
                img : 'https://st2.depositphotos.com/1006318/5909/v/950/depositphotos_59094623-stock-illustration-female-avatar-woman.jpg',
            },
            msg: "Adri is one of the FemCoders of the first promotion in Malaga (Arrabal and F5)."
        }
    },
};
</script>

<template>
    <h3>{{ title }}</h3>
    <div :id="person.id">
        <h4>{{ person.name }}</h4>
        <img :src="person.img" :alt="person.name">
    </div>
    <h5 v-html="msg"></h5>
</template>

<style lang="css" scoped>
    h3{
        color:blueviolet;
    }
    img{
        width: 25%;
    }
</style>