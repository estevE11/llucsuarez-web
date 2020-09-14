<template>
    <div class="popup" id="#pop">
            <div class="back"></div>
            <div class="ph">
                <img id="i" v-bind:src="src">
                <div class="pop-close">
                    X
                </div>
            </div>
    </div>
</template>

<script>
import $ from "jQuery"

export default {
        name: "Popup",
        props: ["src"],
        created: () => {
            $(".pop-close").on("click", () => {
                $(".popup").css({visibility: "hidden"});
                $("#i").css({height: "0vh"});
            })
        }
}
</script>

<style>

.back {
    position: fixed;
    width: 100%;
    height: 100%;
    background-color: black;
    opacity: 80%;
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