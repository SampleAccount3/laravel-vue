<template>
    <div class="card">
        <header class="card-header">
            <p class="card-header-title">
                Task {{ cardData.cardCount + 1 }}
            </p>
            <button class="card-header-icon" aria-label="more options">
                <span class="icon">
                    <i class="fas fa-angle-down" aria-hidden="true"></i>
                </span>
            </button>
        </header>
        <div class="card-content">
            <div class="content">
                <p>{{ cardData.item }}</p>
                <p>Description: {{ cardData.description }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Cards",
    props: {
        cardData: Object,
    },
};
</script>
<style scoped>
    .box1{
        border: 1px;
        border-style:solid;
        border-color: red;
    }
    .box2{
        border: 1px;
        border-style:solid;
        border-color: blue;
    }
</style>
