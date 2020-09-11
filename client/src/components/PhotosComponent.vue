<template>
    <div class="photos">
        <div class="cont">
            <b-container fluid class="p-4 bg-dark" id="cont-photos">
                <b-container>    
                    <div v-for="photos in photosArray" v-bind:key="photos" class="row">
                        <div v-for="photo in photos" v-bind:key="photo" class="col">
                            <Photo :src="photo"/>
                        </div>
                    </div>
                </b-container>
            </b-container>
        </div>
        <Popup src="/img/ph_00.jpg"/>
    </div>
</template>

<script>
import Photo from "./Photo.vue"
import Popup from "./Popup.vue"

export default {
    components: {
        Photo,
        Popup
    },
    name: 'PhotosComponent',
    computed: {
        photosArray: () => {
            return [
                ["ph_00.jpg", "ph_01.jpg", "ph_02.jpg"],
                ["ph_03.jpg", "ph_04.jpg", "ph_01.jpg"],
                ["ph_02.jpg", "ph_01.jpg", "ph_00.jpg"],
                ["ph_04.jpg", "ph_03.jpg", "ph_01.jpg"]
            ];
        }
    }
}
</script>

<style scoped>



</style>