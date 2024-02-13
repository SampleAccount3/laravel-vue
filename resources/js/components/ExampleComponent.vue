<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="columns">
                    <b-field label="Task" class="column">
                        <b-input v-model="inputTask"></b-input>
                    </b-field>
                </div>
                <div>
                    <b-button @click="AddStringToArrayList(inputTask)" class="mb-6" expanded type="is-primary">
                        Add New Task
                    </b-button>
                </div>
                <div>
                    <CardsVue v-for="(item, index) in sampleArrayList" :key="index" :cardData="item" />
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import CardsVue from './Cards.vue';
export default {
        // ... other component options
        name: 'ExampleComponents',
        components: {
            CardsVue,
        },
        data() {
    return {
        sampleArrayList: [],
        inputTask: '',
    };
    },
    methods: {
        AddStringToArrayList(value) {
            const newItem = {
                item: value,
                cardCount: this.sampleArrayList.length,
                description: 'Description goes here', // Add a description property
                // Add more properties if needed
            };
            this.sampleArrayList.push(newItem);
        },
    },
};
</script>
