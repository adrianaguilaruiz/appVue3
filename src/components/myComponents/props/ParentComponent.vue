<script>
import ChildComponent from './ChildComponent.vue';

export default {
    data() {
        return {
            movieTitle: 'Superman',
            brandParent: '',
            count: 0,
        };
    },
    components: { ChildComponent },
    methods: {
        receivedBrand(data){
            this.brandParent = data;
            this.count++;
        }
    }
};
</script>

<template>
    <h2>I'm your parent</h2>
    <span>{{ movieTitle }}</span>
    <ChildComponent :movieTitle="movieTitle" @changeBrand="receivedBrand"/>
    <span>BRAND: {{ brandParent }} / {{ count }}</span>
</template>

<style></style>