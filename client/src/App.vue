<template>
    <div id="app">
        <HomeComponent/>
        <PhotosComponent/>
    </div>
</template>

<script>
import HomeComponent from './components/HomeComponent.vue'
import PhotosComponent from './components/PhotosComponent.vue'

export default {
    name: 'App',
    components: {
        HomeComponent,
        PhotosComponent
    }
}
</script>

<style>

#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 0px;
}

body::-webkit-scrollbar {
    visibility: hidden;
    width: 0px;
}

body::-webkit-scrollbar-track {
    visibility: hidden;
}

body::-webkit-scrollbar-thumb {
    visibility: hidden;
}

</style>
