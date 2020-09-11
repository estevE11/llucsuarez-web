<template>
    <div class="hdr">
        <div class="homeImg"></div>
        <div class="creator">
            <span>Created with ❤ by <a href="https://www.linkedin.com/in/roger-esteve-sanchez-12a265175/">Roger Esteve</a></span>
        </div>
        <div class="data">
            <h1>{{name}}</h1>
            <h3>{{desc}}</h3>
        </div>
        <div class="scroll-button">
            <a href="#cont-photos" class="scroll-link">
                <h4>My work</h4>
                <br>
                <svg version="1.0" xmlns="http://www.w3.org/2000/svg" width="35px" height="35px" viewBox="0 0 512.000000 512.000000" preserveAspectRatio="xMidYMid meet" class="jsx-156389127">
                    <g transform="translate(0.000000,512.000000) scale(0.100000,-0.100000)" fill="white" stroke="none" class="jsx-156389127" data-darkreader-inline-fill="" data-darkreader-inline-stroke="" style="--darkreader-inline-fill:#181a1b; --darkreader-inline-stroke:none;">
                        <path d="M207 4822 l-207 -207 1278 -1278 1277 -1277 1275 1275 1275 1275 -210 210 -210 210 -1065 -1065 -1065 -1065 -1065 1065 c-586 586 -1067 1065 -1070 1065 -3 0 -98 -93 -213 -208z" class="jsx-156389127"></path>
                        <path d="M207 2652 l-207 -207 1223 -1223 1222 -1222 110 0 110 0 1218 1218 c669 669 1217 1222 1217 1227 0 6 -92 102 -205 215 l-205 205 -1068 -1068 -1067 -1067 -1065 1065 c-586 586 -1067 1065 -1070 1065 -3 0 -98 -93 -213 -208z" class="jsx-156389127"></path>
                    </g>
                </svg>
            </a>
        </div>
    </div>
</template>

<script>
import $ from "jQuery"

export default {
    name: 'HomeComponent',
    data() { 
        return{
            name: "LLUC SUAREZ",
            desc: "Photography & Filmmaking"
        }
    },
    mounted() {
        $(".scroll-button a").on("click", e => {
            console.log(e)
            const hash = e.currentTarget.hash;
            if(hash != "") {
                e.preventDefault();

                console.log(hash);

                $("html, body").animate({
                    scrollTop: $(hash).offset().top
                }, 800)
            }
        })
    }
}
</script>

<style scoped>

.homeImg {
    background-image: url("../assets/home_img.jpg");
    height: 100vh;
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
}

.data {
    font-family: "Arial";
    color: white;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
}

.data > h1 {
    letter-spacing: 20px;
}

.scroll-button {
    position: absolute;
    text-align: center;
    left: calc(50% - 54px);
    top: calc(100% - 140px);
}

.scroll-button > a {
    text-decoration: none;
    color: white;
}

.creator {
    position: absolute;
    color: white;
    top: 5px;
    left: 10px;
}

.creator > span > a {
    color: white;
}
</style>
