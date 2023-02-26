<script>
    export default {
        data() {
            return {
                listCountry: ["Spain", "Venezuela", "Argentina"],
            }
        },
    }
</script>

<template>
    <div>
        <h3>----------v-for directive------------</h3>
        <ul>
            <template v-for="(country, key) in listCountry" :key="key">
                <li :id="[key + 1]"> {{ key }}: {{ country }}</li>
            </template>
        </ul>
    </div>
</template>

<style></style>