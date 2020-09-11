<template>
  <img class="phot" v-bind:src="'/img/' + src">
</template>

<script>
import $ from "jQuery"

export default {
    name: "Photo",
    props: ["src"],
    mounted() {
        $(".phot").on("click", function() {
            console.log("caca");
        })
    }
}
</script>

<style scoped>
img {
    width: 50%;
    padding-top: 10px;
    padding-bottom: 10px;

    transition-property: width, padding-top, padding-bottom, filter;
    transition-duration: .5s;
}

img:hover {
    animation: trans .5s;
    width: 53%;
    padding-top: 2px;
    padding-bottom: 2px;
}

@keyframes trans {
    0% {
        width: 50%;
        padding-top: 10px;
        padding-bottom: 10px;
    }

    50% {
        filter: blur(2px);
    }

    100% {
        width: 53%;
        padding-top: 2px;
        padding-bottom: 2px;
        filter: blur(0px);
    }
}
</style>