<script>
export default {
    data() {
        return {
            femcoders: [],
            newPerson: '',
            adding: false,
        }
    },
    methods: {
        addAFemCoder(){
            this.femcoders.push({
                id: this.femcoders.length + 1,
                person: this.newPerson,
            })
            this.newPerson=''
        },
        showInputToAdd(state){
            this.adding = state
            this.newPerson = ''
        },
    },
};
</script>


<template>
    <div>
        <h3>Directives v-if and v-else</h3>
        <label class="m-3">Testing directive v-if and v-else</label>
        <button
            v-if="adding == false"
            v-on:click="showInputToAdd(true)">
            Add a FemCoder
        </button>
        <button
            v-else
            v-on:click="showInputToAdd(false)">
            Cancel
        </button>
        <div v-if="adding">
            <input
                id="add-femcoder-input"
                @keyup.enter="addAFemCoder()"
                v-model="newPerson"
                placeholder="Add a FemCoder"
            />
            <button v-on:click="addAFemCoder()" class="btn btn-primary">+</button>
        </div>
        <span v-if="femcoders.length == 0" class="m-3">Please, add a FemCoder</span>
        <ul class="m-3">
            <template v-for="(femcoder, key) in femcoders" :key="femcoder.id">
                <li :id="key">{{ femcoder.id }}: {{ femcoder.person }}</li>
            </template>
        </ul>
    </div>
</template>

<style></style>