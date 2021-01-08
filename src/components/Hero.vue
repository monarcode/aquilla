<template>
    <div>
        <img src="../assets/img/model.png" alt="" class="hero">
    </div>
</template>

<script>
export default {
    name: "Hero"
}
</script>

<style lang="scss" scoped>
    .hero {
        width: 40rem;
        height: auto;
        background-color: var(--secondary_clr);
        box-shadow: 0 0 30px -5px rgba(0, 0, 0, 0.233);
    }
</style>