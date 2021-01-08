<template>
    <div class="header">
        <h1>{{list.name}}</h1>
    </div>
</template>

<script>
export default {
    name: "Header",
    props: ["list"]
}
</script>

<style lang="scss" scoped>
    .header {
        text-align: center;
        margin: calc(var(--spacer) * 3) 0;
        letter-spacing: calc(var(--spacer) * 2);
    }
</style>