<template>
    <div class="container">
        <b-button type="is-primary" @click="IncreaseNumber()">
            {{ totalNumber }}
        </b-button>
        <div class="is-flex my-3">
            <div @mouseenter="HandleEvent" class="boxSample me-2">
                Mouse On enter   
            </div>
            <div @mouseout="HandleEvent" class="boxSample mx-2">
                Mouse On exit  
            </div>
            <div @dblclick="HandleEvent" class="boxSample mx-2">
                Mouse Double Click
            </div>
            <div @mousemove="HandleMouseMovement" class="boxSample mx-2">
                {{ x }} - {{ y }}
            </div>
        </div>
        <b-button type="is-primary">Primary</b-button>
    </div>
</template>
<style></style>
<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        },
        methods: {
            IncreaseNumber(){
                this.totalNumber++;
            },
            HandleEvent(){
                console.log("OK");
            },
            HandleMouseMovement(e){
                this.x = e.offsetX;
                this.y = e.offsetY;
            }
        },
        data() {
            return {
                totalNumber: 0,
                x: 0,
                y:0
            }
        }
    }
</script>
<style scoped>
    .boxSample{
        height: 100px;
        width: 100px;
        background: skyblue;
    }
</style>
