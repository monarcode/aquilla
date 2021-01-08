<template>
    <div>
        <ul class="socials">
            <li v-bind:key="socials.instagram" class="socials__link">
                <a v-bind:href="'https://instagram.com/' + socials.instagram " ><img src="../assets/img/instagram-ic.svg" alt=""></a>
            </li>
            <li v-bind:key="socials.twitter" class="socials__link">
                <a v-bind:href="'https://twitter.com/' + socials.twitter " ><img src="../assets/img/twitter-ic.svg" alt=""></a>
            </li>
            <li v-bind:key="socials.snapchat" class="socials__link">
                <a v-bind:href="'https://snapchat.com/' + socials.snapchat " ><img src="../assets/img/snapchat-ic.svg" alt=""></a>
            </li>
            <li v-bind:key="socials.instagram" class="socials__link">
                <a v-bind:href="'mailto:' + socials.email " ><img src="../assets/img/email-ic.svg" alt=""></a>
            </li>
        </ul>
        <!-- <p>{{socials.instagram}}</p> -->
    </div>
</template>

<script>
export default {
    name: "Socials",
    props: ["socials"]
}
</script>

<style lang="scss" scoped>
    .socials {
        position: absolute;
        right: 5%;
        top: 50%;
        transform: translateY(-50%);
        list-style: none;

        &__link {
            margin: 1.2rem 0;
            transition: all 0.3s ease-in-out;

            &:hover {
                transform: scale(1.2);
                transition: all 0.3s ease-in-out;
            }
        }

    }
</style>