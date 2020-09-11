<template>
    <div class="popup">
            <div class="back"></div>
            <div class="ph">
                <img v-bind:src="src">
            </div>
    </div>
</template>

<script>
export default {
        name: "Popup",
        props: ["src"]
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

.popup > .ph > img {
    height: 90vh;
}


</style>