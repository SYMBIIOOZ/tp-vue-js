<template>
    <div>
        <h1>Liste des Photos</h1>
        
        <Photo    v-for="photo of photos" :key="photo" :photo="photo"/>
        
        
    </div>
</template>
<script>
import Photo from "../components/PictureComponent.vue"
    export default {
        components: {
            Photo
        },
        
        data() {
            return {
                photos: []
            }

        },
        async mounted() {
            let result = await fetch('https://jsonplaceholder.typicode.com/photos');
            let photos = await result.json();

            this.photos = photos;
        },
        
        method() {
            
        }
    }

</script>