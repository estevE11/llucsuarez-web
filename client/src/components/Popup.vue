<template>
    <div class="popup" id="#pop">
            <div class="back" @click="close"></div>
            <div class="ph">
                <img id="i" v-bind:src="src">
                <div class="pop-close" @click="close">
                    
                </div>
            </div>
    </div>
</template>

<script>
import $ from "jquery"

export default {
        name: "Popup",
        props: ["src"],
        created: () => {
        },
        methods: {
            close() {
                $("#i").css({height: "0vh"});
                $(".back").css({opacity: "0%"})
                setTimeout(() => {
                    $(".popup").css({visibility: "hidden"})
                }, 150);
            }
        }
}
</script>

<style>

.back {
    position: fixed;
    width: 100%;
    height: 100%;
    background-color: black;
    opacity: 0%;

    transition: opacity .2s;
}

.popup {
    visibility: hidden;
    position: fixed;
    top: 0%;
    left: 0%;
    width: 100vh;
    height:100vh;
}

.popup > .ph {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
}

#i {
    transition: height .2s;
}

.pop-close {
    cursor: pointer;
    color: white;
    position: fixed;
    top: 0%;
    left: 105%;
    font-size: 50px;
}

</style>