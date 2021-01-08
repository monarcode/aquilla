<template>
    <div class="navv">
        <ul class="list">
            <li class="list__item"><a href="#">Home</a></li>
            <li class="list__item"><a href="#">About</a></li>
            <li class="list__item list__model"><img src="../assets/img/model-2.png" alt="model-2"></li>
            <li class="list__item"><a href="#">Gallery</a></li>
            <li class="list__item"><a href="#">Contact</a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "Nav"
}
</script>

<style lang="scss" scoped>
    .list {
        display: flex;
        list-style: none;
        display: flex;
        justify-content: center;
        align-items: center;

        &__item {
            margin: 1rem calc(var(--spacer) * 2);

            a {
                font-size: 1.4rem;
                text-transform: uppercase;
                letter-spacing: calc(var(--spacer) * 1);
                position: relative;

                &::before {
                    content: '';
                    width: 10px;
                    height: 10px;
                    border: 1px solid rgba(235, 235, 235, 0);
                    border-radius: 50%;
                    position: absolute;
                    top: -5px;
                    left: -5px;
                }

                &:hover::before{
                    width: 100%;
                    height: 30px;
                    border: 1px solid rgb(235, 235, 235);
                    border-radius: 10px;
                    transition: all 0.2s ease-in-out;
                }
            }
        }

        &__model {
            border-radius: 50%;
            width: 10rem;
            height: 10rem;
            display: inline-block;
            overflow: hidden;
        }
    }
</style>