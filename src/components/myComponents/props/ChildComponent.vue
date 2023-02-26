<script>
export default {
    props: {
        movieTitle: String,
    },
    data() {
        return {
            brandChild: 'DC Comics',
        }
    },
    methods: {
        sendBrand(){
            this.$emit('changeBrand', this.brandChild)
        }
    }
}
</script>

<template>
    <h2>Child {{ movieTitle }}child</h2>
    <button @click="sendBrand">sendBrand</button>
</template>

<style></style>